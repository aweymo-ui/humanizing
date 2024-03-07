---
title: Bibliometrics
nav: Bibliometrics
---

**Once this data on the document archive was standardized and formatted**, I was able to start on the first digital scholarship aspect of the project, bibliometrics. Bibliometrics are the use of statistical methods to analyze books, articles and other publications, especially in scientific contents. The concept was to see if there was some way to visualize all of the academic work that came out of Taylor to give a sense of the institution’s “research impact,” looking at how many times that work was cited, the changing subject matter over time and seeing how researchers collaborated through co-authorship of papers. 

There are a few different sites people can use to generate bibliometric data but the best one I found for this group of researchers was [Web of Science](https://www.webofscience.com/). Within the site, you can search for specific authors and works, create collections of those items where you can see how they relate to scholarly works and export that data directly.

## Qualitative Questions

In digital scholarship, you will sometimes be faced with qualitative questions around balancing validity and sufficiency of data. In this case, I found that searching for specific names of the scientific papers in Web of Science wasn’t yielding very many results – mainly for two reasons: 

1. These were often early drafts of future publications, which meant the titles didn’t always match up and, mainly, 

2. Web of Science’s data swings very heavily towards more recent papers, with the majority of their data beginning in the late 90s onward. 

This means the vast majority of the papers published from 1970 onward were largely absent.

## What does it mean for a paper to be the direct product of a specific place? 

- Does Taylor need to be mentioned in the title, abstract or body of the text? Does the region need to be mentioned? 
- Are we only looking at work that comes out of University of Idaho or did Washington State research also count? 
- Is it still a product of Taylor if the research was conducting ten or twenty years after the paper is published?


**With this in mind**, I pivoted to looking at authors from the University of Idaho who were present in the archive, rather than specific titles.

Another hurdle: Web of Science doesn’t have a bulk search function where I could simply import a spreadsheet of the 737 individual authors that contributed to the archive collection and find all of the papers they produced. To save myself from a dreary 737 individual searches, I created an equation in Google Sheets that pulled groups of 100 names at a time, such as “k. Aho” OR “H. Akenson” OR “E. Ables” etc. Searching all of these names produced 805 titles, which were exported with all of Web of Science’s (extremely thorough) academic metadata. 

## Network Visualization

I then imported this data into [VOSviewer](https://www.vosviewer.com/), a Dutch, open-source network visualization platform with excellent documentation and much more intuitive interface than it’s open source competitor [Gephi](https://gephi.org/).The Web of Science csv file can be plugged directly into the VOSviewer desktop application and filtered to visualize certain aspects of that data. For this project, I wanted to analyze future citations of specific documents, co-authorship of papers, and fields of interest over time. 

Once these three visualizations are completed, customizations can be done to highlight elements of the data: nodes (circles) representing titles can be colored based on scientific discipline, size of the node can represent the number of times the work has been cited, nodes can be arranged according to when they were published, etc. Selecting a node brings up a pane on the lower right hand corner of the screen which reveals more details on the title and, if available, creates a link to the research paper itself.

These visualizations can then be embedded into a live site, in this case, on our CollectionBuilder. While the visualizations do take about three to five seconds to process all of the JSON data, the bibliometrics add a colorful and interactive element  that reduces hundreds of scholarly papers into a single visualization.

