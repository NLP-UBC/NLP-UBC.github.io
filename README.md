# Guide to the UBC NLP Group Website Repository
  
## General Instructions
The most common case when updating the website will be a pure content change, e.g., adding, updating or removing group members, showcase projects and papers. To make those frequent changes more easy and efficient, we show the most common use-cases for content updates here. In case a structural change needs to be made, please take a look at the repository structure below and refer to [this website](https://jekyllrb.com/) to better understand the framework used.

## Most Common Use-Cases

### Updating Webpage Information (on the Example of the Reading Group Page)
To update information on a webpage, find the appropriate \*.md file in the \_pages folder (here ./\_pages/reading_group.md).
The file content looks something like:
```
---
layout: page
permalink: /reading-group/
title: Reading Group
in_navbar: true
img:
---

#### UBC NLP Reading Group

The UBC NLP reading group (nlp-rg) is organized to discuss recent research papers in NLP. We are currently meeting on:

> DATE, TIME
> LOCATION
> (*LAST UPDATED*)

To stay up-to-date, please feel free to join our Mailing List by signing up to nlp-rg@cs.ubc.ca through Majordomo. 

For questions, issues and inquiries, please email ubc-nlp@cs.ubc.ca
```
The first part between the "---" is the so called [front matter](https://jekyllrb.com/docs/front-matter/), defining the layout and metadata, such as the URL link, the title, a flag indicating if the page should be listed in the navigation and an optional image (shown at the top of the page if selected). While setting these parameters is important when creating a new webpage, they are not directly content related and should only be touched with clear intention.

Everything after the second "---" is the content of the page, formatted in [YAML](https://learn-the-web.algonquindesign.ca/topics/markdown-yaml-cheat-sheet/) and shown on the page. In this section, we can, for example, change the date, time and location of the reading group or add additional information if necessary.

### Adding a New Paper
With the website design based on Jekyll, the rather frequent action of adding a new paper to the website has become especially straight-forward. Once you got a paper accepted or published, simply open the ./\_bibliography/papers.bib file and paste the paper BibTex at any position.

To facilitate a variety of additional resources linked to a paper, we set up 8 generic tags
 *  **venue**: The conference/journal at which the paper has been accepted
 *  **url**: Link to the paper on the conference/journal website or arxiv
 *  **code**: Link to available code, e.g., on github
 *  **demo**: Link to an interactive demo
 *  **software**: Link to software packages
 *  **slides**: Link to presentation slides
 *  **video**: Link to a presentation video or animations
 *  **documents**: Link to any other documents

which can be added to any paper by adding the respective tags to the BibTex file (see below).

```
@article{name,
  title={},
  author={},
  year={},
  ...
  venue={},
  url={},
  code={},
  demo={},
  software={},
  slides={},
  video={},
  documents={}
}
```

If you're the first person in a new year to add a paper, there is one additional step: Go to ./\_pages/publications.md and add the recent year to the _years_ list in the file [front matter](https://jekyllrb.com/docs/front-matter/) as shown below:

```
---
layout: page
...
years: [NEW_YEAR, 2022, 2021, 2020, 2019, 2018, ...]
---
```

### Adding News
To add a news item, create a new markdown (\*.md) file under ./\_news. The name of the file does thereby not matter and can be anything from a simple enumeration to the news topic or date. The general structure should look as follows:

```
---
layout: post
date: DATE_OF_NEWS
img:
---

This is the news content
```

The [front matter](https://jekyllrb.com/docs/front-matter/) requires the date of the item, which is used to determine their order. Be aware, if you backdate news, they will likely not appear on the homepage, where only the latest news are shown. The _img_ tag allows to optionally add an image, which will be shown along with the news text. After the front matter, the content of the file is shown as the news item.

### Adding, Updating or Removing a Group Member
Another frequent action is adding, updating and removing group members, including faculty, post-docs, students and research associates. 

Adding a new group member is similar to generating a new news item. First, generate a new markdown (\*.md) file under ./\_people. The name of the file can technically be anything, however, we recommend using the group members name. The structure of a group member markdown file looks like this:

```
---
layout: post
date: START_DATE
name: NAME
role: PICK_A_ROLE # {faculty|student|postdoc|researcher}
type: ROLE_SPECIFICATION # e.g., {PhD Candidate|PhD Student|Master Student|Visiting Student|...}
img: IMAGE.png
link: URL # Link to the individual professional website
status: STATUS # {active|inactive}
research: RESEARCH_AREA # e.g., NLP, Summarization, Question Answering, ...
job: JOB_AFTER_GRADUATION # Job shown if the group member is inactive
---
```

A few notes on creating and updating the group members markdown file: 
  * Group member files do not contain any content after the [front matter](https://jekyllrb.com/docs/front-matter/)
  * The _role_ must be one of the pre-defined options (faculty|student|postdoc|researcher)
  * _type_, _link_ and _research_ are optional free-text fields to specify group members. Despite being optinoal, it is highly encouraged to add information
  * _img_ contains the filename of a **square-sized** image of the group member, uploaded to ./assets/img/people. To crop your image into square format, we recommend the easy-to-use, free, browser-based tool [Pixlr](https://pixlr.com/e/) or any other photo editing software 
  * The _status_ field indicates if a group member is still an active part of the UBC NLP group. If the member is currently part of the group, set the attribute to _active_, otherwise set to _inactive_, which will move the member from the list of group members into the past members section (bottom of the people page)
  * _job_ is another optional field reserved for _inactive_ group members, defining their role and company/univeristy after leaving the UBC NLP group

To remove a group member, either the group member markdown file can be deleted from the repository (i.e., hard-delete, the member will be completely gone from the website) or the _status_ can be set to _inactive_ (i.e., moving the member into the past members section).

### Adding a New Showcase Project
To highlight a completed project beyond the publication list (see section _Adding a New Paper_), we added a _Showcase Projects_ page, where additional details, demos, corpora-links and explanations can be given in a more free-form manner. Every project is represented by a markdown (\*.md) file in the ./\_showcase folder. Again, the name does technically not matter, however, we encourage people to be descriptive with their naming scheme. The structure of a showcase project file looks as follows:

```
---
layout: post
date: DATE
img: IMAGE.png
title: TITLE
link: LINK_ON_IMG
---

###### We are proudly presenting our new project

TL;DR of the project goals and impact (e.g., a shortened version of the abstract). Try to keep the description to about 1-3 sentences.

List of links and resources.
```

The [front matter](https://jekyllrb.com/docs/front-matter/) of a showcase project contains the _date_, used for ordering projects in reverse chronological order, an _image_ (highly recommended; please use reasonable landscape ratio) as well as a _title_ and _link_.

After the [front matter](https://jekyllrb.com/docs/front-matter/), the project can be described with standard [YAML](https://learn-the-web.algonquindesign.ca/topics/markdown-yaml-cheat-sheet/) syntax. For consistency between projects, we highly recommend using a Header-6 (###### Title) font for the title. To describe the main content of the project, please limit yourself to a few sentences, to avoid overcrowding of the page. In the final paragraph, add links to further resources and the paper itself.

### Standalone Project Page
If a section on the showcase page is not enough to describe the project in sufficient detail, or you have additional, custom requirements (e.g., host a dataset, require a user consent form, ...), a stand-alone project page can be created by generating a new markdown (\*.md) file of arbitrary name (ideally the project name) in the ./\_pages folder of the following structure:

```
---
layout: project_page
permalink: /LINK/
title: TITLE
in_navbar: false
img:
---

#### Project Title

##### Content Section 1
...

##### Content Section n
...
```

The [front matter](https://jekyllrb.com/docs/front-matter/) _layout_ property needs to be set to _project_page_ standalone projects, adding additional spacing around the content to align with the website design. The _permalink_ defines the relative path to the main webpage at which the project will be published, facilitating deep-linking directly to the project. Further define the _title_ and an optional _img_ to show at the top of the page. Please note: The _in_navbar_ parameter needs to be set to false, to not show the page in the main navigation. At the same time, don't forget to link the standalone page in the publication and the (optional) showcase page (see above sections).

## Repository Structure
For more detailed information on what role different parts of the repository play for the UBC NLP website, please refer to the repository structure below:

    .
    ├── .github/workflows               # Deployment code for the github page, do not touch unless broken
    ├── _bibliography                   # Folder for style and content of the bibliography page
    │     └── papers.bib                # BibTex style list of group publications (add new papers here!)
    ├── _includes                       # Folder for static HTML fragments and widgets
    │     ├── footer.html               # Footer fragment of the website
    │     ├── head.html                 # <head></head> portion of the document, containing style and code imports
    │     ├── header.html               # Header fragment containing UBC logo, navigation and UBC-NLP sub-header
    │     ├── news_ticker.html          # News-ticker widget used on the homepage to show the top-n latest news
    │     └── [other_fragments.html]    # Additional fragments and widgets can be added here for dynamic content
    ├── _layouts                        # Folder for hierarchical HTML website structure
    │     ├──default.html               # Contains the root (most outer) website structure
    │     ├──page.html                  # Contains the structure of a single webpage with dynamic content area
    │     ├──news.html                  # Custom structure for listing news (extends page.html)
    │     ├── ...                       # [Additional structures left out for brevity]
    │     ├──people.html                # Custom structure for listing group members (extends page.html)
    │     └── [custom_pages.html]       # Additional pages that require iteration over a dynamic set of datapoints
    ├── _pages                          # Folder for page content
    │     ├── news.md                   # Static page content outside of dynamic portion, e.g. for captions
    │     ├── ...                       # [Additional pages left out for brevity]
    │     ├── reading_group.md          # Static page content without dynamic components
    │     └── [new_page_content.md]     # Additional pages (static or dynamic) can be added here
    ├── _news                           # Folder for news items
    │     ├── news_1.md                 # Structured markup file for a news item, which will be dynamically shown 
    │     └── [news_n.md]               # Additional news items can be added as individual files here
    ├── _people                         # Folder for group members
    │     ├── person_1.md               # Structured markup file for a group member, which will be dynamically shown 
    │     └── [person_n.md]             # Additional group members can be added as individual files here
    ├── _showcase                       # Folder for showcase projects
    │     ├── showcase_1.md             # Structured markup file for a showcase project, which will be dynamically shown
    │     └── [showcase_n.md]           # Additional showcase projects can be added as individual files here
    ├── assets                          # Folder for local assets
    │     ├── css                       # Folder containing framework and custom CSS files
    │     ├── js                        # Folder containing framework and custom JavaScript files 
    │     └── img                       # Folder containing images
    │          ├── people               # Folder for images of group members (pls add images of new group members in here)
    │          ├── icons                # Folder for icons
    │          ├── image.png            # Site-wide images
    │          └── [new_image.{png|..}] # Additional images can be added here
    ├── bin/{cibuild|deploy}            # Deployment code for the github page, do not touch unless broken
    ├── 404.html                        # Fallback page if requested resource is not available
    ├── Gemfile                         # File containing Ruby gems for plugins
    ├── _config.yml                     # Global config file for website wide properties and jekyll processing
    ├── index.md                        # Content of the homepage (otherwise similar to files in _pages)
    └── README.md



    
