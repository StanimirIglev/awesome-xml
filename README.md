# Awesome XML [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of the best tools, libraries, tutorials, and more for all things XML-related.

## Contents

- [The XML Family (in a nutshell)](#the-xml-family-in-a-nutshell)
- [Drafts and Community Advances](#drafts-and-community-advances)
- [Processing Libraries](#processing-libraries)
- [Command-Line Tools](#command-line-tools)
- [Online Tools](#online-tools)
- [Validation](#validation)
  - [Schema Languages](#schema-languages)
- [Native XML Databases](#native-xml-databases)
- [XML-based Formats/Languages](#xml-based-formatslanguages)
- [Community](#community)
  - [Websites/Forums](#websitesforums)
  - [Conferences](#conferences)
  - [Blogs](#blogs)
  - [Mailing Lists](#mailing-lists)
  - [Articles](#articles)
- [Tutorials](#tutorials)
- [Books](#books)
- [VS Code Extensions](#visual-studio-code-extensions)
- [Editors (validating)](#editors-validating)
- [Browser Extensions](#browser-extensions)
  - [Mozilla Firefox](#mozilla-firefox)
  - [Google Chrome](#google-chrome)
- [Contribute](#contribute)

## The XML Family (in a nutshell)

A list of W3C standards closely related to XML.

- Extensible Markup Language (XML) Specifications - [XML 1.0](https://www.w3.org/TR/xml/), [XML 1.1](https://www.w3.org/TR/xml11/)
  - [Annotated specification](https://www.xml.com/axml/testaxml.htm) by Tim Bray.
- Namespaces in XML - [Namespaces in XML 1.0](https://www.w3.org/TR/REC-xml-names/), [Namespaces in XML 1.1](https://www.w3.org/TR/xml-names11/)
- [XML Information Set](https://www.w3.org/TR/xml-infoset/) - an abstract data model for XML documents.
- [Extensible Stylesheet Language (XSL)](https://www.w3.org/TR/xsl/) - a family of languages used for transforming and presenting XML documents.
  - [XSL-FO (Formatting Objects)](https://www.w3.org/TR/xsl11/#fo-section) - presentation layer for ormatting XML data for output to screen, paper, or other media.
  - [XSLT](https://www.w3.org/TR/xslt/) - a language for transforming XML documents into other XML documents, HTML, text, or other formats.
  - [XML Path Language (XPath)](https://www.w3.org/TR/xpath/) - a language used for navigating and selecting nodes in an XML document.
- XML Validation:
  - [Document Type Definition (DTD)](https://www.w3.org/TR/xml/#dt-doctype) - a set of rules that define the legal building blocks of an XML document.
  - [W3C XML Schema Definitions (XSD)](https://www.w3.org/XML/Schema) - a language for describing the structure and content of XML documents.
- Standard Attributes:
  - [XML ID](https://www.w3.org/TR/xml-id/) - a unique identifier for an element within a document.
  - [XML Base](https://www.w3.org/TR/xmlbase/) - a base URI for resolving relative URIs within a document.
- Linking XML resources:
  - [XML Inclusions (XInclude)](https://www.w3.org/TR/xinclude/) - a standard for merging XML documents via inclusion.
  - [XML Pointer Language (XPointer)](https://www.w3.org/TR/xptr/) - a language for addressing and referencing specific parts of a document.
  - [XML Linking Language (XLink)](https://www.w3.org/TR/xlink/) - a language for creating hyperlinks within documents.
- [XForms](https://www.w3.org/TR/xforms/) - a standard for creating web forms.
- [XML Signature](https://www.w3.org/TR/xmldsig-core1/) - a standard for digital signatures.
- [XML Encryption](https://www.w3.org/TR/xmlenc-core1/) - a standard for encrypting XML data.
- [XML Key Management Specification (XKMS)](https://www.w3.org/TR/xkms2/) - a protocol for managing cryptographic keys within XML applications.
- [XQuery](https://www.w3.org/XML/Query/) - a language for querying XML data.
- [XProc](https://www.w3.org/TR/xproc/) - a language for defining XML processing pipelines.

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Drafts and Community Advances

A collection of actively developed drafts and community-driven XML-related projects.

- [MicroXML](https://dvcs.w3.org/hg/microxml/raw-file/tip/spec/microxml.html)
  - [Community Group](https://www.w3.org/community/microxml/)
- [Invisible XML](https://invisiblexml.org/current/)
  - [Community Group](https://www.w3.org/community/ixml/), [GitHub](https://github.com/invisibleXML/)
- [QT4 (XQuery and XSLT extensions)](https://qt4cg.org/)
  - [Community Group](https://www.w3.org/community/xslt-40/), [GitHub](https://github.com/qt4cg/)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Processing Libraries

### Legend for Use Case Tags

| Tag               | Description                                                                                                                        |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **DOM**           | Libraries that support building or navigating XML trees via the Document Object Model.                                             |
| **SAX**           | Libraries that use event-driven parsing, emitting parsing events (start tag, end tag, etc.) instead of building an in-memory tree. |
| **Validation**    | Support for XML schema validation (DTD, XSD, Relax NG, etc.).                                                                      |
| **XPath**         | Libraries that support querying XML documents using XPath expressions.                                                             |
| **XSLT**          | Libraries with support for XML transformation using XSLT stylesheets.                                                              |
| **Serialization** | Libraries that convert between native data structures and XML (marshal/unmarshal).                                                 |

💡 Use these tags to quickly identify what capabilities each library provides. 💡

### Libraries

| Library Name                                                                          | Language   | Use Cases                                        | Notes                                                                    |
| ------------------------------------------------------------------------------------- | ---------- | ------------------------------------------------ | ------------------------------------------------------------------------ |
| [libxml2](http://xmlsoft.org/)                                                        | C          | DOM, SAX, Validation, XPath, XSLT                | Comprehensive XML toolkit with support for various standards.            |
| [expat](https://libexpat.github.io/)                                                  | C          | SAX                                              | Stream-oriented parser suitable for event-driven applications.           |
| [libxml++](https://libxmlplusplus.github.io/libxmlplusplus/)                          | C++        | DOM, SAX, Validation, XPath, XSLT                | C++ wrapper for libxml2 providing an object-oriented API.                |
| [pugixml](https://pugixml.org/)                                                       | C++        | DOM, XPath                                       | Lightweight and fast XML parser with XPath support.                      |
| [TinyXML](https://github.com/leethomason/tinyxml2)                                    | C++        | DOM                                              | Simple and small XML parser for C++ applications.                        |
| [RapidXML](https://rapidxml.sourceforge.net/)                                         | C++        | DOM                                              | High-performance XML parser with in-situ parsing capabilities.           |
| [Xerces-C++](https://xerces.apache.org/xerces-c/)                                     | C++        | DOM, SAX, Validation                             | Full-featured XML parser with support for various XML standards.         |
| [System.Xml](https://docs.microsoft.com/en-us/dotnet/api/system.xml?view=net-5.0)     | C#         | DOM, SAX, Validation, XPath, XSLT, Serialization | .NET's comprehensive XML processing library.                             |
| [Dart XML](https://pub.dev/packages/xml)                                              | Dart       | DOM                                              | Lightweight library for parsing and building XML documents.              |
| [encoding/xml](https://pkg.go.dev/encoding/xml)                                       | Go         | Serialization                                    | Standard library for encoding and decoding XML.                          |
| [xml-conduit](https://hackage.haskell.org/package/xml-conduit)                        | Haskell    | DOM, Streaming                                   | Provides parsing and rendering functions for XML with streaming support. |
| [Haskell XML Toolbox](https://intern.fh-wedel.de/~si/HXmlToolbox/index.html)          | Haskell    | DOM, Validation, XPath                           | Collection of tools for processing XML with Haskell.                     |
| [JAXP](https://docs.oracle.com/javase/8/docs/technotes/guides/xml/jaxp/index.html)    | Java       | DOM, SAX, Validation, XPath, XSLT                | Java API for XML Processing supporting various standards.                |
| [dom4j](https://dom4j.github.io/)                                                     | Java       | DOM, XPath                                       | Flexible XML framework for Java applications.                            |
| [JDOM](http://www.jdom.org/)                                                          | Java       | DOM                                              | Java-based document object model for XML that is easy to use.            |
| [VTD-XML](https://vtd-xml.sourceforge.io/)                                            | Java       | DOM, XPath                                       | High-performance XML parser with non-extractive parsing.                 |
| [Xerces2-J](https://xerces.apache.org/xerces2-j/)                                     | Java       | DOM, SAX, Validation                             | Java version of Xerces with comprehensive XML support.                   |
| [DOMParser](https://developer.mozilla.org/en-US/docs/Web/API/DOMParser)               | JavaScript | DOM                                              | Built-in browser API for parsing XML documents.                          |
| [xml-js](https://www.npmjs.com/package/xml-js)                                        | JavaScript | DOM                                              | Converts XML text to JavaScript objects and vice versa.                  |
| [xml2js](https://www.npmjs.com/package/xml2js)                                        | JavaScript | DOM                                              | Simple XML to JavaScript object converter.                               |
| [fast-xml-parser](https://www.npmjs.com/package/fast-xml-parser)                      | JavaScript | DOM                                              | Fast and lightweight XML parser for JavaScript.                          |
| [XmlUtil](https://github.com/pdvrieze/xmlutil)                                        | Kotlin     | DOM                                              | Utility functions for XML processing in Kotlin.                          |
| [XML::Parser](https://metacpan.org/pod/XML::Parser)                                   | Perl       | SAX                                              | Perl module for parsing XML documents.                                   |
| [XML::LibXML](https://metacpan.org/pod/XML::LibXML)                                   | Perl       | DOM, XPath, Validation                           | Interface to the libxml2 library for Perl.                               |
| [XML::Simple](https://metacpan.org/pod/XML::Simple)                                   | Perl       | DOM                                              | Simple API for reading and writing XML.                                  |
| [SimpleXML](https://www.php.net/manual/en/book.simplexml.php)                         | PHP        | DOM                                              | Provides a simple way to access XML elements.                            |
| [xml.etree.ElementTree](https://docs.python.org/3/library/xml.etree.elementtree.html) | Python     | DOM                                              | Lightweight XML parser and tree builder.                                 |
| [lxml](https://lxml.de/)                                                              | Python     | DOM, XPath, XSLT, Validation                     | Powerful and feature-rich XML processing library.                        |
| [xml.dom.minidom](https://docs.python.org/3/library/xml.dom.minidom.html)             | Python     | DOM                                              | Minimal implementation of the Document Object Model interface.           |
| [NokoGiri](https://nokogiri.org/)                                                     | Ruby       | DOM, XPath, XSLT                                 | HTML, XML, SAX, and Reader parser with XPath and CSS selector support.   |
| [REXML](https://ruby.github.io/rexml/)                                                | Ruby       | DOM                                              | Pure Ruby XML processor conforming to the XML 1.0 specification.         |
| [xml-rs](https://crates.io/crates/xml-rs)                                             | Rust       | SAX                                              | Event-based XML parser for Rust.                                         |
| [quick-xml](https://crates.io/crates/quick-xml)                                       | Rust       | SAX                                              | Fast and low-level XML reader and writer.                                |
| [scala-xml](https://github.com/scala/scala-xml)                                       | Scala      | DOM                                              | XML processing library for Scala.                                        |
| [SWXMLHash](https://github.com/drmohundro/SWXMLHash)                                  | Swift      | DOM                                              | Simple XML parser for Swift.                                             |
| [AEXML](https://github.com/tadija/AEXML)                                              | Swift      | DOM                                              | Lightweight XML parser for iOS and macOS.                                |

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Command-Line Tools

A collection of command-line tools for XML processing.

- [xmllint](http://xmlsoft.org/xmllint.html) - a multifaceted XML tool that comes with libxml2.
- [xmlstarlet](http://xmlstar.sourceforge.net/) - a set of utilities for querying, editing, validating, and transforming XML documents.
- [xq](https://github.com/sibprogrammer/xq) - beautifier and content extractor.
- [dasel](https://github.com/TomWright/dasel) - query and modify data structures using standart selector strings. Supports XML among others.
- [graphtage](https://github.com/trailofbits/graphtage) - semantically compare and merge tree-like structures.
- [HTML-XML-utils](https://www.w3.org/Tools/HTML-XML-utils/) - a collection of utilities for XML/HTML manipulation.
- [Saxon](https://www.saxonica.com/welcome/welcome.xml) - XML processor supporting XSLT 3.0, XQuery 3.1, XPath 3.1, and XSD 1.1. (Note: **only the HE version is free**.)
- [tidy (libtidy)](http://www.html-tidy.org/) - correct and clean-up HTML and XML documents.
- [xsltproc (libxslt)](https://gitlab.gnome.org/GNOME/libxslt/-/wikis/home) - XSLT processor for the application of stylesheets to XML documents.

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Online Tools

A small excerpt of the many online tools for XML processing.

- FreeFormatter XML Tools - [Formatter](https://www.freeformatter.com/xml-formatter.html), [Validator](https://www.freeformatter.com/xml-validator-xsd.html), [XSD Generator](https://www.freeformatter.com/xsd-generator.html), [XML-to-JSON](https://www.freeformatter.com/xml-to-json-converter.html), [XSL Transformer](https://www.freeformatter.com/xsl-transformer.html), [XML Escape](https://www.freeformatter.com/xml-escape.html)
- JSON Formatter XML Tools - [Formatter](https://jsonformatter.org/xml-formatter), [Minify](https://jsonformatter.org/xml-minify), [Viewer](https://jsonformatter.org/xml-viewer), [XML Pretty Print](https://jsonformatter.org/xml-pretty-print), [Validator](https://jsonformatter.org/xml-validator), [Editor](https://jsonformatter.org/xml-editor), [Parser](https://jsonformatter.org/xml-parser)
- Code Beautify XML Tools - [Coverter](https://codebeautify.org/xml-converter-online), [Generator](https://codebeautify.org/generate-random-xml), [Difftool](https://codebeautify.org/xml-diff), [Minify](https://codebeautify.org/xml-minifier), [Editor](https://codebeautify.org/online-xml-editor), [Parser](https://codebeautify.org/xml-parser-online), [Validator](https://codebeautify.org/xmlvalidator), [Viewer](https://codebeautify.org/xmlviewer)
- ExtendsClass XML Tools - [Difftool](https://extendsclass.com/xml-diff.html), [Formatter](https://extendsclass.com/xml-formatter-online.html), [Generator](https://extendsclass.com/xml-generator.html), [Validator](https://extendsclass.com/xml-validator.html), [XSD Generator](https://extendsclass.com/xml-schema-validator.html)
- XMLable XML Tools - [Formatter](https://xmlable.com/formatter/), [Validator](https://xmlable.com/validator/), [XSD Generator](https://xmlable.com/xml-to-xsd/), [XPath tester](https://xmlable.com/xpath/), [Difftool](https://xmlable.com/compare/), [Generator](https://xmlable.com/generator/), [XSL Transformation](https://xmlable.com/xslt/)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Validation

### Schema Languages

- [Document Type Definition (DTD)](https://www.w3.org/TR/xml/#dt-doctype)
  - Part of the original XML 1.0 specification.
  - Additional resources: [Wiki](https://en.wikipedia.org/wiki/Document_Type_Definition), [Tutorial](https://www.w3schools.com/xml/xml_dtd_intro.asp)
- [W3C XML Schema Definitions (XSD)](https://www.w3.org/XML/Schema) - [Primer](https://www.w3.org/TR/xmlschema-0/), [Part 1](https://www.w3.org/TR/xmlschema11-1/), [Part 2](https://www.w3.org/TR/xmlschema11-2/)
  - W3C Recommendation.
  - Additional resources: [Wiki](<https://en.wikipedia.org/wiki/XML_Schema_(W3C)>), [Tutorial](https://www.w3schools.com/xml/schema_intro.asp)
- [Relax NG](https://relaxng.org)
  - Part of DSDL - the [ISO/IEC 19757-2 standard](https://www.iso.org/standard/52348.html).
  - Additional resources: [Wiki](https://en.wikipedia.org/wiki/Relax_NG), [Tutorial](https://relaxng.org/tutorial-20011203.html)
- [Schematron](http://www.schematron.com)
  - Part of DSDL - the [ISO/IEC 19757-3 standard](https://www.iso.org/standard/74515.html).
  - Additional resources: [Wiki](https://en.wikipedia.org/wiki/Schematron), [Tutorial](https://www.xml.com/pub/a/2003/11/12/schematron.html)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Native XML Databases

A list of XML databases that store and query XML data natively.

- [BaseX](http://basex.org/)
  - [Wiki](https://en.wikipedia.org/wiki/BaseX), [Documentation](http://docs.basex.org/), [GitHub](https://github.com/BaseXdb/basex)
- [Berkeley DB XML](https://www.oracle.com/database/technologies/related/berkeleydb.html)
  - [Wiki](https://en.wikipedia.org/wiki/Berkeley_DB_XML), [Documentation](https://docs.oracle.com/cd/E17276_01/html/index.html), [GitHub](https://github.com/berkeleydb/dbxml)
- [eXist-db](https://exist-db.org/)
  - [Wiki](https://en.wikipedia.org/wiki/EXist), [Documentation](https://exist-db.org/exist/apps/doc/), [GitHub](https://github.com/exist-db/exist/)
- [MonetDB](https://www.monetdb.org/)
  - [Wiki](https://en.wikipedia.org/wiki/MonetDB), [Documentation](https://www.monetdb.org/documentation-Dec2023/), [Repository](https://www.monetdb.org/hg/MonetDB/file/)
- [Sedna](https://www.sedna.org/)
  - [Wiki](<https://en.wikipedia.org/wiki/Sedna_(database)>), [Documentation](https://www.sedna.org/documentation.html), [GitHub](https://github.com/sedna/sedna)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## XML-based Formats/Languages

A curated list of popular formats and languages that use the XML syntax (often defined via a schema).
A more extensive, but less curated list can be found [here](https://en.wikipedia.org/wiki/List_of_XML_markup_languages).

❗ The goal for this section is to have a list of established formats with links to resources, such as specifications, schemas, and tutorials. Feel free to contribute! ❗

- [Analytical Information Markup Language(AnIML)](https://www.animl.org/) - XML standard for analytical chemistry and biological data.
  - [XSD Schemas](https://www.animl.org/current-schema), [GitHub](https://github.com/AnIML)
- [Atom](https://tools.ietf.org/html/rfc4287) - a web feed format.
  - [Wiki](<https://en.wikipedia.org/wiki/Atom_(Web_standard)>), [Tutorial](https://validator.w3.org/feed/docs/atom.html)
- [CDF Markup Language (CDFML)](https://cdf.gsfc.nasa.gov/html/faq.html)
  - [XSD](https://spdf.gsfc.nasa.gov/pub/software/cdf/dist/latest/linux/cdf.xsd)
- [CellML](https://www.cellml.org/) - a language for describing mathematical models.
  - [Wiki](https://en.wikipedia.org/wiki/CellML), [Tutorials](https://www.cellml.org/getting-started/tutorials), [XSD](https://www.cellml.org/tools/cellml_1_1_schema)
- [Chemical Markup Language (CML)](https://www.xml-cml.org/)
  - [Wiki](https://en.wikipedia.org/wiki/Chemical_Markup_Language), [Schemas](https://www.xml-cml.org/schema/)
- [Darwin Information Typing Architecture (DITA)](http://dita.xml.org/)
  - [Wiki](https://en.wikipedia.org/wiki/Darwin_Information_Typing_Architecture), [Schemas](https://docs.oasis-open.org/dita/), [GitHub](https://github.com/oasis-tcs/dita)
- [DocBook](https://docbook.org/) - a semantic markup language for technical documentation.
  - [Wiki](https://en.wikipedia.org/wiki/DocBook), [Schemas](https://docbook.org/schemas/)
- [Digital Weather Markup Language (DWML)](https://docs.safe.com/fme/html/FME-Form-Documentation/FME-ReadersWriters/dwml/dwml.htm)
  - [XSD](https://schemas.liquid-technologies.com/DWML/0/)
- [Electronic Business using eXtensible Markup Language (ebXML)](https://www.ebxml.org/) - a set of specifications for electronic business.
  - [Wiki](https://en.wikipedia.org/wiki/EbXML)
- [Encoded Archival Description (EAD)](https://www.loc.gov/ead/) - astandard for encoding archival finding aids.
  - [Wiki](https://en.wikipedia.org/wiki/Encoded_Archival_Description), [A Primer (Video)](https://www.youtube.com/watch?v=WYWQeBRnhz0),[EAD3 Schemas](https://loc.gov/ead/ead3schema.html), [EAD 2002 Schemas](https://loc.gov/ead/eadschema.html)
- [FictionBook](https://en.wikipedia.org/wiki/FictionBook) - an e-book format.
  - [Wiki](https://en.wikipedia.org/wiki/FictionBook), [XSD](http://www.fictionbook.org/index.php/Eng:XML_Schema_Fictionbook_2.1)
- [Geography Markup Language (GML)](https://www.ogc.org/standard/gml/) - a language for expressing geographical features.
  - [Wiki](https://en.wikipedia.org/wiki/Geography_Markup_Language), [Schemas](https://schemas.opengis.net/gml/)
- [GraphML](http://graphml.graphdrawing.org/index.html) - format for describing graphs.
  - [Wiki](https://en.wikipedia.org/wiki/GraphML), [XSD](http://graphml.graphdrawing.org/specification/schema_element.xsd.htm)
- [MathML](https://www.w3.org/Math/) - a language for describing mathematical notation.
  - [Wiki](https://en.wikipedia.org/wiki/MathML), [Tutorial](https://www.tutorialspoint.com/mathml/index.htm), [Schemas](https://www.w3.org/Math/XMLSchema/)
- [Metadata Object Description Schema (MODS)](https://www.loc.gov/standards/mods/)
  - [Wiki](https://en.wikipedia.org/wiki/Metadata_Object_Description_Schema), [Schemas](https://www.loc.gov/standards/mods/mods-schemas.html)
- [News Industry Text Format (NITF)](https://iptc.org/standards/nitf/) - a standard for news content.
  - [Wiki](https://en.wikipedia.org/wiki/News_Industry_Text_Format), [NITF 3.6 XSD](https://www.iptc.org/std/NITF/3.6/specification/nitf-3-6.xsd) (other versions available [here](https://iptc.org/standards/nitf/))
- [Outline Processor Markup Language (OPML)](http://opml.org/) - a format for outlines.
  - [Wiki](https://en.wikipedia.org/wiki/OPML), [Unofficial XSD](https://github.com/eclipse-archived/buckminster/blob/master/org.eclipse.buckminster.opml/src/opml-2.0.xsd)
- [PhyloXML](http://phyloxml.org/) - a language for describing phylogenetic trees (or networks) and associated data.
  - [Wiki](https://en.wikipedia.org/wiki/PhyloXML), [XSD](http://www.phyloxml.org/1.20/phyloxml.xsd)
- [RSS](https://www.rssboard.org/rss-specification) - a web feed format.
  - [Wiki](https://en.wikipedia.org/wiki/RSS), [Tutorial](https://www.w3schools.com/xml/xml_rss.asp), [XSD](https://schemas.liquid-technologies.com/w3c/rss/2.0.1.9/?page=rss-2_0_1-rev9_xsd.html)
- [Scalable Vector Graphics (SVG)](https://www.w3.org/Graphics/SVG/)
  - [Wiki](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics), [MDN Tutorial](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial), [W3Schools Tutorial](https://www.w3schools.com/graphics/svg_intro.asp), [Awesome SVG](https://github.com/willianjusten/awesome-svg)
- [Extensible HyperText Markup Language (XHTML)](https://html.spec.whatwg.org/) - a reformulation of HTML.
  - [Wiki](https://en.wikipedia.org/wiki/XHTML), [Tutorial](https://www.tutorialspoint.com/xhtml/index.htm)
- [XSpec](https://xspec.io/) - a unit test and behaviour-driven development (BDD) framework for XSLT, XQuery, and Schematron.
  - [Wiki](https://github.com/xspec/xspec/wiki)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Community

### Websites/Forums

- [XML.com](https://www.xml.com) - a site for XML resources, tutorials, and news.
- [XML.org](https://www.xml.org) - a community-driven site for XML resources.
- [r/xml](https://www.reddit.com/r/xml/) - a subreddit for XML discussions.
- [XML @ Stack Overflow](https://stackoverflow.com/questions/tagged/xml) - XML-related discussions on Stack Overflow.

### Conferences

- [XML Prague](https://www.xmlprague.cz/) - an annual conference on markup languages and data on the web.
- [Balisage](https://www.balisage.net/) - an annual conference devoted to descriptive markup
- [Markup UK](https://markupuk.org/) - a conference about XML and other markup technologies
- [Declarative Amsterdam](https://declarative.amsterdam/) - a conference on the technologies and methods used for declarative programming and data
- [XML Summer School](https://xmlsummerschool.org/) - a week-long event comprised of courses for XML and related technologies

### Blogs

- [Michael Kay's Blog / Saxon Diaries](https://blog.saxonica.com/mike/)
- [DeltaBlog - DeltaXML](https://www.deltaxml.com/blog/)
- [XML Aficionado](https://xmlaficionado.com/)
- [XML Press Blog](https://xmlpress.net/xml-press-blog/)
- [Oxygen XML Blog](https://blog.oxygenxml.com/)
- [Altova's Blog](https://www.altova.com/blog/)
- [Inera's Blog](https://inera.com/blog/)

### Mailing Lists

- [XSL-List](https://www.mulberrytech.com/xsl/xsl-list/index.html) - mailing list for XSLT questions and applications.
- [Schematron](http://schematronist.org/mailman/listinfo/schematron_schematronist.org) - mailing list for Schematron discussions.
- [XML-DEV](https://www.xml.org/xml-dev) - active mailing list on XML.org.

### Articles

- [In defense of XML](https://blog.frankel.ch/defense-xml/) by Nicolas Fränkel.

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Tutorials

A list of tutorials that provide a good introduction to the XML ecosystem.

- [W3Schools XML Tutorial](https://www.w3schools.com/xml/) - covers XML, XPath, XSLT, XQuery, DTD, XSD, AJAX, DOM, and several XML-based web services.
- [Tutorials Point XML Tutorial](https://www.tutorialspoint.com/xml/index.htm) - beginners intro to XML and related technologies.
- [Javatpoint XML Tutorial](https://www.javatpoint.com/xml-tutorial) - covers XML, XML validation, XPath, XQuery, and XSLT.
- [XMLFiles Tutorials and Guides](https://www.xmlfiles.com/) - covers basics, XSL, DTD, DOM, RSS feeds, SEO, XBRL, XHTML, and other awesome articles.

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Books

Note that many of these books are available online for free - a quick Google search should suffice. 😉

- [XML: Visual QuickStart Guide](https://www.goodreads.com/book/show/3339815-xml) by Kevin Howard Goldberg
- [Learning XML](https://www.goodreads.com/book/show/231160.Learning_XML) by Erik Ray
- [XML in a Nutshell](https://www.goodreads.com/book/show/231158.XML_in_a_Nutshell) by Elliotte Rusty Harold, W. Scott Means
- [An Introduction to XML and Web Technologies](https://www.goodreads.com/book/show/922023.An_Introduction_to_XML_and_Web_Technologies) by Anders Møller, Michael I. Schwartzbach
- [XML for Dummies](https://www.goodreads.com/book/show/1727076.XML_For_Dummies) - Ed Tittel, Frank Boumphrey, Lucinda Dykes
- [Beginning XML](https://www.goodreads.com/book/show/13319079-beginning-xml) - Joe Fawcett, Danny Ayers, Liam R. E. Quin
- [Sams Teach Yourself XML in 24 Hours](https://www.goodreads.com/book/show/831166) by Michael Morrison
- [Professional XML](https://www.goodreads.com/book/show/684553.Professional_XML) - Didier Martin, Michael Kay, Stephen F. Mohr

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Visual Studio Code Extensions

- [XML (Red Hat)](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml) - support for creating and editing documents, based on the [LemMinX XML Server](https://github.com/eclipse/lemminx)
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) - Auto rename paired HTML/XML tags
- [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag) - Automatically add HTML/XML close tag
- [XML Tools](https://marketplace.visualstudio.com/items?itemName=DotJoshJohnson.xml) - XML Formatting, XQuery, and XPath Tools for Visual Studio Code
- [C# XML Documentation Comments](https://marketplace.visualstudio.com/items?itemName=k--kato.docomment) - Generate XML documentation comments
- [SVG Preview](https://marketplace.visualstudio.com/items?itemName=SimonSiefke.svg-preview) - Live preview of SVG files
- [Pretty XML](https://marketplace.visualstudio.com/items?itemName=PrateekMahendrakar.prettyxml) - XML formatter
- [XML Toolkit](https://marketplace.visualstudio.com/items?itemName=SAPOSS.xml-toolkit) - Syntax and well-formedness validation

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Editors (validating)

These are standalone XML editors with the inherent capability to validate XML against a DTD or schema.
Browser-based XML editors (such as under [Browser Extensions](#browser-extensions)) and general text editors like Notepad++ and Vim are not included.

### Free

- [XML Copy Editor](https://xml-copy-editor.sourceforge.io/) - GPLv2 license.
- [XML Notepad](https://microsoft.github.io/XmlNotepad/#) - MIT license.
- [XMLPad](https://www.softpedia.com/get/Programming/File-Editors/XMLPad.shtml)

### Commercial, but with a free for personal use version

- [Liquid Studio XML Editor](https://www.liquid-technologies.com/xml-editor)
- [XMLmind XML Editor](https://www.xmlmind.com/xmleditor/)

### Commercial

- [Adobe Framemaker](https://www.adobe.com/products/framemaker.html)
- [Oxygen XML Editor](https://www.oxygenxml.com/)
- [Stylus Studio](https://www.stylusstudio.com/xml/editor/)
- [XML ValidatorBuddy](https://www.xml-buddy.com/)
- [XML Spy](https://www.altova.com/xmlspy-xml-editor)
- [XMetal Author](https://xmetal.com/content-xmetal-author/)

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Browser Extensions

### Mozilla Firefox

- [XML Viewer Plus](https://addons.mozilla.org/en-US/firefox/addon/xml-viewer/)
- [Pretty XML](https://addons.mozilla.org/en-US/firefox/addon/pretty-xml/)

### Google Chrome

- [XML Tree](https://chrome.google.com/webstore/detail/xml-tree/gbammbheopgpmaagmckhpjbfgdfkpadb) - Displays XML data in a user friendly way.
- [XML Plus](https://chromewebstore.google.com/detail/xml-plus/jmhicemblbmkcbonbhkjmflehkmkiidj) - XML Viewer
- [XML Formatter](https://chromewebstore.google.com/detail/xml-formatter/ejmpbcebpllmffkidemmlecpgboklcme) - in-browser formatter for XML
- [XML Editor](https://chromewebstore.google.com/detail/xml-editor/offpnjldifddbopdmimolhcjniloicin) - XML code editor and validator
- [Night XML](https://chromewebstore.google.com/detail/night-xml-dark-mode-xml-v/dbbcealbkponjcfeafmabmjjkffclpgf) - dark mode XML viewer
- [XML Tools](https://chromewebstore.google.com/detail/xml-tools/pjlccigfdcjmbgbmaidfgmchilpfomam) - collection of tools for XML - conversion, formatting, minification, etc.
- [XML Formatter](https://chromewebstore.google.com/detail/xml-formatter/piocgilonokogjhfcillbljpifenhabk) - another XML formatter

<p align="right"><a href="#contents"><b>↥ back to top ↥</b></a></p>

## Contribute

Contributions are welcome! Read the [contribution guidelines](CONTRIBUTING.md) first.
