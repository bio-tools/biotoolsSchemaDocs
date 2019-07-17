Controlled vocabularies
=======================
biotoolsSchema defines 17 controlled vocabularies - as standarised enumerations of terms - for description of technical software aspects (see below).

.. csv-table::
   :header: "Vocabulary", "Description"
   :widths: 25, 50

   "tool type ", "The type of application software."
   "operating system ", "The operating system supported by a downloadable software package, e.g. 'Linux'."
   "programming language ", "Name of programming language the software source code was written in, e.g. 'C'."
   "license ", "Software or data usage license, e.g. 'GPL-3.0'"
   "maturity ", "How mature the software product is, e.g. 'Mature'."
   "cost ", "Monetary cost of acquiring the software, e.g. 'Free of charge'."
   "accessibility ", "Whether the software is freely available for use, e.g. 'Open access'."
   "link type", "The type of data, information or system that is obtained when the link is resolved, e.g. 'Helpdesk'."
   "download type ", "Type of download that is linked to, e.g. 'Source code'."
   "documentation type ", "Type of documentation that is linked to, e.g. 'API documentation'."
   "publication type ", "Type of publication, e.g. 'Review'."
   "relation type ", "Type of relation between this and another registered software, e.g. 'isNewVersionOf'."
   "entity type ", "Types of entities that may be credited, e.g. 'Person'."
   "entity role ", "Roles that may be assigned to creditable entities, e.g. 'Developer'."
   "ID type ", "Type of tool identifier, e.g. 'rrid'."
   "ELIXIR Platform ", "Name of the ELIXIR Platform that is credited, e.g. 'Tools'"
   "ELIXIR Node ", "Name of the ELIXIR Node that is credited, e.g. 'Norway'"



Tool type
---------
*The type of application software: a discrete software entity can have more than one type, e.g. "Command-line tool, Web application"*

.. csv-table::
   :header: "Type", "Description"
   :widths: 25, 100
      
   "Command-line tool", "A tool with a text-based (command-line) interface."
   "Database portal", "A Web application, suite or workbench providing a portal to a biological database."
   "Desktop application", "A tool with a graphical user interface that runs on your desktop environment, *e.g.* on a PC or mobile device."
   "Library", "A collection of components that are used to construct other tools.  bio.tools scope includes component libraries performing high-level bioinformatics functions but excludes lower-level programming libraries."
   "Ontology", "A collection of information about concepts, including terms, synonyms, descriptions etc."
   "Plug-in", "A software component encapsulating a set of related functions, which are not standalone, *i.e.* depend upon other software for its use, *e.g.* a Javascript widget, or a plug-in, extension add-on etc. that extends the function of some existing tool."
   "Script", "A tool written for some run-time environment (*e.g.* other applications or an OS shell) that automates the execution of tasks. Often a small program written in a general-purpose languages (*e.g.* Perl, Python) or some domain-specific languages (*e.g.* sed)."
   "SPARQL endpoint", "A service that provides queries over an RDF knowledge base via the SPARQL query language and protocol, and returns results via HTTP."
   "Suite", "A collection of tools which are bundled together into a convenient toolkit.  Such tools typically share related functionality, a common user interface and can exchange data conveniently.  This includes collections of stand-alone command-line tools, or Web applications within a common portal."
   "Web application", "A tool with a graphical user interface that runs in your Web browser."
   "Web API", "An application programming interface (API) consisting of endpoints to a request-response message system accessible via HTTP.  Includes everything from simple data-access URLs to RESTful APIs."
   "Web service", "An API described in a machine readable form (typically WSDL) providing programmatic access via SOAP over HTTP."
   "Workbench", "An application or suite with a graphical user interface, providing an integrated environment for data analysis which includes or may be extended with any number of functions or tools.  Includes workflow systems, platforms, frameworks etc."
   "Workflow", "A set of tools which have been composed together into a pipeline of some sort.  Such tools are (typically) standalone, but are composed for convenience, for instance for batch execution via some workflow engine or script."


Operating system
----------------

*The operating system supported by a downloadable software package, e.g. "Linux"*

.. csv-table::
   :header: "Maturity", "Description"
   :widths: 25, 100
	    
   "Linux", "All flavours of Linux/UNIX operating systems."
   "Windows", "All flavours of Microsoft Windows operating system."
   "Mac", "All flavours of Apple Macintosh operating systems (primarily Mac OS X)."

Programming language
--------------------

*Name of programming language the software source code was written in, e.g. "C"*

See the `technical docs <http://bio-tools.github.io/biotoolsSchema/>`_ for a list of valid terms.

License
-------
*Software or data usage license, e.g. "GPL-3.0"*

See the `technical docs <http://bio-tools.github.io/biotoolsSchema/>`_ for a list of valid terms.

