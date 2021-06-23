# WMO WIS 2.0 Discovery Metadata exchange, harvesting and search pilot project Engineering Report

## Overview

This directory contains the engineering report and provides
instructions for managing the document.

### Dependencies

Documentation is managed with [Asciidoctor](https://asciidoctor.org).

Link checking is managed with [asciidoc-link-check](https://www.npmjs.com/package/asciidoc-link-check).

### Building

```bash
# create HTML (single page)
asciidoctor --trace -o wis2-metadata-search-engineering-report.html index.adoc
# create PDF
asciidoctor --trace -r asciidoctor-pdf --trace -b pdf -o wis2-metadata-search-engineering-report.pdf index.adoc
```

# check links
```bash
find . -name "???.adoc" -exec asciidoc-link-check -p -c asciidoc-link-check-config.json {} \;
```

**Note**: `Makefile` provides shortcuts to these commands if you are able to run `make`.
