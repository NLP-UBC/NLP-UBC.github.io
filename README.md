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
 *  venue: The conference/journal at which the paper has been accepted
 *  url: Link to the paper on the conference/journal website or arxiv
 *  code: Link to available code, e.g., on github
 *  demo: Link to an interactive demo
 *  software: Link to software packages
 *  slides: Link to presentation slides
 *  video: Link to a presentation video or animations
 *  documents: Link to any other documents

which can be added to any paper by adding the respective tags to the BibTex file (see below).

```
@article{name,
  title={},
  author={},
  year={2021},
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
### Adding, Updating or Removing a Group Member
### Adding a New Showcase Project

## Repository Structure
For more detailed information on what role different parts of the repository play for the UBC NLp website, please refer to the repository structure below:

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
    │     ├── img                       # Folder containing images
    │     │    ├── people               # Folder for images of group members (pls add images of new group members in here)
    │     │    ├── icons                # Folder for icons
    │     │    ├── image.png            # Site-wide images
    │     │    └── [new_image.{png|..}] # Additional images can be added here
    │     └── js                        # Folder containing framework and custom JavaScript files
    ├── bin/{cibuild|deploy}            # Deployment code for the github page, do not touch unless broken
    ├── 404.html                        # Fallback page if requested resource is not available
    ├── Gemfile                         # File containing Ruby gems for plugins
    ├── _config.yml                     # Global config file for website wide properties and jekyll processing
    ├── index.md                        # Content of the homepage (otherwise similar to files in _pages)
    └── README.md



    
