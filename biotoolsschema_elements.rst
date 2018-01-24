biotoolsSchema elements
=======================

A summary of elements in biotoolsSchema is below, focussing on what is currently supported in `bio.tools <https://bio.tools>`_.  For further information, please see the `comprehensive documentation <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_ on GitHub.


Element groups
--------------
biotoolsSchema includes scientific, technical and administrative software attributes, organised for convenience into 11 logical groupings (see below).


.. image:: images/tool.png

.. csv-table::
   :header: "Group", "XSD element", "Description"
   :widths: 25, 50, 50
	    
   "Summary", "summary", "Basic information about the software."
   "Function", "function", "Details of the function(s) (i.e. modes of operation) the software provides, expressed in terms from the EDAM ontology."
   "Labels", "label", "Miscellaneous scientific, technical and administrative details of the software, expressed in terms from controlled vocabularies."
   "Links", "lnk", "Miscellaneous links for the software e.g. repository, issue tracker or mailing list."
   "Downloads", "download", "Links to downloads for the software, e.g. source code, virtual machine image or container."
   "Documentation", "documentation", "Links to documentation about the software e.g. manual, API specification or training material."
   "Publications", "publication", "Publications about the software."
   "Credits", "credit", "Individuals or organisations that should be credited, or may be contacted about the software."


Elements
--------
  

Summary group
^^^^^^^^^^^^^
*Basic information about the software.*

.. image:: images/summary.png

.. image:: images/otherid.png
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
      
   "name", "Canonical software name assigned by the software developer or service provider.", "xs:token (restriction)", "1 only"
   "shortDescription", "Short and concise textual description of the software function.", "xs:token (restriction)", "0 or 1"
   "description", "Textual description of the software.", "xs:token (restriction)", "1 only"
   "homepage", "Homepage of the software, or some URL that best serves this purpose.", "URL", "1 only"
   "biotoolsId", "Unique ID (case insensitive) of the tool that is assigned upon registration of the software in bio.tools, normally identical to tool name.", "URL (restriction)", "0 or 1"
   "biotoolsCURIE ", "bio.tools CURIE (compact URI) based on the bio.tools tool ID.", "xs:token (restriction)", "0 or 1"
   "version", "Version information (typically a version number) of the software applicable to this bio.tools entry.", "xs:token (restriction)", "0 or more"
   "otherID", "A unique identifier of the software, typically assigned by an ID-assignment authority other than bio.tools.", "(see below)", "0 or more"
   "otherID->value", "Value of tool identifier.", "xs:token (restriction)", "1 only"
   "otherID->type", "Type of tool identifier.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_)", "0 or 1"
   "otherID->version", "Version information (typically a version number) of the software applicable to this identifier.", "xs:token (restriction)", "0 or 1"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#summary-group>`_

	    
Function group
^^^^^^^^^^^^^^
*Details of a function (i.e. mode of operation) the software provides, expressed in terms from the EDAM ontology.*

Each software entity has one more functions, each corresponding to a mode of operation that the software provides.  Each function performs one or more basic operations, and has zero or more primary input and/or output data, each of a specified type and supported format(s).
For each operation, data or format element, an `EDAM ontology <https://github.com/edamontology/edamontology>`_ concept URL and/or term are specified.  

.. important::

   The URL must be in the appropriate EDAM Operation | Data | Format namespace, *e.g.*

   * http://edamontology.org/operation_0492
   * http://edamontology.org/data_0863
   * http://edamontology.org/format_1929

   The term, *e.g.* "Multiple sequence alignment" must be either the preferred label of the concept or a synonym of this term, as defined in EDAM.
   
.. image:: images/function.png

.. image:: images/operation.png

   Data and Format are modelled in the same way as Operation (shown above).
	   
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100

   "operation", "The basic operation(s) performed by this software function (EDAM Operation).", "Ontology concept (restriction)", "1 or more"
   "input", "*Details of primary input data.*", "-", "-"
   "input->data", "Type of primary input data, if any (EDAM data). ", "Ontology concept (restriction)", "1 only"
   "input->format", "Allowed format(s) of the input data (EDAM Format). ", "Ontology concept (restriction)", "0 or more"
   "output", "*Details of primary output data.*", "-", "-"
   "output->data", "Type of primary output data, if any (EDAM Data).", "Ontology concept (restriction)", "1 only"
   "output->format", "Allowed format(s) of the output data (EDAM Format).", "Ontology concept (restriction)", "0 or more"
   "operation | data | format | topic->url", "URL of an EDAM Operation | Data | Format concept.", "URL (restriction)",  "0 or 1"
   "operation | data | format | topic->term", "An EDAM Operation | Data | Format term (preferred label or synonym).", "xs:token", "0 or 1"
   "comment", "Concise comment about this function, if not apparent from the software description and EDAM annotations.", "xs:token (restriction)", "0 or 1"
   "cmd", "Relevant command, command-line fragment or option for executing this function / running the tool in this mode.", "xs:token (restriction)", "0 or 1"


