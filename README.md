# Wikibase knowledge graphs

[![DOI](https://zenodo.org/badge/381375115.svg)](https://zenodo.org/badge/latestdoi/381375115)

A collection of open source tools and resources related to [Wikibase](https://www.wikiba.se) knowledge graphs.

- [Motivation](#motivation)
- [Awesome knowledge graphs](#awesome-knowledge-graphs)
- [Awesome Wikibase tutorials](#awesome-wikibase-tutorials)
- [Wikibase Architecture](#wikibase-architecture)
- [Installing Wikibase](#installing-wikibase)
- [Data Model](#data-model)
- [Data Import](#data-import)
  * [The Wikibase frontend](#the-wikibase-frontend)
  * [The Wikibase API and wrappers](#the-wikibase-api-and-wrappers)
  * [The Mediawiki MySQL database](#the-mediawiki-mysql-database)
- [Federated Properties](#federated-properties)
- [Data wrangling](#data-wrangling)
- [Data reconciliation](#data-reconciliation)
- [Named Entity Linking](#named-entity-linking)
  * [Texts](#texts)
  * [Tables](#tables)
- [Data validation](#data-validation)
- [Wikibase Ecosystem](#wikibase-ecosystem)
- [Wikibase Community](#wikibase-community)
- [Wikibase Summaries](#wikibase-summaries)
- [Conferences and workshops](#conferences-and-workshops)
- [Awesome Master and PhD theses](#awesome-master-and-phd-theses)
- [Wikibase-Wikidata papers](#wikibase-wikidata-papers)
- [Awesome Wikibase instances](#awesome-wikibase-instances)
- [Notes](#notes)

## Motivation

1. Given multiple unlinked datasets describing the same things ([entities](https://www.wikidata.org/wiki/Q35120)). 
2. Need for agile collaborative data integration ([Wikidata](https://www.wikidata.org)).
3. Need for a semantic layer in data/information/knowledge management in an organization.

## Awesome knowledge graphs

1. __Knowledge graphs__ by Aidan Hogan et al. [[preprint](https://arxiv.org/pdf/2003.02320.pdf)], [[HTML book](https://kgbook.org)]
2. __The Knowledge Graph Cookbook. Recipes that work__ by Andreas Blumauer & Helmut Nagy [[book](https://www.poolparty.biz/wp-content/uploads/2020/04/the-knowledge-graph-cookbook.pdf)]
3. __KIT Knowledge Graphs course__ by Harald Sack & Mehwish Alam [[description](https://open.hpi.de/courses/knowledgegraphs2020)]
4. __Stanford Knowledge Graphs course CS 520__ [[2020](https://web.stanford.edu/~vinayc/kg/2020/)], [[2021](https://web.stanford.edu/~vinayc/kg/2021/)]
5. __Knowledge Graphs - Foundations and Applications__ by Harald Sack [[description](https://open.hpi.de/courses/knowledgegraphs2023)]
6. __Knowledge Graphs: Methodology, Tools and Selected Use Cases__ Dieter Fensel et al [[book](https://www.knowledgegraphbook.ai/wp-content/uploads/2020/10/KnowledgeGraphBook.pdf)]

## Awesome Wikibase tutorials

1. __Programmer's guide to Wikibase__ [[guide](https://www.mediawiki.org/wiki/Wikibase/Programmer%27s_guide_to_Wikibase)]
2. __Wikibase: configure, customize, and collaborate__ by [Dan Scott](https://stuff.coffeecode.net/2018/wikibase-workshop-swib18.html) [[tutorial](https://stuff.coffeecode.net/2018/wikibase-workshop-swib18.html)]
3. __posts about [Wikibase](https://addshore.com/tag/wikibase) & [Wikidata](https://addshore.com/tag/wikidata/) and [Tech Lead Digests](https://addshore.com/tag/tech-lead/)__ by [Adam 'addshore' Shorland](https://addshore.com/about)
4. __Wikibase Install Basic Tutorial__ by [Matt Miller](https://thisismattmiller.com/about) [[tutorial](https://semlab.io/howto/wikibase_basic)]
5. __Wikibase for Research Infrastructure__ by [Matt Miller](https://thisismattmiller.com/about) [[post](https://medium.com/@thisismattmiller/wikibase-for-research-infrastructure-part-1-d3f640dfad34)]
6. __Vanderbilt Heard Library digital scholarship resources on Wikidata and Wikibase__ [[resources](https://heardlibrary.github.io/digital-scholarship/host/wikidata/)]
7. __Putting Data into Wikidata using Software__ by [Steve Baskauf](https://github.com/baskaufs) [[post](http://baskauf.blogspot.com/2019/06/putting-data-into-wikidata-using.html)]
8. [Learning Wikibase](http://learningwikibase.com)
9. __Get your own copy of WikiData__ by [Wolfgang Fahl](https://github.com/WolfgangFahl) [[post](http://wiki.bitplan.com/index.php/Get_your_own_copy_of_WikiData)]
10. __Transferring Wikibase data between wikis__ by [Jeroen De Dauw](https://www.EntropyWins.wtf) [[post](https://wikibase.consulting/transferring-wikibase-data-between-wikis)]
11. __Wikibase resources__ by Olaf Janssen & KB national library of the Netherlands [GitHub repo](https://github.com/KBNLwikimedia/Wikibase-resources)

## Wikibase Architecture

* [Architecture overview](https://www.mediawiki.org/wiki/Wikibase/Maintaining#Architecture_overview)
* [Wikibase Architecture Documentation](https://wmde.github.io/wikidata-wikibase-architecture/)

## Installing Wikibase

1. Manual installation of the [Wikibase Suite](https://www.mediawiki.org/wiki/Wikibase/Suite)
2. If you already have [Mediawiki](https://www.mediawiki.org/wiki/Manual:Installation_guide), install manually the [Wikibase extension](https://www.mediawiki.org/wiki/Wikibase/Installation)
3. ```docker-compose up -d``` of the [Wikibase Docker Image](https://www.mediawiki.org/wiki/Wikibase/Docker)
4. Obsolete: [WbStack](https://www.wbstack.com) as a part of the "Wikibase as a service". Ask an invitation from [Adam Shorland](https://addshore.com/contact)
5. [Wikibase Cloud](https://www.wikibase.cloud) is "Wikibase as a service".
6. [Ansible playbook](https://gitlab.com/nfdi4culture/ta5-knowledge-graph/wikibase-deploy) for Wikibase [[docs](https://gitlab.com/nfdi4culture/ta5-knowledge-graph/wikibase-process)]

## Data model

* [Conceptual data model](https://www.mediawiki.org/wiki/Wikibase/DataModel)
* [Simplified conceptual data model](https://www.mediawiki.org/wiki/Wikibase/DataModel/Primer)
* [RDF Dump Format](https://www.mediawiki.org/wiki/Wikibase/Indexing/RDF_Dump_Format)
* [Canonical PHP implementation of the Wikibase Data Model](https://github.com/wmde/WikibaseDataModel)
* [Wikibase DataModel Serialization](https://github.com/wmde/WikibaseDataModelSerialization)

## Data import

Before starting with data import please read the following resources:
* [Fast Bulk Import Into Wikibase](https://wikibase.consulting/fast-bulk-import-into-wikibase) by Jeroen De Dauw
* [A protocol for adding knowledge to Wikidata, a case report](https://doi.org/10.1101/2020.04.05.026336)
* [A protocol for adding knowledge to Wikidata: aligning resources on human coronaviruses](https://doi.org/10.1186/s12915-020-00940-y)

#### The Wikibase frontend

* Creating new items: Click __Special Pages__ on the left-hand menu and then __Create a new item__
* Creating new properties: Click __Special Pages__ on the left-hand menu and then __Create a new property__

#### The Wikibase API and wrappers

A recommended way to import data into a Wikibase instance is via the [Wikibase API](https://www.mediawiki.org/wiki/Wikibase/API/en). Many wrappers of the Wikibase API exist:
1. With Graphical User Interface (GUI)
   - [QuickStatements](https://github.com/magnusmanske/quickstatements) [[GUI](https://quickstatements.toolforge.org/#/)], [[Help](https://www.wikidata.org/wiki/Help:QuickStatements)]
   - [OpenRefine](https://github.com/OpenRefine/OpenRefine) [[homepage](https://openrefine.org)], [[docs](https://openrefine.org/documentation.html)]
2. With command Line Interface (CLI)
   - [wikibase-cli](https://github.com/maxlath/wikibase-cli) is a CLI interface to the JS modules [wikibase-edit](https://www.npmjs.com/package/wikibase-edit) and [wikibase-sdk](https://www.npmjs.com/package/wikibase-sdk)
3. Libraries
   - [Wikidata-Toolkit](https://github.com/Wikidata/Wikidata-Toolkit) is a Java library [[overview](https://www.mediawiki.org/wiki/Wikidata_Toolkit)]
   - [WikidataIntegrator](https://github.com/SuLab/WikidataIntegrator) is a Python library [[zenodo](https://doi.org/10.5281/zenodo.3621064)]
   - [wikibase-edit](https://github.com/maxlath/wikibase-edit) is a NodeJS library [[docs](https://github.com/maxlath/wikibase-edit/blob/master/docs/how_to.md)]
   - [WikibaseIntegrator](https://github.com/LeMyst/WikibaseIntegrator) is a Python library
   - [Pywikibot](https://github.com/wikimedia/pywikibot) is a Python library [[manual](https://www.mediawiki.org/wiki/Manual:Pywikibot)]

#### The Mediawiki MySQL database

An unrecommended way to import data into a Wikibase intance is via direct inserts into the MySQL database (MariaDB). Then, [Wikibase Query Updater](https://wikitech.wikimedia.org/wiki/Wikidata_Query_Service) sends data from MariaDB to the graph database Blazegraph. It is faster but more risky, because undesired inserts might happen by accident.
1. [wikibase-insert](https://github.com/jze/wikibase-insert) is a Java tool described in the [[FactGrid's post](https://blog.factgrid.de/archives/2013)]
2. [RaiseWikibase](https://github.com/UB-Mannheim/RaiseWikibase) is a Python tool described in [[preprint](https://openreview.net/pdf?id=87hp7LJDJE)], [[docs](https://ub-mannheim.github.io/RaiseWikibase/)], [[poster](https://ub-mannheim.github.io/RaiseWikibase/poster)]

## Federated Properties

Federated properties in Wikibase are still under development:
* Federated properties in Wikibase: [[docs](https://doc.wikimedia.org/Wikibase/master/php/md_docs_components_repo-federated-properties.html)]
* [Workboard at Phabricator](https://phabricator.wikimedia.org/project/view/4604/)

Current workaround is getting basic info about the properties from the Wikidata SPARQL endpoint and creating those properties locally:
* [WikidataIntegrator Notebook](https://github.com/SuLab/WikidataIntegrator/blob/main/notebooks/CreateWikidataProperties.ipynb) and its [parallel implementation](https://github.com/SuLab/WikidataIntegrator/blob/main/notebooks/CreateWikidataPropertiesParallel.ipynb)
* [miniWikibase.py](https://github.com/UB-Mannheim/RaiseWikibase/blob/main/miniWikibase.py) in [RaiseWikibase](https://github.com/UB-Mannheim/RaiseWikibase)
* [wikibase-tools](https://github.com/stuppie/wikibase-tools)

Every property is associated with a certain datatype in the Wikibase Data Model. Some of the datatypes are not native and require extensions. See:
* [Testing all datatypes](https://github.com/UB-Mannheim/RaiseWikibase#testing-all-datatypes)
* [issue T278674](https://phabricator.wikimedia.org/T278674)
* [Native and non-native datatypes](https://www.mediawiki.org/wiki/Wikibase/Suite#Native_and_non-native_data_types)

## Data Wrangling

* [OpenRefine](https://github.com/OpenRefine/OpenRefine) is a Java tool for working with messy data and for improving data [[homepage](https://openrefine.org)], [[docs](https://openrefine.org/documentation.html)]

## Data reconciliation

* __Wikibase reconciliation interface__ [[code](https://github.com/wetneb/openrefine-wikibase)], [[API](https://wikidata.reconci.link/en/api)], [[paper](http://ceur-ws.org/Vol-2773/paper-17.pdf)]
* [Reconciliation Service API: A protocol for data matching on the Web](https://reconciliation-api.github.io/specs/latest/)
* [testbench](https://github.com/reconciliation-api/testbench)

## Named Entity Linking

Named entity linking is widely used for creating and extending knowledge graphs.

### Texts

SOTA algorithms can be found at [paperswithcode](https://paperswithcode.com/task/entity-linking). 16 benchmarks are available.

* [GENRE & mGENRE](https://github.com/facebookresearch/GENRE) is a multilingual entity linker to Wikidata based on [BART](https://arxiv.org/abs/1910.13461) and [mBART](https://arxiv.org/abs/2001.08210), [[paper GENRE](https://arxiv.org/pdf/2010.00904.pdf)], [[paper mGENRE](https://arxiv.org/pdf/2103.12528.pdf)], [[examples GENRE](https://github.com/facebookresearch/GENRE/tree/main/examples_genre)], [[examples mGENRE](https://github.com/facebookresearch/GENRE/tree/main/examples_mgenre)]
* [BLINK](https://github.com/facebookresearch/BLINK) links entities to Wikipedia based on fine-tuned BERT, links to Wikidata are obtained for free from Wikipedia [[paper](https://arxiv.org/pdf/1911.03814.pdf)], [[see a fork](https://github.com/TheScienceMuseum/BLINK)]
* [entity-fishing](https://github.com/kermitt2/entity-fishing) is a named entity linker on Wikidata [[demo](https://cloud.science-miner.com/nerd)], [[docs](http://nerd.readthedocs.io)], [[presentation](https://grobid.s3.amazonaws.com/presentations/29-10-2017.pdf)]
* [spacyfishing](https://github.com/Lucaterre/spacyfishing) is a spaCy wrapper for entity-fishing
* [OpenTapioca](https://github.com/wetneb/opentapioca) is a real-time entity linker to Wikidata [[live demo](https://opentapioca.org)], [[paper](https://arxiv.org/pdf/1904.09131.pdf)], [[docs](https://opentapioca.readthedocs.io/en/latest/)]
* [Spacy Entity Linker](https://github.com/egerber/spaCy-entity-linker) is a simple experimental NELinker to Wikidata using queries to a local database
* [spaCyOpenTapioca](https://github.com/UB-Mannheim/spacyopentapioca) is a spaCy pipeline for OpenTapioca [[spaCy Universe](https://spacy.io/universe/project/spacyopentapioca)]
* [Survey on English Entity Linking on Wikidata](http://www.semantic-web-journal.net/system/files/swj2865.pdf) is a survey paper
* [falcon2.0](https://github.com/SDM-TIB/falcon2.0) is a joint entity and relation linking tool over Wikidata [[demo](https://labs.tib.eu/falcon/falcon2)], [[paper](https://arxiv.org/pdf/1912.11270.pdf)]

### Tables

SOTA algorithms at Wikidata were tested at [SemTab 2020: Semantic Web Challenge on Tabular Data to Knowledge Graph Matching](https://www.cs.ox.ac.uk/isg/challenges/sem-tab/2020/) and [SemTab 2021](https://www.cs.ox.ac.uk/isg/challenges/sem-tab/2021/):

* [MTab](https://github.com/phucty/mtab_tool) is the best algorithm for semantic table interpretation [[online demo & APIs](https://mtab.app)], [[paper](http://ceur-ws.org/Vol-2775/paper9.pdf)]
* [bbw](https://github.com/UB-Mannheim/bbw) is based on meta-lookup (metasearch over SearX) [[docs](https://ub-mannheim.github.io/bbw/)], [[paper](http://ceur-ws.org/Vol-2775/paper2.pdf)]
* [JenTab](https://github.com/fusion-jena/JenTab) is a modular tool [[paper](http://ceur-ws.org/Vol-2775/paper4.pdf)]
* [MantisTable 4](https://bitbucket.org/disco_unimib/mantistable-4/src/master/) is a tool with advanced GUI [[paper](http://ceur-ws.org/Vol-2775/paper8.pdf)]

See also: 

* [table-linker](https://github.com/usc-isi-i2/table-linker) is an entity linkage tool which links the given string to Wikidata Q nodes [[table-linker-pipelines](https://github.com/usc-isi-i2/table-linker-pipelines)]

## Data validation

The first mechanism is using constraints:
* [Extension:WikibaseQualityConstraints](https://www.mediawiki.org/wiki/Extension:WikibaseQualityConstraints)
* For Wikidata see [Help:Property constraints portal](https://www.wikidata.org/wiki/Help:Property_constraints_portal)

The second mechanism is using Entity Schemas and Shape Expressions (ShEx).
* [Extension:EntitySchema](https://www.mediawiki.org/wiki/Extension:EntitySchema)
* For Wikidata see [Wikidata: Schemas](https://www.wikidata.org/wiki/Wikidata:Schemas) and [Wikidata:WikiProject Schemas](https://www.wikidata.org/wiki/Wikidata:WikiProject_Schemas)

Tools for entity schemas:
* [WikiShape](https://wikishape.weso.es) is a playground (vizualization, querying, validation & extraction) customized for Wikibase instances [[code](https://github.com/weso/wikishape)]
* [Wikidata Shape Expressions Inference](https://wd-shex-infer.toolforge.org) is a tool for automatic inference of ShEx schemas from a set items [[code](https://phabricator.wikimedia.org/source/tool-wd-shex-infer/)]
* [sheXer](http://shexer.weso.es) is an automatic inference of ShEx schemas from a set of items [[code](https://github.com/DaniFdezAlvarez/shexer)]
* [YASHE](https://www.weso.es/YASHE/) is a ShEx editor [[code](https://github.com/weso/YASHE)]
* [ShExStatements](https://shexstatements.toolforge.org) is a tool for simplified writing the shape expressions in Wikidata [[paper](https://wikiworkshop.org/2021/papers/Wiki_Workshop_2021_paper_14.pdf)], [[code](https://github.com/johnsamuelwrites/ShExStatements)]
* [ShEx2](https://rawgit.com/shexSpec/shex.js/wikidata/packages/shex-webapp/doc/shex-simple.html) (aka shex.js) is a simple online validator [[code](https://github.com/shexSpec/shex.js/tree/v0.9.2)], [[zenodo](http://doi.org/10.5281/zenodo.1213693)]
* [RDFShape](https://rdfshape.weso.es) is a general RDF playground for data validation and conversion between semantic formats [[paper](http://ceur-ws.org/Vol-2180/paper-35.pdf)]
* [PyShExy](https://tools-static.wmflabs.org/pyshexy/) is an API to validate RDF entities against ShEx schemas using PyShEx

Relevant papers:
* [Using Shape Expressions (ShEx) to Share RDF Data Models and to Guide Curation with Rigorous Validation](https://doi.org/10.1007/978-3-030-21348-0_39)
* [Using logical constraints to validate information in collaborative knowledge graphs: a study of COVID-19 on Wikidata](https://doi.org/10.5281/zenodo.4008358)
* [Creating Knowledge Graphs Subsets using Shape Expressions](https://arxiv.org/pdf/2110.11709.pdf)

## Wikibase Ecosystem

* [Strategy for the Wikibase Ecosystem 2019](https://upload.wikimedia.org/wikipedia/commons/c/cc/Strategy_for_Wikibase_Ecosystem.pdf)
* [Strategy for the Wikibase Ecosystem 2021](https://meta.wikimedia.org/wiki/LinkedOpenData/Strategy2021/Wikibase)
* [Wikibase Registry](https://wikibase-registry.wmflabs.org)

## Wikibase Community

* [Wikibase Community User Group](https://meta.wikimedia.org/wiki/Wikibase_Community_User_Group)
* [Wikibase Live Sessions](https://meta.wikimedia.org/wiki/Category:Wikibase_Community_User_Group/Meetings)
* [Wikibase Stakeholder Group](https://wbstakeholder.group)

## Wikibase Summaries

* [Wikibase Yearly Summary 2020](https://www.lehir.net/wikibase-yearly-summary-2020)
* [Wikibase Yearly Summary 2021](https://www.lehir.net/wikibase-yearly-summary-2021)
* [Wikibase Yearly Summary 2022](https://www.lehir.net/wikibase-yearly-summary-2022)

## Conferences and workshops

* [The first Federated-Wikibase-Workshop: Antwerp, 2018-04-23/25](https://blog.factgrid.de/archives/835)
* [Wikibase Workshop in Berlin, 2018](https://blog.wikimedia.de/2018/07/13/wikibase-workshop-in-berlin)
* [The Wikibase Summit: New York, 2018](https://www.wikidata.org/wiki/Wikidata:WikiProject_Wikidata_for_research/Meetups/2018-09-19-21-New-York)
* [Ghent University Wikidata and Wikibase Workshop 2019](https://www.wikidata.org/wiki/Wikidata:Events/Belgium/Universiteit_Gent/Wikidata_and_Wikibase_Workshop/2019)
* [Wikidata Workshop 2020](https://wikidataworkshop.github.io/2020/) [[papers](http://ceur-ws.org/Vol-2773)]
* [Wikidata Workshop 2021](https://wikidataworkshop.github.io/2021/) [[papers](http://ceur-ws.org/Vol-2982)]
* [Wikidata Workshop 2022](https://wikidataworkshop.github.io/2022/) 

## Awesome Master and PhD theses

* __Schema Inference on Wikidata__ by Lucas Werkmeister [[thesis](https://doi.org/10.5281/zenodo.2578258)]
* __Modelling and Importing Dynamic Data into Wikibase: A Case Study of the Swiss Transportation System__ by Samuel Meuli [[thesis](https://www.merlin.uzh.ch/contributionDocument/download/12658)]

## Wikibase-Wikidata papers

1. Fudie Zhao, A systematic review of Wikidata in Digital Humanities projects, Digital Scholarship in the Humanities, Volume 38, Issue 2, June 2023, Pages 852–874, https://doi.org/10.1093/llc/fqac083
2. Tharani, Karim. "Much more than a mere technology: A systematic review of Wikidata in libraries." The Journal of Academic Librarianship 47.2 (2021): 102326. https://doi.org/10.1016/j.acalib.2021.102326
3. Waagmeester, A., Stupp, G., Burgstaller-Muehlbacher, S., Good, B. M., Griffith, M., Griffith, O. L., ... & Su, A. I. (2020). Wikidata as a knowledge graph for the life sciences. Elife, 9, e52614. https://doi.org/10.7554/eLife.52614
4. Nielsen, F.Å., Mietchen, D., Willighagen, E. (2017). Scholia, Scientometrics and Wikidata. In: Blomqvist, E., Hose, K., Paulheim, H., Ławrynowicz, A., Ciravegna, F., Hartig, O. (eds) The Semantic Web: ESWC 2017 Satellite Events. ESWC 2017. Lecture Notes in Computer Science(), vol 10577. Springer, Cham. https://doi.org/10.1007/978-3-319-70407-4_36
5. Turki, H., Shafee, T., Taieb, M.A.H., Aouicha, M.B., Vrandečić, D., Das, D. and Hamdi, H., 2019. Wikidata: A large-scale collaborative ontological medical database. Journal of Biomedical Informatics, 99, p.103292. https://doi.org/10.1016/j.jbi.2019.103292

## Awesome Wikibase instances

1. [Wikidata](https://www.wikidata.org) is a general-purpose Wikibase knowledge graph [[SPARQL](https://query.wikidata.org)]
2. [Wikibase Registry](https://wikibase-registry.wmflabs.org) is a Wikibase knowledge graph of Wikibase knowledge graphs [[SPARQL](https://wikibase-registry-query.wmflabs.org)], [[timeline of Wikibase instances](https://wikibase-registry-query.wmflabs.org/#%23defaultView%3ATimeline%0ASELECT%20%3Fitem%20%3FitemLabel%20%3FcreationDate%20%28SAMPLE%28%3Flogo%29%20AS%20%3Fimage%29%0AWHERE%0A%7B%0A%20%20%20%20%3Fitem%20wdt%3AP11%20wd%3AQ20%20.%0A%20%20%20%20%3Fitem%20wdt%3AP5%20%3FcreationDate%20.%0A%09SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22%20%7D%0A%20%20%20%20OPTIONAL%20%7B%20%3Fitem%20wdt%3AP8%20%3Flogo%20%7D%0A%7D%0AGROUP%20BY%20%3Fitem%20%3FitemLabel%20%3FcreationDate)]
3. [Rhizome Artbase](https://artbase.rhizome.org) is a Wikibase knowledge graph of born-digital artworks from 1999 to the present day [[SPARQL](https://query.artbase.rhizome.org)]
4. [FactGrid](https://database.factgrid.de) is a Wikibase knowledge graph for historical research [[SPARQL](https://database.factgrid.de/query/)], [[Viewer](https://database.factgrid.de/viewer/)], [[fast search via ringgaard.com](https://factgrid.ringgaard.com/kb)]
5. [Lingua Libre](https://lingualibre.org) is a Wikibase knowledge graph of audiovisual data [[SPARQL](https://lingualibre.org/bigdata/#query)]
6. [OpenStreetMap Metadata](https://wiki.openstreetmap.org/wiki/Data_items) is a Wikibase knowledge graph of metadata in [OpenStreetMap](https://www.openstreetmap.org) [[SPARQL](https://sophox.org)]
7. [PersonalData.io](https://wiki.personaldata.io) is a Wikibase knowledge graph about personal data ecosystem [[SPARQL](https://query.personaldata.io)]
8. [EU knowledge graph](https://linkedopendata.eu) is a Wikibase knowledge graph about European Union [[SPARQL](https://query.linkedopendata.eu)], [[Question-Answering over KG](https://qa.linkedopendata.eu)], [[paper at ISWC2021 "Wikibase as an Infrastructure for Knowledge Graphs: the EU Knowledge Graph"](https://hal.archives-ouvertes.fr/hal-03353225/document)]
9. [enslaved.org](https://lod.enslaved.org) is a Wikibase knowledge graph about people of the historical slave trade [[frontend](https://enslaved.org)]
10. [Semlab Wikibase](http://base.semlab.io) is a Wikibase knowledge graph of [Semantic Lab at Pratt Institute](https://semlab.io) with data about [their research projects](https://semlab.io/projects) [[SPARQL](https://query.semlab.io)]
11. [Virus-Taxonomy](https://virus-taxonomy.wiki.opencura.com) is a Wikibase knowledge graph of virus taxonomy [[SPARQL](https://virus-taxonomy.wiki.opencura.com/query/)]
12. [DataTrek](https://data.wikitrek.org) is a Wikibase knowledge graph of open data for Star Trek 
13. [Nonbinary](https://data.nonbinary.wiki) is a Wikibase knowledge graph of concepts relevant to nonbinary identities
14. [The De Jonge Wiki](https://set.kuleuven.be/rlicc/dejongewiki/w/index.php/Main_Page) is a Wikibase knowledge graph of research that has been carried out on the [Arenberg Castle](https://set.kuleuven.be/rlicc/dejongewiki/w/index.php/Arenberg_Castle)
15. [Biblissima](https://data.biblissima.fr/w/Accueil) is a Wikibase knowledge graph of the Biblissima authority repositories
16. [Standartopedia](https://standartopedia.ru) is a Wikibase knowledge graph of Russian legal norms and requirements of standards 
17. [DataCegeSoma](https://adochs.arch.be) is a Wikibase knowledge graph of authority data for [CegeSoma](https://www.cegesoma.be) / [State Archives in Belgium](http://arch.arch.be) created by [Anne Chardonnens](https://linkingthepast.org/about) as a part of her PhD thesis [[SPARQL](https://query-adochs.arch.be)]
18. [MaRDi portal](https://portal.mardi4nfdi.de) is a Wikibase knowledge graph of mathematical research data [[SPARQL](https://query.portal.mardi4nfdi.de)]
19. [MiMoTextBase](https://data.mimotext.uni-trier.de) is a Wikibase knowledge graph of the French Enlightenment novel [[SPARQL](https://query.mimotext.uni-trier.de)] [[MiMoText Project](https://mimotext.github.io/MiMoTextBase_Tutorial/)] [[Tutorial](https://mimotext.github.io/MiMoTextBase_Tutorial/tutorial_index.html)]
20. [EURHISFIRM](http://data.eurhisfirm.eu) is a sandbox Wikibase knowledge graph of historical high-quality firm level data for Europe [[SPARQL](http://data.eurhisfirm.eu:8282)], [[GitLab](https://gitlab.huma-num.fr/eurhisfirm)]
21. [Aktienführer](https://akf.kgi.uni-mannheim.de) is a Wikibase knowledge graph of the German listed stock companies from the Hoppenstedt-Aktienführer from 1956 to 2018 [[SPARQL](https://query.akf.kgi.uni-mannheim.de)]

More Wikibase instances can be found at [Wikibase Registry](https://wikibase-registry.wmflabs.org) and [WikiAPIary](https://www.wikiapiary.com/w/index.php?title=Special:Ask&offset=0&limit=500&q=%5B%5BHas+extension%3A%3AExtension%3AWikibaseRepository%5D%5D&p=mainlabel%3D-2D%2Fformat%3Dtable%2Flink%3Dall%2Fheaders%3Dshow%2Fintro%3D-3Cb-3EThis-20extension-20is-20in-20use-20on-20the-20following-20websites%3A-3C-2Fb-3E-3Cbr-20-2F-3E%2Fsearchlabel%3D%E2%80%A6-20further-20results%2Fdefault%3DThis-20extension-20is-20no-20longer-20in-20use-20on-20any-20website.%2Fclass%3Dsortable-20wikitable-20smwtable&po=%3FHas+website%3DWiki+name%0A%3FHas+MediaWiki+version%3DMediaWiki+version%0A%3FHas+extension+version%3DExtension+version%0A&sort=Has+website&order=rand).

## Notes

The initial version of this repo is based on the slides [Wikibase knowledge graphs for data management & data science](https://madoc.bib.uni-mannheim.de/59865/1/Shigapov_Wikibase_Knowledge_Graphs.pdf) presented at [Data Literacy Snacks 2021](https://www.berd-bw.de/snacks/).
