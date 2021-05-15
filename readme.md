# FondecyTeX

LaTeX templates mimicking Microsoft Word forms which constitute part of an application to the [ANID 2022 Fondecyt Regular National Competition](https://www.anid.cl/concursos/concurso/?id=603).

## Disclaimer

This repository is provided in the hope that it will be useful, but I cannot provide any guarantee that it will work for you.
It is certainly not intended for LaTeX novices.

Should you want to use these templates, I **strongly** recommend producing a quick and dirty draft, including filling out those complicated tables of the _Requested Amounts_ section, **test** that the output PDF files are accepted by the ANID application system, and only then start working in earnest.

I'm also afraid that I cannot promise to promptly (or ever) deal with bugs or technical questions that might arise.

## Repository contents

This repository contains LaTeX templates that mimic the English versions of the Microsoft Word forms that have to be filled as part of the application to the [ANID 2022 Fondecyt Regular National Competition](https://www.anid.cl/concursos/concurso/?id=603); namely:

* **Abstract:** [**abstract.tex**](abstract.tex) for [AbstractRegEng.docx](https://s3.amazonaws.com/documentos.anid.cl/fondecyt/2022/regular/AbstractRegEng.docx)
* **Proposed research:** [**prop.tex**](prop.tex) for  [ProposedResearchRegEng.docx](https://s3.amazonaws.com/documentos.anid.cl/fondecyt/2022/regular/ProposedResearchRegEng.docx)
* **Bibliographical references:** [**bib.tex**](bib.tex), which depends on the BibTeX file [**refs.bib**](refs.bib), for [BibliographicalReferencesRegEng.docx](https://s3.amazonaws.com/documentos.anid.cl/fondecyt/2022/regular/BibliographicalReferencesRegEng.docx),
* **Justification of requested amounts:** [**justification.tex**](justification.tex) for [JustificationRequestedAmountsRegEng.docx](https://s3.amazonaws.com/documentos.anid.cl/fondecyt/2022/regular/JustificationRequestedAmountsRegEng.docx)
* **Available resources:** [**resources.tex**](resources.tex) for [AvailableResourcesRegEng.docx](https://s3.amazonaws.com/documentos.anid.cl/fondecyt/2022/regular/AvailableResourcesRegEng.docx)

These LaTeX source files are all included in the container [**main.tex**](main.tex) LaTeX source code, where additional packages (`\usepackage`) and custom commands (`\newcommand`) should go.

The bash script [**compileAndSplit**](compileAndSplit) compiles the source code into a single PDF and calls [QPDF](http://qpdf.sourceforge.net/) to split it into five PDF files named `abstract.pdf`, `prop.pdf`, `bib.pdf`, `justification.pdf` and `resources.pdf` which, if everything goes well, can be uploaded to the ANID application system.
The script [**compileAndSplit**](compileAndSplit) admits an optional argument, which, if present, will be suffixed to the filenames of these five PDF files.

## How to obtain the files

Just clone this repository. Use the GitHub interface or, from the command line

```
git clone https://github.com/lfiguero/FondecyTeX.git
```