.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#function-group>`_
      
   
Labels group
^^^^^^^^^^^^
*Miscellaneous scientific, technical and administrative details of the software, expressed in terms from controlled vocabularies.*

.. image:: images/labels.png
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
	    
   "toolType", "A type of application software: a discrete software entity can have more than one type.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#tool-type>`_)", "0 or more"
   "topic", "General scientific domain the software serves or other general category: one of EDAM Topic URL or term is specified.", "Ontology concept (restriction)", "0 or more"
   "topic->url", "URL of an EDAM Topic concept.", "URL (restriction)", "0 or 1"
   "topic->term", "An EDAM Topic term (preferred label or synonym).", "xs:token", "0 or 1"
   "goTermID", "Gene function including molecular function, cellular component and biological process.  Miscellaneous ontology annotation. The ID of Gene Ontology (GO) concept(s) are specified.", "xs:token (restriction)", "0 or more"
   "soTermID", "Features which can be located on a biological sequence. The ID of Sequence Ontology (SO) concept(s) are specified.", "xs:token (restriction)", "0 or more"
   "taxId", "NCBI taxonomy ID of taxonomic group the software (particularly database portals) caters for.", "xs:token (restriction)", "0 or more"
   "operatingSystem", "The operating system supported by a downloadable software package.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#operating-system>`_)", "0 or more"
   "language", "Name of programming language the software source code was written in.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/>`_)", "0 or more"
   "license", "Software or data usage license.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_)", "0 or 1"
   "collectionID", "Tag for a collection that the software has been assigned to within bio.tools.", "xs:token (restriction)", "0 or more"
   "maturity", "How mature the software product is.", "enum (see `link <http://biotools.readthedocs.io/en/latest/curators_guide.html#maturity>`_)", "0 or 1"
   "cost", "Monetary cost of acquiring the software.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_)", "0 or 1"
   "accessibility", "Whether the software is freely available for use.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#accessibility>`_)", "0 or more"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#labels-group>`_.

Relation group
^^^^^^^^^^^^^^
*Details of a relationship this software shares with other software registered in bio.tools.*

See the `GitHub docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_.

API spec group
^^^^^^^^^^^^^^
*Details of the API to a service including service endpoints.*

See the `GitHub docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_.

Links group
^^^^^^^^^^^
*Miscellaneous links for the software e.g. repository, issue tracker or mailing list.*

.. image:: images/link.png

.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
	    
   "url", "A link of some relevance to the software (URL).", "URL", "1 only"
   "type", "The type of data, information or system that is obtained when the link is resolved.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#id60>`_)", "1 only"
   "comment", "Comment about the link.", "xs:token (restriction)", "0 or more"
   "isAvailable", "Used (with value of 'Not available') when a link of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"

   
.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#links-group>`_.
   

Download group
^^^^^^^^^^^^^^
*Links to downloads for the software, e.g. source code, virtual machine image or container.*

.. image:: images/download.png

.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100

   "url", "Link to download (or repo providing a download) for the software.", "URL", "1 only"
   "type", "Type of download that is linked to.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#download-type>`_)", "1 only"
   "comment", "Comment about the download.", "xs:token (restriction)", "0 or 1"
   "diskFormat", "Virtual machine image disk format.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_)", "0 or 1"
   "containerFormat", "Virtual machine container format.", "enum (see `docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_)", "0 or 1"
   "cmd", "A useful command pertinent to the download, e.g. for getting or installing a tool.", "xs:token (restriction)", "0 or 1"
   "version", "Version information (typically a version number) of the software applicable to this download.", "xs:token (restriction)", "0 or 1"
   "isAvailable", "Used (with value of 'Not available') when a download of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group>`_.

Documentation group
^^^^^^^^^^^^^^^^^^^
*Links to documentation about the software e.g. manual, API specification or training material.*

