## Pubs 📚

<style>
  /* Reusable container for badges */
  .badge-box {
    background-color: #ffffff;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    margin: 5px 0;
  }
</style>

<script>
  document.addEventListener("DOMContentLoaded", function(){
    // For Altmetric badges: inject common attributes into every element with the "donut-badge" class
    document.querySelectorAll(".donut-badge").forEach(function(el) {
      el.setAttribute("data-badge-type", "donut");
      el.setAttribute("data-badge-popover", "right");
      el.setAttribute("data-hide-no-mentions", "false");
    });
    
    // For Dimensions badges: inject common attributes into every element with the "small-dimensions-badge" class
    document.querySelectorAll(".small-dimensions-badge").forEach(function(el) {
      el.setAttribute("data-hide-zero-citations", "false");
      el.setAttribute("data-style", "small_circle");
      el.setAttribute("data-legend", "hover-left");
    });
  });
</script>

<script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>

<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js"></script>

<p>🔗 Links to official publications, arXiv preprints, and GitHub projects are provided.</p>

<p>🔗 All public work is freely available on <a href="<< profile.links.arxiv >>">arXiv</a>. See also <a href="<< profile.links.scholar >>">Google Scholar</a> and <a href="<< profile.links.inspire >>">INSPIRE-HEP</a>.</p>

<% macro pubtable(title, items, badges=true) %>
<h4><< title >></h4>
<table border="1">
  <thead>
    <tr>
      <th>Full Citation</th>
<% if badges %>
      <th>Dimensions Badge</th>
      <th>Altmetric Badge</th>
<% endif %>
    </tr>
  </thead>
  <tbody>
<% for p in items %>
    <tr>
      <td>
        << h.cite(p) >>
      </td>
<% if badges %>
<% set doi = h.badge_doi(p) %>
      <td>
        <div class="badge-box">
          <span class="__dimensions_badge_embed__ small-dimensions-badge" data-doi="<< doi >>"></span>
        </div>
      </td>
      <td>
        <div class="badge-box">
<% if p.altmetric_id is defined %>
          <div class="altmetric-embed donut-badge" data-altmetric-id="<< p.altmetric_id >>"></div>
<% else %>
          <div class="altmetric-embed donut-badge" data-doi="<< doi >>"></div>
<% endif %>
        </div>
      </td>
<% endif %>
    </tr>
<% endfor %>
  </tbody>
</table>
<% endmacro %>
<< pubtable('Peer-Reviewed Journal Articles', pubs.journal) >>
<< pubtable('Book Chapters &amp; Review Articles', pubs.chapter) >>
<< pubtable('Institutional &amp; Technical Reports', pubs.report, badges=false) >>
<< pubtable('Dissertation', pubs.dissertation) >>
