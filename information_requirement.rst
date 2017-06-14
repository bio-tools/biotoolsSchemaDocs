Information requirement
=======================

bio.tools information standard
------------------------------

**This is a work in progress.**  Please join the `discussion on GitHub <https://github.com/bio-tools/biotoolsSchema/issues/77>`_

biotoolsSchema provides the foundation for an *information standard* for the description of tools that is being adopted by https://bio.tools.  The standard has two components:

* a list of tool attributes that must be specified (or stated as not being available) for an entry to be labelled in a 5 tier rating of annotation quality
* a set of `Curation Guidelines <http://biotools.readthedocs.io/en/latest/curators_guide.html>`_ describing *how* each attribute should be specified, *i.e.* things that go beyond syntactic and semantic constraints defined by `biotoolsSchema <https://github.com/bio-tools/biotoolsSchema/>`_.  Some guidelines are checked by automated QC checks within bio.tools whereas others must be manually verified.  An entry in which all attributes pass the automated and manual checks can be labelled as "Verified" 



.. image:: information_standard.png

Attributes defined as mandatory in the latest stable schema (`biotools-2.0.0 <https://github.com/bio-tools/biotoolsSchema/tree/master/versions/biotools-2.0.0>`_) are those in the "OKAY" tier plus  "Scientific operation" from the "GOOD" tier.  NB: A persistent human readable URL e.g. https://bio.tools/tool/signalp is derived from the unique ID.

.. csv-table::
   :header: "Attribute", "Description", "Format", "element"
   :widths: 15, 75, 10, 10

   "**Name**", "Canonical software name assigned by the software developer or service provider", "Text", "``<name>``"
   "**Description**", "Short and concise textual description of the software function", "Text", "``<description>``"
   "**Homepage**", "Homepage of the software, or some URL that best serves this purpose", "URL", "``<homepage>``"
   "**Tool type**", "The type of application software: a discrete software entity can have more than one type.", "enum (from biotoolsSchema, see below)", "``<toolType>``"
   "**Unique ID**", "Unique ID of the tool that is assigned upon registration of the software in bio.tools", "Text (URL-safe version of tool name)", "``<toolID>``"
   "**Scientific topics**", "General scientific domain the software serves or other general category, *e.g.* 'Proteomics'", "Term and / or URI of `EDAM Topic <http://edamontology.org/topic_0004>`_ concept(s) (1)", "``<topic>``"
   "**Publications**", "Publications about the software", "DOI, PMID or PMCID", "``<publication>``"
   "**Contact information**", "Primary contact, *e.g.* a person, helpdesk or mailing list", "Email address and / or URL",  "``<contact>``"
   "**Scientific operations**", "The basic operation(s) performed by the software, *e.g.* 'Multiple sequence alignment'", "Term and / or URI of `EDAM Operation <http://edamontology.org/operation_0004>`_ concept(s)", "``<function><operation>``"
   "**General documentation**", "General documentation", "URL", "``<documentation><type>General</type>``"
   "**API documentation**", "Human-readable API documentation.", "URL", "``<documentation><type>API documentation</type>``"
   "**API specification**", "File providing an API specification for the software, e.g. Swagger/OpenAPI, WSDL or RAML file.", "URL", "``<download><type>API specification</type>``"
   "**Type of input & output data**", "Type of primary input / output data (if any), *e.g.* 'Protein sequences'", "Term and / or URI of `EDAM Data <http://edamontology.org/data_0006>`_ concept(s)", "``<function><input>/<output><data>``"
   "**Repository**", "Link to repository where source code, data and other files may be downloaded", "URL", "``<link><type>Repository</type>``"
   "**Source code**", "Software source code.", "URL", "``<download><type>Source code</type>``"
   "**License**", "Software or data usage license", "enum (from biotoolsSchema)", "``<labels><license>``"
   "**Terms of use**", "Rules that one must agree to abide by in order to use a service.", "URL", "``<link><type>Terms of use</type>``"
   "**Supported data formats**", "Allowed format(s) of primary inputs/outputs, *e.g.* 'FASTA'", "Term and / or URI of `EDAM Format <http://edamontology.org/format_1915>`_ concept(s)", "``<function><input>/<output><format>``"
   "**Helpdesk**", "Helpdesk providing support in using the software.", "URL", "``<link><type>Helpdesk</type>``"
   "**Issue tracker**", "Link to tracker for software issues, bug reports, feature requests etc.", "URL", "``<link><type>Issue tracker</type>``"
   "**Mailing list**", "Link to mailing list for software announcements, discussions, support etc.", "URL", "``<link><type>Mailing list</type>``"
   "**Operating system**", "The operating system supported by a downloadable software package.", "enum (from biotoolsSchema)", "``<labels><OperatingSystem>``"
   "**Language**", "Name of programming language the software source code was written in.", "enum (from biotoolsSchema)", "``<labels><Language>``"
   "**Cost**", "Monetary cost of acquiring the software.", "enum (from biotoolsSchema)", "``<labels><Cost>``"
   "**Accessibility**", "Whether the software is freely available for use.", "enum (from biotoolsSchema)", "``<labels><Accessibility>``"
   "**Maturity**", "How mature the software product is.", "enum (from biotoolsSchema)", "``<labels><Maturity>``"

   


  
.. note:: (1) EDAM is a simple ontology of well established, familiar concepts that are prevalent within bioinformatics, including types of data and data identifiers, data formats, operations and topics. EDAM provides a set of terms with synonyms and definitions - organised into an intuitive hierarchy for convenient use.  You can find `EDAM on GitHub <https://github.com/edamontology/edamontology>`_.

