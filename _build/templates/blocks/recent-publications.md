<# website index.md: the three most recent publications (first entries of publications.yml, excluding reports/in-prep/dissertation) #>
<% for p in pubs_all if p.type in ['journal', 'chapter'] %>
<% if loop.index <= 3 %>
* << r.cite(p) >>
<% endif %>
<% endfor %>
