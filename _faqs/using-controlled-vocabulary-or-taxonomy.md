---
title: "How to use existing controlled vocabulary, taxonomy or thesaurus with Confluence?"
description: "Explains how to use Taxonomies for Confluence add-on to reuse existing controlled vocabulary, taxonomy or thesaurus, such as industry classification scheme, to tag and search for Confluence pages and blog posts."
weight: 1
layout: page
---

Labels may be suitable in situations where terms evolve quickly, and you are happy to live with the resulting folksonomy. In cases where you intend to manage terms tightly, however, integrate controlled vocabulary, taxonomy or thesaurus with Confluence using [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on.

* Start with creating or adopting existing controlled vocabularies, taxonomies or thesauri built with [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/).
* Install [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on.
* Navigate to the Taxonomies Admin page and import the files - RDF/XML, N-Triples, Turtle, Turtle-star, N3/Notation3, TriX, TriG, TriG-star, binary RDF, N-Quads, JSON-LD, RDF/JSON and HDT formats are supported. Taxonomies you can readily use include [Australian and New Zealand Standard Industrial Classification (ANZSIC)](https://github.com/cadmiumkitty/anzsic-taxonomy), [TOGAF® Content Metamodel Vocabulary](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology), [APRA CPG 235 Taxonomy for manaring data risk](https://github.com/cadmiumkitty/cpg235-taxonomy) and more.
* Specify the subject of the Confluence page or blog post using Subject Byline - click on the subject byline, search for a concept among the ones imported using preferred or alternative labels or identifier, and select the appropriate one to set the subject.
* Insert related concept into the Confluence page or blog post with Related Concept macro - search for Related Concept macro to insert, search for a concept, select the appropriate one and click Insert.
* Build a table of contents with About and Related macro - search for About and Related macro to insert, build criteria using the query builder and click Insert.
* Navigate to the Taxonomies page to explore imported controlled vocabularies, taxonomies or thesauri, along with Confluence pages or blog posts about or related to particular concepts.

![Using ANZSIC, APRA Data Quality Dimensions and custom investment capabilities taxobnomy for human-readable documentation on Confluence](/images/tfc-faq/using-controlled-vocabulary-or-taxonomy-image.png "Using ANZSIC, APRA CPG 235 Data Quality Dimensions and custom investment capabilities taxonomy for human-readable data quality controls documentation on Confluence.")