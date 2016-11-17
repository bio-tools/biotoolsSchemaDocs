Information requirement
=======================

bio.tools standard
------------------
Attributes defined as mandatory in the schema version used by bio.tools (`biotools-1.4 <https://github.com/bio-tools/biotoolsSchema/tree/master/versions/biotools-1.4>`_) and the latest stable version (`biotools-2.0.0 <https://github.com/bio-tools/biotoolsSchema/tree/master/versions/biotools-2.0.0>`_) are indicated by "Version" column.  https://bio.tools specifies an information requirement for "standard" and "beta" (less well annotated) entries, as indicated in the respective columns.

.. csv-table:: Information requirements
   :header: "Attribute", "Description", "Format", "beta", "standard", "Version", "element"
   :widths: 15, 75, 10, 10, 10, 10, 10

   "name (1 only)", "Canonical resource name", "Text", "y", "y", "1.4, 2.0.0", "``<name>``, ``<name>``"
   "toolID (1 only)", "Unique tool ID", "Text", "y", "y", "2.0.0", "``<toolID>``"
   "homepage (1 only)", "Resource homepage", "URL", "y", "y", "1.4, 2.0.0", "``<homepage>``, ``<homepage>``"
   "description (1 only)", "Short textual description of the resource", "Text", "y", "y", "1.4, 2.0.0", "``<description>``, ``<description>``"
   "tool type (1 or more)", "Type of tool.  A tool may have more than one type reflecting its different facets.", "enum (see below)", "y", "y", "2.0.0", "``<toolType>``"
   "resource type (1 or more)", "Basic resource type", "enum (see below)", "n/a", "n/a", "1.4", "``<resourceType>``"
   "interface type (1 or more)", "Resource interface type", "enum (see below)", "n/a", "n/a", "1.4", "``<interfaceType>``"
   "topic (1 or more)", "General scientific domain(s) the resource serves, e.g. 'Proteomics'", "Term and / or URI of `EDAM Topic <http://edamontology.org/topic_0004>`_ concept(s) (1)", "y", "y", "1.4, 2.0.0", "``<topic>``"
   "function (1 or more)", "The basic resource function(s), e.g. 'Multiple sequence alignment'", "Term and / or URI of `EDAM Operation <http://edamontology.org/operation_0004>`_ concept(s)", "y", "y", "1.4, 2.0.0", "``<function><functionName>>``, ``<function><operation>>``"
   "input data (0 or more)", "Type(s) of data: primary inputs (if any), e.g. 'Protein sequences'", "Term and / or URI of `EDAM Data <http://edamontology.org/data_0006>`_ concept(s)", "-", "y", "-", "``<function><input><dataType>>``, ``<function><input><data>>``"
   "output data (0 or more)", "Type(s) of data: primary outputs (if any), e.g. 'Protein sequence alignment'", "Term and / or URI of `EDAM Data <http://edamontology.org/data_0006>`_ concept(s)", "-", "y", "-", "``<function><output><dataType>>``, ``<function><output><data>>``"
   "contact (1 or more)", "Primary contact, e.g. a person, helpdesk or mailing list", "Email address and / or URL of contact (2)", "-", "y", "1.4", "``<contact>``, ``<contact>``"
   "publication (0 or more)", "Publications about the software", "PMID, PMCID or DOI", "-", "y", "-", "``<publication>``, ``<publication>``"

.. note:: (1) EDAM is a simple ontology of well established, familiar concepts that are prevalent within bioinformatics, including types of data and data identifiers, data formats, operations and topics. EDAM provides a set of terms with synonyms and definitions - organised into an intuitive hierarchy for convenient use.  You can find `EDAM on GitHub <https://github.com/edamontology/edamontology>`_.


Tool types
----------
Valid values of toolType in in the latest schema (`biotools-2.0.0 <https://github.com/bio-tools/biotoolsSchema/tree/master/versions/biotools-2.0.0>`_).

.. csv-table:: Tool types
   :header: "Type", "Description"
   :widths: 25, 100
	    
   "Command-line tool", "A tool with a text-based (command-line) interface."
   "Database portal", "A Web application, suite or workbench providing a portal to a biological database."
   "Desktop application", "A tool with a graphical user interface that runs on your desktop environment, e.g. on a PC or mobile device."
   "Library", "A collection of components that are used to construct other tools.  bio.tools scope includes component libraries performing high-level bioinformatics functions but excludes lower-level programming libraries."
   "Ontology", "A collection of information about concepts, including terms, synonyms, descriptions etc."
   "Plug-in", "A software component encapsulating a set of related functions, which are not standalone, i.e. depend upon other software for its use, e.g. a Javascript widget, or a plug-in, extension add-on etc. that extends the function of some existing tool."
   "Script", "A tool written for some run-time environment (e.g. other applications or an OS shell) that automates the execution of tasks. Often a small program written in a general-purpose languages (e.g. Perl, Python) or some domain-specific languages (e.g. sed)."
   "SPARQL endpoint", "A service that provides queries over an RDF knowledge base via the SPARQL query language and protocol, and returns results via HTTP."
   "Suite", "A collection of tools which are bundled together into a convenient toolkit.  Such tools typically share related functionality, a common user interface and can exchange data conveniently.  This includes collections of stand-alone command-line tools, or Web applications within a common portal."
   "Web application", "A tool with a graphical user interface that runs in your Web browser."
   "Web API", "An application programming interface (API) consisting of endpoints to a request-response message system accessible via HTTP.  Includes everything from simple data-access URLs to RESTful APIs."
   "Web service", "An API described in a machine readable form (typically WSDL) providing programmatic access via SOAP over HTTP."
   "Workbench", "An application or suite with a graphical user interface, providing an integrated environment for data analysis which includes or may be extended with any number of functions or tools.  Includes workflow systems, platforms, frameworks etc."
   "Workflow", "A set of tools which have been composed together into a pipeline of some sort.  Such tools are (typically) standalone, but are composed for convenience, for instance for batch execution via some workflow engine or script."

