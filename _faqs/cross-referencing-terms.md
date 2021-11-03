---
title: "How to make Confluence pages searchable using both preferred and alternative terms?"
description: "Explains how to make a Confluence page or blog post searchable by preferred and alternative terms or identifiers such as product codes with Taxonomies for Confluence add-on."
featured: true
weight: 2
layout: page
---

In cases where several user groups use different terms to refer to the same concept, adopt controlled vocabulary - dictionary, taxonomy or thesaurus - that includes preferred and alternative labels, and identifiers such as product or industry classification codes. Integrate controlled vocabulary with Confluence using [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on. Insert concepts into Confluence pages and blog posts to make them searchable by preferred and alternative labels as well as the identifier.

* Start with creating or adopting existing controlled vocabularies, taxonomies or thesauri using [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/). 
* Specify preferred label (`skos:prefLabel`), alternative labels (`skos:altLabel`), and, if needed, common identifiers (`skos:notation`).
* Install [Taxonomies for Confluence](https://marketplace.atlassian.com/apps/1226218/taxonomies-for-confluence) add-on.
* Insert related concepts into Confluence pages or blog posts with Related Concept macro - search for Related Concept macro to insert, search for a concept using its preferred or alternative label or the identifier, select the appropriate one and click Insert. 
* You can now find Confluence content by preferred and alternative labels and the identifier.

![The Confluence page shows the name of the referenced ASX listed company. Find the page by either company name or the ASX ticker.](/images/tfc-faq/cross-referencing-terms-image.png "The Confluence page shows the name of the referenced ASX listed company. Find the page by either company name or the ASX ticker.")