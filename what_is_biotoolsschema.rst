What is biotoolsSchema?
=======================
**biotoolsSchema** is a formalised XML schema (XSD) which defines a description model for bioinformatics software.  It can be used to describe bioinformatics tools - application software with well-defined data processing functions (inputs, outputs and operations).   This includes simple tools with one or a few closely related functions, and complex, multimodal tools with many functions, tools available available for immediate use as online services, or in a form which which you can download, install, configure and run yourself.  

biotoolsSchema defines over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software.  It concentrates upon the salient common features, with a minimal core of 3 attributes only (name, short description and homepage), to provide maximum flexibility for applications.  To enable concise information, standard identifiers are used where possible, including ontology concept IDs for specialised scientific and technical aspects.  Verbose information are referred to by URL.

It is used by the ELIXIR Tools & Data Services Registry (`bio.tools <https://bio.tools>`_).

Documentation
-------------
Full documentation of biotoolsSchema is available at:

- `GitHub <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_ 

Version 2.0.0 is currently supported in `bio.tools <https://bio.tools>`_.  Support for version 3.0.0 is currently being rolled out in a staged manner (see `g-doc <https://docs.google.com/document/d/1tqw7FELV4F_qzrTA9KpVYoORAeFPyY1ZOjaGTPN2H1E/edit#heading=h.fffoc8urhpt8>`_).


Download
--------
Latest stable version

- https://github.com/bio-tools/biotoolsSchema/blob/master/stable/biotools.xsd

Current development version

- https://github.com/bio-tools/biotoolsSchema/blob/master/biotools_dev.xsd
  
Versioned releases

- https://github.com/bio-tools/biotoolsSchema/tree/master/versions


Status
------
biotoolsSchema is a mature schema having undergone a lot of community-driven revision (e.g. see `bio.tools events <http://biotools.readthedocs.io/en/latest/events.html>`_).  Development is use-case driven, primarily by `bio.tools <https://bio.tools>`_.  Future versions will not depart fundamentally from the current elements or structure.  The development of biotoolsSchema can be followed at `GitHub <https://github.com/bio-tools/biotoolsschema/>`_.  From version 2.0.0, version number follow the `MAJOR.MINOR.PATCH` pattern:

* `MAJOR` version for incompatible API changes
* `MINOR` version for addition of functionality in a backwards-compatible manner
* `PATCH` version for backwards-compatible bug fixes

For ways to contribute, please see the `Contributors Guide <http://biotools.readthedocs.org/en/latest/contributors_guide.html>`_. 

Motivation
----------
Bioinformaticians routinely use a large and diverse set of tools and data, and demand powerful and convenient means to organise, find, understand, compare, select, use and connect the available resources. These tasks rely on consistent, machine-understandable resource descriptions. The need - filled by biotoolsSchema - is for an information model that puts the description of a broad range of resources  on a consistent syntactic basis. 

Citing biotoolsSchema
---------------------
If you use biotoolsSchema, please cite:

Ison, J. et al. (2016). Tools and data services registry: a community effort to document bioinformatics resources. *Nucleic Acids Research*, **44** (D1): D38-D47.

The article is `freely available <http://nar.oxfordjournals.org/content/44/D1/D38>`_.

doi: `10.1093/nar/gkv1116 <http://doi.org/10.1093/nar/gkv1116>`_ 


