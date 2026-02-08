---
layout: post
title:  "Journal Club Publication Watcher"
date:   2026-01-30 02:21:37 -0500
categories: cofactors enzymes coordination-networks
---
**TL;DR:** I built a Python tool that searches PubMed and CrossRef weekly, finds papers matching your keywords and tracked authors, and generates a PowerPoint presentation + interactive HTML dashboard for easy review. The PowerPoint presentation is because PIs often like to flip through slides.


---

  

## The Problem

Staying current with literature in your field is a constant battle and it doesn't get taught (at least not to me)! Email alerts don't work for me, and I wasn't satisfied with any other tool I found.

For the journal club during my postdoctoral stage (~30 people), we needed a better system. Something that could:


- Track specific authors by ORCID
- Search specific keywords i.e. fields
- Filter by relevant journals
- Generate outputs that work for group discussion



  

## A Solution

**Journal Club Publication Watcher** is a command-line tool that automates the entire literature discovery workflow:

  

```bash

python main.py --auto --mode both

```


Then:

1. Searches PubMed by your configured keywords

2. Searches CrossRef by your tracked authors' ORCIDs

3. Deduplicates results across sources

4. Generates four output formats:

- **PowerPoint** - One slide per paper for visual review

- **HTML Dashboard** - Interactive, sortable table with dark mode

- **Text Summary** - Human-readable report with statistics

- **JSON Export** - Machine-readable for further processing

  


## Key Features

### Multi-Source Search

The tool queries both **PubMed** (via Biopython's Entrez API) and **CrossRef** (via REST API). This dual-source approach catches papers that might only be indexed in one database and allows tracking authors by ORCID regardless of name variations.




### Flexible Configuration

Everything is configured via simple YAML files:

  

```yaml

# keywords.yaml

topics:

- machine learning pathology

- digital pathology

- computational histology

  

# authors.yaml

authors:

- 0000-0001-2345-6789 # Jane Smith

- 0000-0002-3456-7890 # John Doe

```

  

### Smart Date Handling

Configure a lookup frequency like "1 week" or "2 months" and the tool automatically calculates the date range. Or run interactively to specify custom dates.

  

### Multiple Output Formats

The PowerPoint generation creates presentation-ready slides with abstracts, author lists, and DOI links. The HTML dashboard uses DataTables for sorting/filtering and includes a dark mode toggle for late-night literature reviews. Additional feature to open each publication found in Safari such that graphical abstracts can be copied over manually into the Powerpoint presentation.

  



## Getting Started

1. Clone the repository

2. Install dependencies: `pip install -r requirements.txt`

3. Copy sample configs and customize:

```bash

cp config/*.sample.yaml config/

# Edit meta.yaml with your email (required for PubMed)

# Edit keywords.yaml with your search terms

# Edit authors.yaml with ORCIDs to track

```

4. Run: `python main.py`

  













## What's New in v3.7.0

  
This release focuses on code cleanup and consistency:
- Removed legacy duplicate code
- Synchronized version numbers across modules
- Cleaned up commented-out code blocks



## Future Ideas

- Add support for more databases (Semantic Scholar, arXiv)
- Email/Slack notifications for new papers
- Web interface
- Integration with reference managers (Zotero most likely)
- Pulling the graphical abstract from each publication


---

  

**GitHub:** [Journal_Club_Publication_Watcher](https://github.com/aaronledray/Journal_Club_Publication_Watcher)

  

*Built with Python, Biopython, python-pptx, and requests. Open source under GPL v3 license.*




---



