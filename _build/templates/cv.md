## C.V. 📄

### << profile.name >>, << profile.credential >>

Updated << r.mon_year(profile.updated) >> - [Download CV (PDF)](<< profile.cv_pdf >>)

- **Email:** <a href="mailto:<< profile.email >>"><< profile.email >></a>
- **Website:** [<< profile.website >>](<< profile.website >>)
- **ORCID:** [![ORCID](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/<< profile.orcid >>)&nbsp;[<< profile.orcid >>](https://orcid.org/<< profile.orcid >>)

### Employment

<% set rows = [] %>
<% for e in employment %>
<% do rows.append([r.text(e.title) ~ r.fn(e.get('footnotes')), r.text(e.department), r.text(e.institution), r.span(e.start, e.get('end'), r.mon_year)]) %>
<% endfor %>
<< r.md_table(['Position Title', 'Department', 'Institution', 'Dates'], rows) >>

<< r.fnlist() >>

### Education

<% set rows = [] %>
<% for e in education %>
<% do rows.append([e.degree, r.text(e.field), r.text(e.institution) ~ r.fn(e.get('footnotes')), r.mon_year(e.date)]) %>
<% endfor %>
<< r.md_table(['Degree', 'Field', 'Institution', 'Dates'], rows) >>

<< r.fnlist() >>

### Research Interests

<% for ri in profile.research_interests %>
- **<< r.text(ri.label) >>:** << r.text(ri.text) >>
<% endfor %>

<% set diss = pubs.dissertation[0] %>
### Dissertation

- **Title:** << r.text(diss.title) >>
- **Committee:** <% for c in diss.committee %>Prof. << r.esc(c.name) >> (<< c.role >>)<< ", " if not loop.last >><% endfor %>

- **Identifiers:** << r.pub_ids(diss) | join(', ') >>
- **Presentation:** << r.ident(diss.presentation_doi, 'https://doi.org/' ~ diss.presentation_doi) >>

### Publications

Citations = << profile.metrics.citations >>; h-index = << profile.metrics.h_index >> ([<< profile.metrics.source >>](<< profile.links.scholar >>), << r.mon_year(profile.metrics.as_of) >>). See also [INSPIRE-HEP](<< profile.links.inspire >>) and [arXiv](<< profile.links.arxiv >>).

<% macro publist(title, items) %>
#### << title >>

<% for p in items %>
<< loop.index >>. << r.cite(p) >>
<% endfor %>
<% endmacro %>
<< publist('Peer-Reviewed Journal Articles', pubs.journal) >>
<< publist('Book Chapters & Review Articles', pubs.chapter) >>
<< publist('Institutional & Technical Reports', pubs.report) >>
<< publist('Works in Progress', pubs['in-prep']) >>
### Conference Presentations & Talks

<% set hx = '####' %>
<% include '_talks.md' %>

### Grants & Awards

<% for a in awards_all %>
<< loop.index >>. << r.award(a) >>
<% endfor %>

### Teaching Experience (as Instructor-of-Record)<< r.fn('evaluations') >>

**Key:** <% for k in profile.institution_key %><< k.key >> (<< r.text(k.name) >>)<< ", " if not loop.last >><% endfor %>


<< r.md_table(['Course #', 'Course Title', 'Delivery Method', '# of Sections', '# of Students', 'Institution', 'Semester'],
              r.course_rows(teaching_groups.gt.courses + teaching_groups['ua-act'].courses,
                            ['code', 'title', 'delivery', 'sections', 'students', 'inst', 'term'])) >>

<< r.fnlist() >>

<% for gid in ['pcc', 'ua-ta'] %>
<% set g = teaching_groups[gid] %>
- **<< r.text(g.summary_heading) >>:** <% for label, yrs in r.teaching_summary(g) %><< label >> (<< yrs >>)<< ", " if not loop.last >><% endfor %>

<% endfor %>

### Academic Service & Associations

#### Institutional Committees & Appointments
<% for s in service.institutional %>
- << r.service(s) >>
<% endfor %>

#### Professional Service & Membership
<% for s in service.professional %>
- << r.service(s) >>
<% endfor %>
- << r.reviewer(service.reviewer) >>

#### Laboratory Safety Certifications
<% for c in certifications %>
- << r.text(c.name) >>, << c.unit >> (<< c.year >>)
<% endfor %>

#### Public Outreach
<% for o in outreach %>
<< loop.index >>. << r.outreach(o) >>
<% endfor %>

### External & Institutional Press

<% for p in press %>
<< loop.index >>. << r.press(p) >>
<% endfor %>

### Other Links and Websites

<% set rows = [] %>
<% for i in range([profile.professional_links | length, profile.social_links | length] | max) %>
<% set a = profile.professional_links[i] if i < profile.professional_links | length else none %>
<% set b = profile.social_links[i] if i < profile.social_links | length else none %>
<% do rows.append([r.link(a.label, a.url) if a else '', r.link(b.label, b.url) if b else '']) %>
<% endfor %>
<< r.md_table(['Professional', 'Socials'], rows) >>

My Erd<< r.esc('ő') >>s number is << profile.erdos.number >>. [(Source)](<< profile.erdos.source >>)
