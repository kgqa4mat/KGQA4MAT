# Knowledge Graph Question Answering for Materials Science (KGQA4MAT)
## A Benchmark for Developing Natural Language Interface for Metal-Organic Frameworks Knowledge Graph (MOF-KG)

Data source 1: The MOF collection in the CSD database: https://www.ccdc.cam.ac.uk/free-products/csd-mof-collection/ 

Data Source 2: The synthesis procedures extracted from the literature: Mining Insights on Metal–Organic Framework Synthesis from Scientific Literature Texts. Hyunsoo Park, Yeonghun Kang, Wonyoung Choe, and Jihan Kim. https://doi.org/10.1021/acs.jcim.1c01297 

Data Source 3: Computation-Ready Experimental Metal-Organic Framework (CoRE MOF) 2019 Dataset: https://zenodo.org/record/3370144#.ZDvnDNLMKCU

Data Source 4: Reticular Chemistry Naming and Numbering Database: https://globalscience.berkeley.edu/database

The following steps describe how to create the MOF-KG from the sources:
- Download the MOF collection, CoRE dataset, RCNN dataset, and the extracted MOF synthesis procedures.
- Query the CSD crystal database using licensed CSD Python API to extract the information about crystal system and space group.
- Apply the CSD ConQuest tool to identify a MOF's {family} by applying the search criteria developed by Moghadam et al. in [1]. There are six prototypical   MOF families identified: Zr-oxide nodes (e.g. UiO-66), Cu–Cu paddlewheels (e.g. HKUST-1), ZIF-like, Znoxide nodes, IRMOF-like, and MOF-74/CPO-27-like   materials.
- Leverage the MOFid system\footnote{https://github.com/snurr-group/mofid} developed by Bucior et al. in [2] to identify a MOF's metals, organic linkers, and topology.
- Populate the MOF-KG by directly mapping the extracted data to the ontology.
