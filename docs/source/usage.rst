Usage
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']


.. raw:: html

    <div class="sticky-first-column">

.. csv-table:: Biocuration Resource Table - main table
    :header: Type, Name, Curation(Manual/Automated), Programmatic access?, Input format, Output format, Number of models/pathways/interactions if database, Systems modeled?, Automated verification or validation?, Automated filtering?, Automated identification of extensions/contradictions, Automatically resolve contradictions?, Automatically resolve contradictions?
    :widths: 5, 5, 10, 10, 6, 6, 34, 6, 20, 15, 30, 20, 20

    Entity database,GO (Gene Ontology),Maual and automated,Yes (API),N/A,"OWL, OBO, GAF, etc.","43,850 GO terms / 7,928,834 annotations /1,568,828 gene products",Multiple species,No,No,No,No,No
    Entity database,miRBase,Manual (staff curators),No,N/A,"FASTA, EMBL","38,589 miRNAs",Multiple species,No,No,No,No,No
    Entity database,ChEBI (Chemical Entities of Biological Interest),Manual (staff curators),Yes (Web service),N/A,"Molfile, XML, SDF","151,344 substances / 139,678 annotations",Multiple species,No,No,No,No,No
    Interaction database,BioGRID (The Biological General Repository for Interaction Datasets),Manual and automated,Yes (API),N/A,"PSI-MITAB, XML, BioGRID TAB",>3 million interactions,Multiple species,No,No,No,No,No
    Interaction database,HPRD (Human Protein Reference Database),Manual (staff curators),No,N/A,"BioPAX, SBML, PSI-MI",">40,000 PPI, 36 pathways",Homo sapiens,No,No,No,No,No
    Interaction database,KEGG (Kyoto Encyclopedia of Genes and Genomes),Manual (staff curators and data providers),Yes (API),N/A,"KGML, PNG","70,423 references ",Multiple Species,No,No,No,No,No
    Interaction database,MINT (Molecular Interaction Database),Manual (registered users),Yes (API),N/A,MITAB,"136,218 interactions",Multiple Species,No,No,No,No,No
    Interaction database,PathwayCommons ,Manual (from data providers),No,N/A,"PNG, SIF, JSON, SBGN, BioPAX","5,772 pathways /2,424,055 interactions/ 22 databases",Multiple species,No,No,No,No,No
    Interaction database,Reactome,Manual (staff curators),Yes (API),N/A,"SBML, BioPAX, SBGN,PNG","13,827 interactions / 2536 pathways",Homo sapiens,No,No,No,No,No
    Interaction database,SIGNOR (Signaling Network Open Resource),Manual (staff curators),Yes (API),N/A,"SBML, TSV","29,245 interactions","Homo sapiens, Mus musculus, Rattus norvegicus",No,No,No,No,No
    Interaction database,STITCH (Search Tool for Interacting Chemicals),Manual and automated,Yes (API),N/A,"TSV, PNG, XML, MFA",1.6 billion interactions,Multiple species,No,No,No,No,Yes
    Interaction database,STRING (Search Tool for Retrieval of Interacting Genes/Proteins),Manual and automated,Yes (API),N/A,"TSV, PNG, XML, MFA",>20 billion interactions,Multiple species,No,No,No,No,Yes
    Interaction database,WikiPathways,Manual (registered users),No,GPML,"PNG, JSON, GPML, SVG",">1,100 pathways",Multiple species,No,No,No,No,No
    Metadatabase,FLUTE (FiLter for Understanding True Events),Manual (staff curators),Yes (Python script),N/A,"BioRECIPE, SIF",30 million+ interactions,Homo sapiens,No,No,No,No,No
    Metadatabase,INDRA (Integrated Network and Dynamical Reasoning Assembler),Manual and automated,Yes (API),N/A,"PySB, SBML, BEL, JSON",N/A,Multiple Species,Has model-checking function,Belief score,No,No,No
    Metadatabase,IntAct,Manual (staff curators),No,N/A,PSI-MITAB,"5,565,271 interactions",Multiple Species,No,No,No,No,No
    Metadatabase,OmniPath,Manual (staff curators),Yes (API),N/A,SIF,100+ networks/databases,Multiple Species,No,No,No,No,No
    Metadatabase,PCnet (Parsimonius Composite Network),Manual (staff curators),No,N/A,SIF,21 networks/databases,Homo sapiens,No,No,No,No,No
    Model repository,BioModels,Manual (registered users),No,"SBML (preferred), CellML, matlab","SBML,XPP, VCML, SciLab, Octave, BioPAX, PNG, SVG","2,914 models",Multiple species,No,No,No,No,No
    Model repository,CellCollective,Manual (registered users),No,"SBML, boolean expressions","SBML, GML, truth tables, boolean expressions",229 models,Multiple species,Yes (simulation),No,No,No,No
    Model repository,Path2Models,Automated (from other databases),No,N/A,"SBML,XPP, VCML, SciLab, Octave, BioPAX, PNG, SVG","~140,00 models",Multiple Species,No,Models are sorted by genus,No,No,No
    Model repository,MINERVA,Manual (registered users),Yes (API),SBML,"CellDesigner SBML, SBML, SBGN, PNG",9 networks,Multiple species,Yes (model annotation requirements),No,No,No,No
    Model repository,BioKC,Manual (registered users),Yes (API),SBML,,No public networks,Multiple species,Yes (model annotation requirements),No,No,No,Yes
    Model repository/metadatabase,nDex (The Network Data Exchange),Manual (registered users),Yes (API),CX,"TSV, CX",">5,000 networks",Multiple species,No,No,No,No,No
    Reader,REACH (Reading and Assembling Contextual and Holistic Mechanisms from Text),N/A,Yes (API),"NXML, text","JSON,TSV",N/A,N/A,No,No,No,No,No
    Reader,RLIMS-P (Rule-based Literature Mining System for Protein Phosphorylation),N/A,No,"Keywords, PMIDs",TSV,N/A,N/A,No,No,No,No,No
    Reader,Sparser,N/A,Yes (Lisp),"Text, XML",None,N/A,N/A,No,No,No,No,No
.. raw:: html

    </div>

