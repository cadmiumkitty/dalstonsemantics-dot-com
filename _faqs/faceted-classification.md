---
title: "How to do faceted classification in Confluence?"
description: "Explains how to use multiple taxonomy concepts and Taxonomies for Confluence add-on to implement faceted classification for Confluence pages and blog posts."
weight: 3
layout: page
---

You often need to classify Confluence content - pages and blog posts - along several dimensions. For example, when using Confluence to manage definitions of data quality controls, you may want to classify each Control page by data quality dimension, data being at rest or in transit, type of data container, and so on. Confluence labels may suffice in the most straightforward cases but not when the number of concepts grows (think classifying pages by industry, as even relatively short [ANZSIC](https://github.com/cadmiumkitty/anzsic-taxonomy) has over 800 concepts), or several user groups use different terms to refer to the same concept. In these cases, consider creating or adopting several corporate taxonomies, each for every dimension used for classification, integrate them with Confluence using [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on and start inserting as many concepts as required for classification into Confluence pages or blog posts.

* Start with creating or adopting existing controlled vocabularies - dictionaries, taxonomies or thesauri - using [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/), one for every classification dimension. Depending on the use case, you can use single taxonomy with multiple top concepts (`skos:topConceptOf` or `skos:hasTopConcept`) or create multiple taxonomies.
* Install [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on.
* Insert concepts into Confluence pages or blog posts with Related Concept macro - search for Related Concept macro to insert, search for a concept using its preferred or alternative label or the identifier, select the appropriate concept and click Insert.
* Repeat for each of the classification dimensions.
* Search for Confluence content and build the table of contents using a combination of these concepts.

![Using Taxonomy for Policy and Data Criticality Taxonomy to manage data quality controls documentation in Confluence](/images/tfc-faq/faceted-classification.png "Using Taxonomy for Policy and Data Criticality Taxonomy to manage data quality controls documentation in Confluence.")