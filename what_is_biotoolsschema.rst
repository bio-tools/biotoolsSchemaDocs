What is biotoolsSchema?
=======================
**biotoolsSchema** is a formalised XML schema (XSD) which defines a description model for bioinformatics software.  It can be used to describe bioinformatics tools - application software with well-defined data processing functions (inputs, outputs and operations).   This includes simple tools with one or a few closely related functions, and complex, multimodal tools with many functions, tools available available for immediate use as online services, or in a form which which you can download, install, configure and run yourself.  

biotoolsSchema defines 50 important scientific, technical and administrative attributes.  It concentrates upon the salient common features, with a minimal core of 7 attributes, mandating the necessary and sufficient information to support cataloguing and discovery of software.  It is used by the ELIXIR Tools & Data Services Registry (`bio.tools <https://bio.tools>`_).

Documentation
-------------
Full documentation of biotoolsSchema is available at:

- https://bio.tools/schema  (version 1.4, currently in production in bio.tools)
- `GitHub <https://github.com/bio-tools/biotoolsSchema/blob/master/versions/biotools-2.0.0/docs/biotools-2.0.0.html>`_ (version 2.0.0, latest stable version)


Download
--------
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
-----------
If you use biotoolsSchema, please cite:

Ison, J. et al. (2016). Tools and data services registry: a community effort to document bioinformatics resources. *Nucleic Acids Research*, **44** (D1): D38-D47.

The article is `freely available <http://nar.oxfordjournals.org/content/44/D1/D38>`_.

doi: `10.1093/nar/gkv1116 <http://doi.org/10.1093/nar/gkv1116>`_ 


