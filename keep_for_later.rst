   "relation type ", "Type of relation between this and another registered software, e.g. 'isInterfaceTo'.", "`link <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`__"
   "shortDescription", "Short and concise textual description of the software function.", "xs:token (restriction)", "0 or 1"
   "goTermID", "Gene function including molecular function, cellular component and biological process.  Miscellaneous ontology annotation. The ID of Gene Ontology (GO) concept(s) are specified.", "xs:token (restriction)", "0 or more"
   "soTermID", "Features which can be located on a biological sequence. The ID of Sequence Ontology (SO) concept(s) are specified.", "xs:token (restriction)", "0 or more"
   "taxId", "NCBI taxonomy ID of taxonomic group the software (particularly database portals) caters for.", "xs:token (restriction)", "0 or more"

   Relation group
^^^^^^^^^^^^^^
*Details of a relationship this software shares with other software registered in bio.tools.*

See the `GitHub docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`__.

API spec group
^^^^^^^^^^^^^^
*Details of the API to a service including service endpoints.*

See the `GitHub docs <https://github.com/bio-tools/biotoolsSchema/tree/master/stable/docs>`__.

   "isAvailable", "Used (with value of 'Not available') when a link of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"
