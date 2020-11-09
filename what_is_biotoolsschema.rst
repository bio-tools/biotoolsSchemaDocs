What is biotoolsSchema?
=======================

**biotoolsSchema** is a formalised XML schema (XSD) which defines a description model for bioinformatics software.  It can be used to describe bioinformatics tools - application software with well-defined data processing functions (inputs, outputs and operations).   This includes simple tools with one or a few closely related functions, and complex, multimodal tools with many functions, tools available available for immediate use as online services, or in a form which which you can download, install, configure and run yourself.  

biotoolsSchema defines over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software.  It concentrates upon the salient common features, with a minimal core of 3 attributes only (name, short description and homepage), to provide maximum flexibility for applications.  To enable concise information, standard identifiers are used where possible, including `EDAM ontology <http://github.com/edamontology/edamontology>`_ concept IDs for specialised scientific aspects.  biotoolsSchema defines 18 controlled vocabularies for technical tool aspects.  Verbose information is referred to by URL.

biotoolsSchema together with the `EDAM ontology <https://github.com/edamontology/edamontology>`_ provide the foundation for an `information standard <https://github.com/bio-tools/Tool-Information-Standard>`_ for the description of tools.  This standard is being adopted by bio.tools and defines the attributes that must be defined within a 5-tier scale of entry completeness and quality.

biotoolsSchema is used by the ELIXIR Tools & Data Services Registry (`bio.tools <https://bio.tools>`_).


How to contribute to biotoolsSchema
-----------------------------------

Contributions to biotoolsSchema are very welcome. Github being our primary communication channel, please do not hesitate to open issues, or comment on them. Pull requests are also welcome! 
The list of repositories hosting biotoolsSchema and its documentation are listed below. All materials are available under the :doc:`CC-BY-SA 4.0 license<license>`_.

Documentation
-------------
These docs describe the latest stable version (currently 3.0.0) and are maintained in `GitHub <https://github.com/bio-tools/biotoolsschemadocs/>`_.  Additional documentation is available:

- `Technical docs <http://bio-tools.github.io/biotoolsSchema/>`_ maintained in `GitHub <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/>`_ where you'll find example data files
- Usage guidelines including the bio.tools `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#>`_ and `API Usage Guide <http://biotools.readthedocs.io/en/latest/api_usage_guide_dev.html>`_

.. note::
   Version 3.0.0 is currently supported in `bio.tools <https://bio.tools>`_.


Download
--------
**Latest stable version** (3.0.0)

- https://github.com/bio-tools/biotoolsSchema/blob/master/stable/biotools.xsd

**Current development version**

- https://github.com/bio-tools/biotoolsSchema/blob/master/biotools_dev.xsd
  
**Versioned releases**

- https://github.com/bio-tools/biotoolsSchema/tree/master/versions


Status
------
biotoolsSchema is a mature schema having undergone a lot of community-driven revision (*e.g.* see `bio.tools events <http://biotools.readthedocs.io/en/latest/events.html>`_).  Development is use-case driven, primarily by `bio.tools <https://bio.tools>`_.  Future versions will not depart fundamentally from the current elements or structure.  The development of biotoolsSchema can be followed at `GitHub <https://github.com/bio-tools/biotoolsschema/>`_.  From version 2.0.0, version numbers follow the `MAJOR.MINOR.PATCH` pattern:

* `MAJOR` version for incompatible API changes
* `MINOR` version for addition of functionality in a backwards-compatible manner
* `PATCH` version for backwards-compatible bug fixes

Please contribute via `GitHub <https://github.com/bio-tools/biotoolsSchema>`_.  See also the bio.tools `Contributors Guide <http://biotools.readthedocs.org/en/latest/contributors_guide.html>`_. 

Motivation
----------
Bioinformaticians routinely use a large and diverse set of tools and data, and demand powerful and convenient means to organise, find, understand, compare, select, use and connect the available resources. These tasks rely on consistent, machine-understandable resource descriptions. The need - filled by biotoolsSchema - is for an information model that puts the description of a broad range of resources  on a consistent syntactic basis. 

Citing biotoolsSchema
---------------------
If you use biotoolsSchema, please cite:

Ison, J. et al. (2016). Tools and data services registry: a community effort to document bioinformatics resources. *Nucleic Acids Research*, **44** (D1): D38-D47.

The article is `freely available <http://nar.oxfordjournals.org/content/44/D1/D38>`_.

doi: `10.1093/nar/gkv1116 <http://doi.org/10.1093/nar/gkv1116>`_ 


