# poi包

| Maven artifactId  | Prerequisites                         | JAR                                    |
| ----------------- | ------------------------------------- | -------------------------------------- |
| poi               | commons-logging, commons-codec, log4j | poi-version-yyyymmdd.jar               |
| poi-scratchpad    | poi                                   | poi-scratchpad-version-yyyymmdd.jar    |
| poi-ooxml         | poi, poi-ooxml-schemas                | poi-ooxml-version-yyyymmdd.jar         |
| poi-ooxml-schemas | xmlbeans                              | poi-ooxml-schemas-version-yyyymmdd.jar |
| poi-examples      | poi, poi-scratchpad, poi-ooxml        | poi-examples-version-yyyymmdd.jar      |
| ooxml-schemas     | xmlbeans                              | ooxml-schemas-1.1.jar                  |



# 包选择

| Component                                                 | Application     type | Maven artifactId                                       | Notes                                                        |
| --------------------------------------------------------- | -------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| [POIFS](http://poi.apache.org/poifs/index.html)           | OLE2 Filesystem      | *poi*                                                  | Required to work with OLE2 / POIFS based files               |
| [HPSF](http://poi.apache.org/hpsf/index.html)             | OLE2 Property Sets   | poi                                                    |                                                              |
| [HSSF](http://poi.apache.org/spreadsheet/index.html)      | Excel XLS            | poi                                                    | For HSSF only, if common SS is needed see below              |
| [HSLF](http://poi.apache.org/slideshow/index.html)        | PowerPoint PPT       | poi-scratchpad                                         |                                                              |
| [HWPF](http://poi.apache.org/document/index.html)         | Word DOC             | poi-scratchpad                                         |                                                              |
| [HDGF](http://poi.apache.org/hdgf/index.html)             | Visio VSD            | poi-scratchpad                                         |                                                              |
| [HPBF](http://poi.apache.org/hpbf/index.html)             | Publisher PUB        | poi-scratchpad                                         |                                                              |
| [HSMF](http://poi.apache.org/hsmf/index.html)             | Outlook MSG          | poi-scratchpad                                         |                                                              |
| [OpenXML4J](http://poi.apache.org/oxml4j/index.html)      | OOXML                | poi-ooxml plus one of poi-ooxml-schemas, ooxml-schemas | Only one schemas jar is needed, see below for differences    |
| [XSSF](http://poi.apache.org/spreadsheet/index.html)      | Excel XLSX           | poi-ooxml                                              |                                                              |
| [XSLF](http://poi.apache.org/slideshow/index.html)        | PowerPoint PPTX      | poi-ooxml                                              |                                                              |
| [XWPF](http://poi.apache.org/document/index.html)         | Word DOCX            | poi-ooxml                                              |                                                              |
| [Common SS](http://poi.apache.org/spreadsheet/index.html) | Excel XLS and XLSX   | poi-ooxml                                              | WorkbookFactory and friends all require poi-ooxml, not just core poi |