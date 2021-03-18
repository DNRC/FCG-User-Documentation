# FCG User Documentation
This repository contains the user documentation for the Montana DNRC's Financial Code Generator, which is an application
used to associate DNRC business information and a billable financial code to incidents in the [IRWIN] system.

The application itself can be found at https://fcg.dnrc.mt.gov/

## Building

This repository can be used to generate a PDF file or static website using [MkDocs]. Follow the linked instructions to install the tool.
To generate a PDF, the [MkDocs PDF Export Plugin] needs to be installed as well.

Run the following in the root directory of the repo to start a development server to see live updates of your changes:

``` sh
mkdocs serve
```

The site preview will then be accessible at http://127.0.0.1:8000

To build the static files, run
``` sh
mkdocs build
```

All generated files will be placed into the `site` directory. The generated PDF can be found at `site/pdf/combined.pdf`.

## File Format

MkDocs uses the Markdown file format for all of its content files. If you are not familiar with Markdown, the following resources will be helpful:
+ https://www.markdownguide.org/
+ [Basic Markdown syntax]
+ [Extended Markdown syntax]

[IRWIN]: https://forestsandrangelands.gov/WFIT/applications/IRWIN/index.shtml
[MkDocs]: https://www.mkdocs.org/
[MkDocs PDF Export Plugin]: https://github.com/zhaoterryy/mkdocs-pdf-export-plugin
[Basic Markdown syntax]: https://www.markdownguide.org/basic-syntax/
[Extended Markdown syntax]: https://www.markdownguide.org/extended-syntax/
