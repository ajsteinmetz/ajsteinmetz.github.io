<< hx >> Talks Presented by Steinmetz, A.

<% for t in talks.presented %>
<< loop.index >>. << r.talk(t) >>
<% endfor %>

<< hx >> Talks Co-Prepared by Steinmetz, A. (Presented by Others)

<% for t in talks.co_prepared %>
<< loop.index >>. << r.talk(t) >>
<% endfor %>

In addition, I have closely collaborated on preparing research and academic talks delivered at the following conferences/institutes: <% for c in talks.collaborated %><< r.text(c) >><< ', ' if not loop.last >><% endfor %>.
