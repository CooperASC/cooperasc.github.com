The website of [Cooper Union](http://cooper.edu)'s Art Student Council.

Powered by [Jekyll](http://jekyllrb.com) and hosted by [Github Pages](http://pages.github.com).

---

## Ordering posts

Posts in Jekyll are displayed in chronological order according to the date in the post's filename `YYYY-MM-DD-Title.md`. Posts which do not follow this naming convention will not appear on the site. 

    |- /notes
       |- 2012-10-23-student-council.md
       |- 2012-10-24-academic-standards.md
       
## Ordering non-chronological posts

Even posts in sections of the site such as `/people` which aren't necessarily ordered chronologically must be named in this date-like format, however you can "hack" the format, as shown below, to control the display order:

    |- /people
       |- 0100-01-01-casey-gollan.md
       |- 0100-01-02-rachel-appel.md
       |- 0100-01-03-jamshed-bharucha.md

## Adding People

To add a new person, create a file in `/_posts/people/` titled `0100-01-XX-Firstname-Lastname.md`. The required YAML Front Matter is as follows:

    ---
    category: people
    layout: people-single
    title: Jamshed Bharucha
    class: Senior
    email: president@cooper.edu
    published: true
    committees:
    - name: Board Chairman
      link: /committees/#board_chairman
    - name: Web and Social
      link: /committees/#web_and_social
    ---