Maturity
--------
*How mature the software product is, e.g. "Mature"*

.. csv-table::
   :header: "Maturity", "Description"
   :widths: 25, 100

   "Emerging", "Nascent or early release software that may not yet be fully featured or stable."
   "Mature", "Software that is generally considered to fulfill several of the following: secure, reliable, actively maintained, fully featured, proven in production environments, has an active community, and is described or cited in the scientific literature."
   "Legacy", "Software which is no longer in common use, deprecated by the provider, superseded by other software, replaced by a newer version, is obsolete etc."

Cost
----
*Monetary cost of acquiring the software, e.g. "Free of charge (with retritions)"*

.. csv-table::
   :header: "Cost", "Description"
   :widths: 25, 100

   "Free of charge", "Software which available for use by all, with full functionality, at no monetary cost to the user."
   "Free of charge (with restrictions)", "Software which is available for use at no monetary cost to the user, but possibly with limited functionality, usage restrictions, or other limitations."
   "Commercial", "Software which you have to pay to access."

Accessibility
-------------
*Whether the software is freely available for use, e.g. "Open access"*

.. csv-table::
   :header: "Accessibility", "Description"
   :widths: 25, 100

   "Open access", "An online service which is available for use to all, but possibly requiring user accounts / authentication."
   "Restricted access", "An online service which is available for use to a restricted audience, e.g. members of a specific institute."
   "Proprietary", "Software for which the software's publisher or another person retains intellectual property rights Å\ usually copyright of the source code, but sometimes patent rights."
   "Freeware", "Proprietary software that is available for use at no monetary cost. In other words, freeware may be used without payment but may usually not be modified, re-distributed or reverse-engineered without the author's permission."

Link type
---------
*The type of data, information or system that is obtained when the link is resolved, e.g. "Mailing list"*

.. csv-table::
   :header: "Link type", "Description"
   :widths: 25, 100

   "Discussion forum", "Online forum for user discussions about the software."
   "Helpdesk", "Helpdesk providing support in using the software."
   "Issue tracker", "Tracker for software issues, bug reports, feature requests etc."
   "Mailing list", "Mailing list for the software announcements, discussions, support etc."
   "Mirror", "Mirror of an (identical) online service."
   "Registry", "Some registry, catalogue etc. other than bio.tools."
   "Repository", "Repository where source code, data and other files may be downloaded."
   "Social media", "A website used by the software community including social networking sites, discussion and support fora, WIKIs etc."
   "Scientific benchmark", "Information about the scientific performance of a tool."
   "Service", "An online service that provides access (an interface) to the software."
   "Technical monitoring", "Information about the technical status of a tool."
   "Other", "Other type of link for software - the default if a more specific type is not available."




Download type
-------------
*Type of download that is linked to, e.g. "Binaries"*

.. csv-table::
   :header: "Download type", "Description"
   :widths: 25, 100

   "API specification", "File providing an API specification for the software, e.g. Swagger/OpenAPI, WSDL or RAML file."
   "Biological data", "Biological data, or a web page on a database portal where such data may be downloaded. "
   "Binaries", "Binaries for the software."
   "Binary package", "Binary package for the software."
   "Command-line specification", "File providing a command line specification for the software."
   "Container file", "Container file including the software."
   "CWL file", "Common Workflow Language (CWL) file for the software."
   "Icon", "Icon of the software."
   "Ontology", "A file containing an ontology, controlled vocabulary, terminology etc."
   "Screenshot", "Screenshot of the software."
   "Source code", "Software source code."
   "Source package", "Source package (of various types) for the software."
   "Test data", "Data for testing the software is working correctly."
   "Test script", "Script used for testing testing whether the software is working correctly."
   "Tool wrapper (galaxy)", "Galaxy tool configuration file (wrapper) for the software."
   "Tool wrapper (taverna)", "Taverna configuration file for the software."
   "Tool wrapper (other)", "Workbench configuration file (other than taverna, galaxy or CWL wrapper) for the software."
   "VM image", "Virtual machine (VM) image for the software."   
   "Downloads page", "Web page summarising general downloads available for the software."
   "Other", "Other type of download for software - the default if a more specific type is not available."


     
Documentation type
------------------
*Type of documentation that is linked to, e.g. "Citation instructions"*

.. csv-table::
   :header: "Documentation type", "Description"
   :widths: 25, 100
		
   "API documentation", "Human-readable API documentation."
   "Citation instructions", "Information on how to correctly cite use of the software."
   "Command-line options", "Information about the command-line interface to a tool."
   "Contributions policy", "Information about policy for making contributions to the software project."
   "FAQ", "Frequently Asked Questions (and answers) about the software."
   "General", "General documentation."
   "Governance", "Information about the software governance model."
   "Installation instructions", "Instructions how to install the software."
   "Manual ", "Information on how to use the software."
   "Release notes", "Notes about a software release or changes to the software; a change log."
   "Terms of use", "Rules that one must agree to abide by in order to use a service."
   "Training material", "Online training material such as text on a Web page, a presentation, video, tutorial etc."
   "Tutorial", "A tutorial about using the software."
   "Other", "Some other type of documentation not listed in biotoolsSchema."



   
