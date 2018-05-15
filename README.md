# *NB: Open work-in-progess.*

# Analysing AI and Deep Learning from ArXiv data 

Some text about what this is

## Datasets

[Matched academic data, with CorEx topics](https://s3.eu-west-2.amazonaws.com/nesta-open-data/arxiv_ai/corex_matched.json) (the output of `step4-grid_and_final_match.ipynb`)

[Analysis outputs](not-implemented-yet) (the output of `step5-analysis.ipynb`)


## Data dictionary

| Field name  | Field description | Value type:description (if required) | 
| ----------- | ----------------- | ----------------- |
| TOPIC_&ast; | Topics of the paper generated by a nominal topic modelling algorithm. Topic keywords are separated by underscores, and ngrams are separated by white space. | float: A weight of this topic in this paper. |
| arxiv_categories | Categories as listed on arXiv. | list: Category names. |
| arxiv_created | Date created on arXiv. | int: Seconds since the epoch. |
| arxiv_id | arXiv oai ID. | str: |
| arxiv_raw_summary | Paper summary as described on arXiv. | str: |
| arxiv_raw_title | Paper title as written on arXiv. | str: |
| arxiv_summary | arxiv_raw_summary with some preprocessing. | list: |
| arxiv_title | arxiv_title with some preprocessing. | list: |
| grid_lat | Latitudes of institutes from GRID database. | list: Each index-wise element in the list has a corresponding value in grid_lon. Multiple values may occur if a matching location is multinational. Values can be NaN if this is listed in GRID. |
| grid_lon | Longitudes of institutes from GRID database. | list: Each index-wise element in the list has a corresponding value in grid_lat. Multiple values may occur if a matching location is multinational. Values can be NaN if this is listed in GRID. |
| mag_arxiv_sources | The arXiv source as described in MAG. | list: |
| mag_citations | Number of citations as described by MAG. | int: |
| mag_date |  Date of publication as described by MAG. | str: |
| mag_full_title | Full title of publication as described by MAG.  | str: |
| mag_institutes | Institute affiliations of authors as described by MAG. | list: |
| mag_journal | Journal of publication as described by MAG. | str: |
| mag_language | Publication language as described by MAG. | str: |
| mag_matched | Was this paper matched to OAG? | bool: |
| mag_title | Shortened title of publication as described by MAG. | str: |
| match_score | Fuzzy matching score between MAG and GRID data. | float: Between 0.85 and 1. Anything less than 0.95 could be suspicious (although a small number of scores of 1 are also false matches). |
| match_value | The matching institute name from GRID. | str: |
| oag_abstract | The publication abstract as described by OAG. | str: |
| oag_doc_type | The publication type as described by OAG. | str: |
| oag_doi | The publication DOI as described by OAG. | str: |
| oag_fos | The fields of study as described by OAG. | list: |
| oag_id | The OAG ID. | str: |
| oag_issue | The publication issue number as described by OAG. | float: |
| oag_keywords | The fields of study as described by OAG. | list: |
| oag_lang | The publication language as described by OAG. | str: |
| oag_n_citation | Number of citations as described by OAG. | float: |
| oag_publisher | Journal publisher as described by OAG.  | str: |
| oag_references | Reference as described by OAG. | list: |
| oag_title | Title of publication as described by OAG. | str: |
| oag_url | URL of publication as described by OAG.  | list: |
| oag_venue | Venue of conference as described by OAG. | str: |
| oag_volume | Volume of journal publication as described by OAG. | float: |
| oag_year | Year of journal publication as described by OAG. | int: |



## Papers & Blogs

Links to papers and blogs

## Code

How to run this analysis yourself

## References

https://www.grid.ac/

Jie Tang, Jing Zhang, Limin Yao, Juanzi Li, Li Zhang, and Zhong Su. ArnetMiner: Extraction and Mining of Academic Social Networks. In Proceedings of the Fourteenth ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (SIGKDD'2008). pp.990-998. [PDF] [Slides] [System] [API]

Arnab Sinha, Zhihong Shen, Yang Song, Hao Ma, Darrin Eide, Bo-June (Paul) Hsu, and Kuansan Wang. 2015. An Overview of Microsoft Academic Service (MAS) and Applications. In Proceedings of the 24th International Conference on World Wide Web (WWW ’15 Companion). ACM, New York, NY, USA, 243-246.
