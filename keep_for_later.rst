## From controlled_vocabularies.rst
   "disk image format ", "Virtual machine disk image format, e.g. 'aki'."
   "containers format", "Virtual machine container format, e.g. 'singularity'."

Disk image format
-----------------
*Virtual machine disk image format*

.. csv-table::
   :header: "Disk format", "Description"
   :widths: 25, 100

   "aki", "An Amazon kernel image"
   "ami", "An Amazon machine image"
   "ari", "An Amazon ramdisk image"
   "iso", "An archive format for the data contents of an optical disc, such as CD-ROM"
   "qcow2", "Supported by the QEMU emulator that can expand dynamically and supports Copy on Write"
   "raw", "An unstructured disk image format; if you have a file without an extension it is possibly a raw format"
   "vdi", "Supported by VirtualBox virtual machine monitor and the QEMU emulator"
   "vhd", "The VHD disk format, a common disk format used by virtual machine monitors from VMware, Xen, Microsoft, VirtualBox, and others"
   "vmdk", "Common disk format supported by many common virtual machine monitors"

Container format
----------------
*Container format*

.. csv-table::
   :header: "Container format", "Description"
   :widths: 25, 100

   "aki", "An Amazon kernel image"
   "ami", "An Amazon machine image"
   "ari", "An Amazon ramdisk image"
   "bare", "The image does not have a container or metadata envelope"
   "docker", "A docker container format"
   "ovf", "The OVF container format"
   "rkt", "Rocket container image"
   "singularity", "Singularity container format"



## From biotoolsschema_elements.rst
   "diskFormat", "Virtual machine image disk format.", "enum (see `docs <http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#disk-image-format>`__)", "0 or 1"
   "containerFormat", "Virtual machine container format.", "enum (see `docs <http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#container-format>`__)", "0 or 1"

   
   


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
   "isAvailable", "Used (with value of 'Not available') when a download of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"

"cmd", "A useful command pertinent to the download, e.g. for getting or installing a tool.", "xs:token (restriction)", "0 or 1"

"isAvailable", "Used (with value of 'Not available') when documentation of a certain type is known not to be available.", "enum ('Not available')", "0 or 1"

   "isAvailable", "Used (with value of 'Not available') when a publication is known not to be available.", "enum ('Not available')", "0 or 1"

   