Publication type
----------------
*Type of publication, e.g. "Primary"*

.. csv-table::
   :header: "Publication type", "Description"
   :widths: 25, 100
	    
   "Primary", "The principal publication about the tool itself; the article to cite when acknowledging use of the tool."
   "Method", "A publication describing a scientific method or algorithm implemented by the tool."
   "Usage", "A publication describing the application of the tool to scientific research, a particular task or dataset."
   "Comparison", "A publication which assessed the performance of the tool."
   "Review", "A publication where the tool was reviewed."
   "Other", "A publication of relevance to the tool but not fitting the other categories."

Relation type
-------------
*Type of relation between this and another registered software, e.g. "isNewVersionOf"*

.. csv-table::
   :header: "Relation type", "Description"
   :widths: 25, 100

   "isNewVersionOf", "The software is a new version of an existing software, typically providing new or improved functionality."
   "hasNewVersion", "(inverse of above)"
   "uses", "The software provides an interface to or in some other way uses the functions of other software under the hood, e.g. invoking a command-line tool or calling a Web API, Web service or SPARQL endpoint to perform its function."
   "usedBy", "(inverse of above)"
   "includes", "A workbench, toolkit or workflow includes some other, independently available, software."
   "includedIn", "(inverse of above)"

   
Entity type
-----------
*Type of entity that is credited, e.g. "Person"*

.. csv-table::
   :header: "Entity type", "Description"
   :widths: 25, 100

   "Person", "Credit of an individual."
   "Project", "Credit of a community software project not formally associated with any single institute."
   "Division", "Credit of or a formal part of an institutional organisation, e.g. a department, research group, team, etc"
   "Institute", "Credit of an organisation such as a university, hospital, research institute, service center, unit etc."
   "Consortium", "Credit of an association of two or more institutes or other legal entities which have joined forces for some common purpose.  Includes Research Infrastructures (RIs) such as ELIXIR, parts of an RI such as an ELIXIR node etc. "
   "Funding agency", "Credit of a legal entity providing funding for development of the software or provision of an online service."

Entity role
-----------
*Role performed by entity that is credited, e.g. "Developer"*

.. csv-table::
   :header: "Role", "Description"
   :widths: 25, 100
	    
   "Developer", "Author of the original software source code."
   "Maintainer", "Maintainer of a mature software providing packaging, patching, distribution etc."
   "Provider", "Institutional provider of an online service."
   "Documentor", "Author of software documentation including making edits to a bio.tools entry."
   "Contributor", "Some other role in software production or service delivery including design, deployment, system administration, evaluation, testing, documentation, training, user support etc."
   "Support", "Provider of support in using the software."
   "Primary contact", "The primary point of contact for the software."


ID type
-------
*Type of tool identifier, e.g. "rrid"*

.. csv-table::
   :header: "Role", "Description"
   :widths: 25, 100

   "doi", "Digital Object Identifier of the software assigned (typically) by the software developer or service provider."
   "rrid", "Research Resource Identifier as used by the NIH-supported Resource Identification Portal (https://scicrunch.org/resources)."
   "cpe", "Common Platform Enumeration (CPE) identifier as listed in the CPE dictionary (https://cpe.mitre.org/dictionary/)."
   "biotoolsCURIE", "bio.tools CURIE (secondary identifier)."      

ELIXIR Platform
---------------
*Name of the ELIXIR Platform that is credited, e.g. "Tools"*

.. csv-table::
   :header: "ELIXIR Platform", "Description"
   :widths: 25, 100
	    
   "Data", "ELIXIR Data Platform"
   "Tools", "ELIXIR Tools Platform"
   "Compute", "ELIXIR Compute Platform"
   "Interoperability", "ELIXIR Interoperability Platform"
   "Training", "ELIXIR Training Platform"


ELIXIR Node
-----------
*Name of the ELIXIR Node that is credited, e.g. "Norway"*

.. csv-table::
   :header: "ELIXIR Node"
   :widths: 25
	    
   "Belgium"
   "Czech Republic"
   "Denmark"
   "EMBL"
   "Estonia"
   "Finland"
   "France"
   "Germany"
   "Greece"
   "Hungary"
   "Ireland"
   "Israel"
   "Italy"
   "Luxembourg"
   "Netherlands"
   "Norway"
   "Portugal"
   "Slovenia"
   "Spain"
   "Sweden"
   "Switzerland"
   "UK"