.. image:: images/documentation.png
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
	    
   "url", "Link to documentation on the web for the tool.", "URL", "1 only"
   "type", "Type of documentation that is linked to.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#id60>`_)", "1 only"
   "comment", "Comment about the documentation.", "xs:token (restriction)", "0 or more"
   "isAvailable", "Used (with value of 'Not available') when documentation of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group>`_.
   
Publications group
^^^^^^^^^^^^^^^^^^
*Publications about the software*

.. image:: images/publication.png
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
	    
   "pmcid", "PubMed Central Identifier of a publication about the software.", "xs:token (restriction)", "1 only"
   "pmid", "PubMed Identifier.", "xs:token (restriction)", "1 only"
   "doi", "Digital Object Identifier.", "xs:token (restriction)", "1 only"
   "type", "Type of publication.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-type>`_)", "0 or 1"
   "version", "Version information (typically a version number) of the software applicable to this publication.", "xs:token (restriction)", "0 or 1"
   "isAvailable", "Used (with value of 'Not available') when a publication is known not to be available.", "enum ('Not available')", "0 or 1"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#publications-group>`_.
   
Credits group
^^^^^^^^^^^^^
*Individuals or organisations that should be credited, or may be contacted about the software.*

.. image:: images/credit.png
	   
.. csv-table::
   :header: "Element", "Description", "Type", "Cardinality"
   :widths: 25, 50, 50, 100
	    
   "name", "Name of the entity that is credited.", "xs:token (restriction)", "1 only"
   "orcidId", "Unique identifier (ORCID iD) of a person that is credited.", "xs:token (restriction)", "0 or 1"
   "gridId", "Unique identifier (GRID ID) of an organisation that is credited.", "xs:token (restriction)", "0 or 1"
   "email", "Email address.", "email address", "0 or 1"
   "url", "URL, e.g. homepage of an institute.", "URL", "0 or 1"
   "tel", "Telephone number.", "xs:token (restriction)", "0 or 1"
   "typeEntity", "Type of entity that is credited.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#entity-type>`_)", "0 or 1"
   "typeRole", "Role performed by entity that is credited.", "enum (see `docs <http://biotools.readthedocs.io/en/latest/curators_guide.html#role>`_)", "0 or more"
   "comment", "A comment about the credit.", "xs:token (restriction)", "0 or 1"

.. note::
   See the `Curators Guide <http://biotools.readthedocs.io/en/latest/curators_guide.html#credits-group>`_.
   
ELIXIR information
^^^^^^^^^^^^^^^^^^
*Information for ELIXIR internal purposes, maintained by ELIXIR Hub.*

See the `GitHub docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_.


Controlled vocabularies
-----------------------
biotoolsSchema defines 16 controlled vocabularies - as standarised enumerations of terms - for description of technical software aspects (see below).

.. csv-table::
   :header: "Vocabulary", "Description", "Link"
   :widths: 25, 50, 50

   "tool type ", "The type of application software.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#tool-type>`_"
   "operating system ", "The operating system supported by a downloadable software package, e.g. 'Linux'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#operating-system>`_"
   "programming language ", "Name of programming language the software source code was written in, e.g. 'C'.", "`link <https://github.com/bio-tools/biotoolsSchema/>`_"
   "license ", "Software or data usage license, e.g. 'GPL-3.0'", "`link <https://github.com/bio-tools/biotoolsSchema/>`_"
   "relation type ", "Type of relation between this and another registered software, e.g. 'isInterfaceTo'.", "`link <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_"
   "maturity ", "How mature the software product is, e.g. 'Mature'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#maturity>`_"
   "cost ", "Monetary cost of acquiring the software, e.g. 'Free of charge'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#cost>`_"
   "accessibility ", "Whether the software is freely available for use, e.g. 'Open access'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#accessibility>`_"
   "link type", "The type of data, information or system that is obtained when the link is resolved, e.g. 'Helpdesk'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#id60>`_"
   "download type ", "Type of download that is linked to, e.g. 'Source code'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#download-type>`_"
   "documentation type ", "Type of documentation that is linked to, e.g. 'API documentation'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#id71>`_"
   "publication type ", "Type of publication, e.g. 'Review'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-type>`_"
   "entity type ", "Types of entities that may be credited, e.g. 'Person'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#entity-type>`_"
   "entity role ", "Roles that may be assigned to creditable entities, e.g. 'Developer'.", "`link <http://biotools.readthedocs.io/en/latest/curators_guide.html#role>`_"
   "disk image format ", "Virtual machine disk image format, e.g. 'aki'.", "`link <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_"
   "containers format", "Virtual machine container format, e.g. 'singularity'.", "`link <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`_"

