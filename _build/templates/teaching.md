## Teaching ✏️

**Key:** <% for k in profile.institution_key %><< k.key >> (<< r.text(k.name) >>)<< ", " if not loop.last >><% endfor %>


<% for g in teaching.groups %>
### Teaching Record (as << g.role >>)<< r.fn('evaluations') if loop.first >> - << g.key >>

<< r.md_table(['Course #', 'Course Title', 'Delivery Method', '# of Sections', '# of Students', 'Semester'],
              r.course_rows(g.courses, ['code', 'title', 'delivery', 'sections', 'students', 'term'])) >>

<% set notes = r.fnlist() %>
<% if notes %>
<< notes >>

<% endif %>
<% endfor %>
