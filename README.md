# sec-parser

<a href="https://project-types.github.io/#federation">
  <img src="https://img.shields.io/badge/project%20type-federation-brightgreen" alt="Federation Badge"/>
</a>


## Overview

The `sec-parser` project simplifies the process of extracting meaningful information from SEC EDGAR HTML documents. It organizes the document's source code into a list or tree of elements that correspond to the visual structure of the document. This includes distinct elements for section titles, paragraphs, and tables, making the data easier to analyze and understand. 

This tool is especially beneficial for Artificial Intelligence (AI) and Large Language Models (LLM) applications. It significantly improves the efficiency of data extraction and analysis in these fields.

## Installation

You can install `sec-parser` using pip:

```bash
pip install sec-parser
```

## Usage

```python
from sec_parser import parse_latest

tree = parse_latest("10-K", ticker="AAPL")

print(tree.render())
# RootSectionElement: PART I — FINANCIAL INFORMATION
# ├── TitleElement: Item 1. Financial Statements
# ├── TitleElement: Apple Inc.
# ├── TitleElement: CONDENSED CONSOLIDATED STATEMENTS OF OPERATIONS (U...
# │   ├── TextElement: (In millions, except number of shares which are re...
# │   ├── TableElement: ...
# │   ...
```

# License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
