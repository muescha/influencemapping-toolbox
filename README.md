# Influence Mapping Toolbox

[![Stories in Ready](https://badge.waffle.io/iilab/influencemapping-toolbox.png?label=ready&title=Ready)](http://waffle.io/iilab/influencemapping-toolbox)

# About the Influence Mapping Toolbox

The influence mapping toolbox brings together resources to help you

 * [Identify data for your project](http://iilab.github.io/influencemapping-toolbox/practices/collecting.html)
 * [Organise your data](http://iilab.github.io/influencemapping-toolbox/practices/organising.html)
 * [Make sense of your data](http://iilab.github.io/influencemapping-toolbox/practices/analysing.html)
 * [Present your data and findings](http://iilab.github.io/influencemapping-toolbox/practices/publishing.html)

The Toolbox has been developped by [iilab - information innovation lab](https://iilab.org) as part of the [Influence Mapping](http://influencemapping.org) project.  

## What is influence mapping?

Influence mapping is an emerging, diverse field. Situated somewhere between data journalism, network visualisation, political science and activism, influence mapping is still building an identity as a practice in its own right. You could be an influence mapper and not even know it yet.

Influence mapping is at a stage now where there are many people doing similar work but, because the community is still fragmented, learning is not being shared as effectively or as widely as it could be. To make the most of the excellent work and expertise already in the space, we set out to create a resource where the varied expertise and in-depth knowledge of influence mappers can be shared and built upon: a toolbox that will help newcomers and experts to map influence and make the most of their work.

So, what is influence mapping? Primarily, influence mapping is about making impact. This can be through a diverse range of practices that span from journalism to activism to research. It can be about finding things out - revealing secrets, discovering a story. Or it can be about getting the word out, telling a story, or even generating evidence that can be used in a legal process. Or it can be about making tools and databases that make doing all that easier. 

Whether that’s through identifying key people, exposing or creating transparency in power relationships, or network mapping and visualisation, influence mapping is ultimately a way to hold accountable those in power - a process that allows citizens to have oversight on governments, organisations and corporations.

Thus, we can delineate influence mapping as projects using varied methodologies and creating tools that help to find evidence, stories and visualisations that aim to hold those in power accountable for their decisions

We’ve used this loose definition to guide the design of the influence mapping toolbox. This toolbox aims to help people learn about existing influence mapping projects, and to share learning about common practices, tools and project experiences, so that influence mapping as a practice can grow and have even more impact.

## Why we made the toolbox

The idea for the Influence Mapping Toolbox came from discussions of the [Influence Mapping community](http://influencemapping.org), a group of practitioners involved in understanding networks of power, established in early 2015. The project was born out of a desire to share the knowledge accumulated in the many and diverse projects and investigations that fall within this loosely defined space - to define the space further and to help others who might want to do similar work. The Influence Mapping community asked [iilab](https://iilab.org) to take on this fascinating project. The work has been carried out by Lilas Duvernois, Kat Austen and Jun Matsushita.

The contents of the website are published under the Creative Commons CC-BY license and the data files are downloadable under ODBL.

## How we did it

Starting from a spreadsheet of projects compiled by Friedrich Lindenberg, research was carried out to add to this list by performing gap analyses, and reaching out to through the iilab networks and the influence mapping community to discover more projects. Through detailed analysis of the projects found, a draft taxonomy for projects and tools was developed, which was shared with the Influence Mapping community for feedback. This was developed iteratively as part of the research and content generation process, including the Technology for Investigative Journalism meeting in London.

In parallel, a user centric approach was applied to the end product design. Projects that were in an early phase were sought out as subjects for user research. Practitioners completed a [short questionnaire](https://docs.google.com/a/iilab.org/forms/d/149mqSqwxCWZDkBT2RhEph-H4ZyOudcWjhbi2Wffz0vU/viewform) which researched their explicit and implicit motivations for their work, backgrounds and needs. The answers were coded, user personas were generated, and a draft user journey was produced, which was refined after attendance and observation of the Technology for Investigative Journalism meeting in London. 

Finally, a series of case studies were made to further interrogate the influence mapping space. The case studies were chosen as representative of a broad spectrum of types of projects, stages in their development and geographic and institutional backgrounds. Project leaders were contacted for interview, and the interview transcripts subject to a two-stage coding process comprising initial descriptive coding, and a second phase of closed coding, using grounded theory produce conceptual categories from the research data. The case study reports are linked from each case study page, and the learning from the case studies and project studies for the website content has been used to inform the Influence Mapping: State of the Art report, which gives an overview of the influence mapping space at the close of 2015.

## Technology

Requirements
 - node.js ```brew install node``` on OSX. 
 - metalsmith ```npm install -g metalsmith```

Installation
 - ```git clone https://github.com/iilab/influencemapping-toolbox.git```
 - ```cd influencemapping-toolbox```
 - ```npm install```

Build
 - ```metalsmith``` will build the site in the ```build``` directory.

Features
 - Generation of the website using the [Metalsmith](http://www.metalsmith.io/) static website generator.
 - Data managed in [google spreadsheet](https://docs.google.com/spreadsheets/d/1j2hl7TlGGoKmO5EVkibU1LASk9p1ncmimI7-26JFX1g/edit?pref=2&pli=1#gid=1087369693) for [tools](https://docs.google.com/spreadsheets/d/1j2hl7TlGGoKmO5EVkibU1LASk9p1ncmimI7-26JFX1g/edit?pref=2&pli=1#gid=1475648190), [projects](https://docs.google.com/spreadsheets/d/1j2hl7TlGGoKmO5EVkibU1LASk9p1ncmimI7-26JFX1g/edit?pref=2&pli=1#gid=0) and [practices](https://docs.google.com/spreadsheets/d/1j2hl7TlGGoKmO5EVkibU1LASk9p1ncmimI7-26JFX1g/edit?pref=2&pli=1#gid=581909931) and exported [as csv files](https://github.com/iilab/influencemapping-toolbox/tree/master/src/data) used for the generation of static pages.
 - Basic project, tool and practice page formatting using [nunjucks formatting in markdown](https://github.com/iilab/influencemapping-toolbox/blob/master/layouts/project.md) and [pandoc markdown conversion](https://github.com/iilab/metalsmith-pandoc) to html with [GFM definition_lists and markdown_in_html_blocks](https://github.com/iilab/influencemapping-toolbox/blob/master/metalsmith.json#L132).
 - Filtered [slick](https://kenwheeler.github.io/slick/) carousel to display relevant Projects and Tools on Practice and Sub-Practice pages.
 - [Static client side indexing with Lunr](https://github.com/iilab/influencemapping-toolbox/blob/master/metalsmith.json#L103-L130)
 - [VisualSearch.js](http://documentcloud.github.io/visualsearch/) for search.
 - [Filter.js](https://github.com/jiren/filter.js) for faceted browsing.


## How you can contribute

 - Content: you can help review the content and let us know if there are problems.
 - Code: Look at the issues tagged with "Help Wanted" and dicuss with us changes or improvements you are thinking of!
 - Do an awesome influence mapping project: [join the influence mapping google group](https://groups.google.com/forum/#!forum/influencemapping) and let us know about what you're doing.
 
