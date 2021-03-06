---
title: About
layout: page
permalink: /about.html
---

# Academic Librarian Status

Academic librarians hold a variety professional status in different institutions.
However, information about librarian status is not easy to discover. 

During the promotion and tenure process librarians are often required to find external librarians of the same status to review their packets.
Thus, this lack of information presents a "pesky bottleneck", as [Elizabeth Choinski observes in *College & Research Libraries News* (2016)](https://crln.acrl.org/index.php/crlnews/article/view/9460/10708). 
Choinski encourages institutions to better represent librarian status in their web directories and for librarians to contribute information to the [Academic Librarian Wikispaces (archived)](https://web.archive.org/web/20180307020737/http://academic-librarian-status.wikispaces.com/).

When Wikispaces was shut down in 2018, the content was migrated to the [Academic Librarian Status](https://academiclibrarianstatus.wordpress.com/) WordPress site.
It does not appear to have been updated since. 
This website harvested that data and presents it as a sortable, searchable table for better ease of use (plus a few minimal updates to the data).

You may also be interested to see ACRL ["Standards for Faculty Status for Academic Librarians"](http://www.ala.org/acrl/standards/standardsfaculty) and ["Standard for the Appointment, Promotion and Tenure of Academic Librarians"](http://www.ala.org/acrl/standards/promotiontenure).

Records in this data set:

{% assign items = site.data.librarian_status %}
{%- assign options = items | map: "status" | uniq -%}
{:.table .table-bordered }
| professional status | count |
| --- | --- |
{% for i in options %}| {{ i }} | {{ items | where: 'status',i | size }} |
{% endfor %}

--------

- Source code: [academic-librarian-status]({{ site.source-code }}) *(get in touch with GitHub Issues)*
- Built with: [Jekyll](https://jekyllrb.com/), [Bootstrap](https://getbootstrap.com/), [DataTables](https://datatables.net/).
- Last build date: {{ site.time | date: "%Y-%m-%d" }}.
