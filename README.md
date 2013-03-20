## About

This is the website of [Cooper Union](http://cooper.edu)'s Art Student Council. It's designed to be a toolkit aiding students in _enacting_ transparency and accountability — rather than just _talking_ about these things — in a way that _is itself_ transparent and accountable. (For more on that, see the [philosophy](#philosophy) section below.)

Art Student Council's notes have been cited by the New York Times, printed and stapled to the walls of the building by our readers, and spawned many online discussions in the viral sharing of _meeting content_. Who woulda thunk?

---

## Stay In The Loop

With [a bunch of Student Council members](https://github.com/CooperASC?tab=members) using this site as a scratchpad and clearinghouse for information, it may seem difficult to keep track of everything going on. However, there are several ways you can stay updated:

### By Text Message

Text "Follow CooperASC" to 40404 and you'll get a message like the one below every time the site changes:

> @CooperASC: [[http://cooperasc.github.com](http://cooperasc.github.com)] http://cooperasc.github.com/commit/... Casey Gollan - adding faculty meeting non-notes

These notifications are free, but if you don't have unlimited text messaging your carrier may charge you.

You can unsubscribe from these notifications at any time by texting "Stop" to 40404.

### On Twitter

Follow [@CooperASC on Twitter](http://twitter.com/CooperASC), which tweets every time the site changes.

### By Checking the Commit History

If you prefer not to get notified about every little change, but still want to check in from time-to-time, vist the site's [commit history](http://github.com/CooperASC/cooperasc.github.com/commmits) to explore a log of site changes.

## Add and Edit Content

Anyone who is a [member of student council](https://github.com/CooperASC?tab=members) can create new pages and edit any page on this site.

### Creating a new note

The easiest way to add new notes is through an online text editor called Prose.

1. Visit [http://prose.io](http://prose.io/) and sign in with your Github account
2. Under Organizations, find [`CooperASC`](http://prose.io/#CooperASC) and click it to enter our group's files
3. Click [`CooperASC.github.com`](http://prose.io/#CooperASC/cooperasc.github.com) to enter the contents of this site
4. Click the folder for [`Notes`](http://prose.io/#CooperASC/cooperasc.github.com/_posts/notes)
5. In the top right click [`+ New File`](http://prose.io/#CooperASC/cooperasc.github.com/_posts/notes/new), to be taken to the editing interface for a new note

SCREENSHOT OF PROSE NEW FILE

### Editing a note

There are three parts of every note

1. **Filename** — contains the date and URL name
2. **Metadata** — structured information like title, author, and tags
3. **Content** — where your write your content

ANNOTATED SCREENSHOT OF PROSE NEW FILE

#### 1. Filename

The filename determines a note's date and URL text. Notes which do not follow the following filename format will not appear on the site:

	/_posts/notes/YYYY-MM-DD-title-firstname.md

Make sure you have:

- a properly formatted date
- seperated words with dashes (NOT spaces)
- written in lowercase
- omitted unneccesary words like "meeting" for brevity

For example:

	/_posts/notes/2013-03-04-faculty-casey.md

#### 2. Metadata

A note's metadata is a list of information like the title, notetaker (that's probably you), and associated committees. Metadata also determines a bunch of site-related functions such as where to display a note, what layout to use, and if it's published or private.

To edit metadata in Prose, hit the toolbar button labeled `Metadata`. A drawer will open below the toolbar with the following preset text.

	category: notes
	layout: notes-single
	published: true
	title: Meeting or Note Title
	notetaker: Firstname Lastname
	tags: committee-name
	filepath: _posts/notes/filename.md

You can edit everything after the colons (`:`). The `category:`, `layout:`, and `published:` fields are already correct, but you'll want to change the `title:`, `notetaker:`, `tags:`, and `filepath:` fields reflect your particular note. Below, you can see a completed set of metadata:

	category: notes
	layout: notes-single
	published: true
	title: Emergency Meeting of The Faculty of the School of Art
	notetaker: Casey Gollan
	tags: faculty
	filepath: _posts/notes/2013-03-04-faculty-casey.md

**Note metadata properties, explained:**

| Property | What it means and _[options]_ |
| ----- | ----------- |
| category | What section of the site this content is displayed in. The site sections are the folders beneath `/_posts`. _[about, committees, notes, people]_ |
| layout | What layout to display this content with. Available layouts are in the `_layouts` directory. _[default, index, about-index, committees-index, notes-index, people-index, notes-single, people-single]_ |
| published | Determines whether or not a page is generated for this content. If a file is set to `private` and saved it will not be shown on index pages or have a webpage generated for it, BUT it will _still_ be publicly visible in the Github repository. _[private, published]_ |
| title | The page title as it will be displayed to readers. Whereas the `filename` should be terse (e.g. `faculty.md`), this field can be descriptive. _[e.g. Faculty Meeting]_ |
| notetaker | The name of the author. If the notetaker field matches the name of a profile in the `/people` section of the site, the site will atuomatically link to their profile from the note, and link to their notes from their profile. _[e.g. Casey Gollan]_ |
| tags | A comma-separated list of dash-separated tags to aid searching and sorting of notes. If the same tag is used in multiple notes, the site will automatically link between them in the `Tools` sidebar. Standardized tags exist for committees, but new ones may be invented as needed for non-committee meetings or notes. _[student-council, faculty-administration, board-chair, fun, faculty, documents-received, art-student-body]_ |
| filepath | The filepath should match your completed filename, with no beginning slash. You can copy-and-paste it from the filename box. This steps is somewhat redundant, but important! If a `filepath` is present, the site will show readers handy shortcut links to where they can edit and review the history of your content. If the filepath is incorrect, readers will end up at a broken link and be very confused, so be sure to test your sidebar links out after publishing! _[e.g. `_posts/notes/2013-03-04-faculty-casey.md`]_ |

## Adding and Remove Members
			 
### Creating new People pages

So you've been added to the Organization on Github, great! This means that you can now edit the site, so the first thing you should probably do is make yourself a page on the site. To add a new person page, create a new file in `/_posts/people` titled `0100-01-01-firstname-lastname.md`. The required metadata is as follows:

	category: people
	layout: people-single
	published: true
	title: Firstname Lastname
	class: Senior
	tags: committee-name
	preferred_email: email@address.com
	gravatar_email: email@address.com
	permalink: /people/firstname-lastname/


	category: people
	layout: people-single
	published: true
	class: Senior
	title: Casey Gollan
	tags: board-chair, admissions
	preferred_email: caseygollan@gmail.com
	gravatar_email: caseygollan@gmail.com
	permalink: /people/casey-gollan/

### Adding Committees

### Larger Site Changes: Editing Locally

#### Desktop Git Clients

For those who are not comfortable with Git's command line interface, Github has decent clients for [Mac](http://mac.github.com) and [Windows](http://windows.github.com) that make cloning, pushing, and pulling a single-button affair.

## Philosophy

### Git & Github

- Collaboration
- Redundancy
- Archival
- Transparency
- Clone / Fork / Push / Pull

### Jekyll

- Why flat file?