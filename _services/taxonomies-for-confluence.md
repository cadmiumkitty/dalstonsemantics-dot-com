---
title: "Taxonomies for Confluence"
description: "Taxonomies for Confluence user guide describing how to import Simple Knowledge Organization System (SKOS) controlled vocabularies, taxonomies and thesauri into Confluence, say what pages are about and related to, and track alignment of Confluence content with capability models, data classifications, control taxonomies and other hierarchies."
featured: true
weight: 1
---

Increase the value of your investment in [Confluence](https://www.atlassian.com/software/confluence) by using it for enterprise architecture, data governance, regulatory compliance, risk management and more. Import [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/) controlled vocabularies, taxonomies and thesauri developed internally, by regulators or standards-setting organisations. Index Confluence pages and track alignment with capability models, data classifications, control taxonomies and other hierarchies without complex and expensive specialised tools.

## Challenge

Organisations taking on the development of enterprise architecture, implementation of data governance or regulatory compliance may opt for expensive specialised software and neglect tools such as Atlassian Confluence and Jira that they already have in place.

## Taxonomies for Confluence

### Getting started

Start with the development or adoption of an existing controlled vocabulary, taxonomy or thesaurus using SKOS.

For example, when developing enterprise architecture you may start with building a common vocabulary of terms such as Business Capability and Business Service (here's [TOGAF 9.2 terms](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology) as an inspiration) and developing a taxonomy of business capabilities of your organisation (here's an example of [Investment Management Capabilities](https://github.com/cadmiumkitty/imc-taxonomy)). Similarly, you can build taxonomies from regulatory rulebooks when working on compliance projects (here's [taxonomy derived from APRA CPG 235 - Managing Data Risk](https://github.com/cadmiumkitty/cpg235-taxonomy)).

### Import SKOS concept schemes

Once Taxonomies for Confluence add-on is installed, new **Taxonomies** menu is added to the **Settings** page that is available to Confluence administrators. It lets you import developed or adopted SKOS taxonomies and use them with Confluence.

Select **Taxonomies** to navigate to the taxonomies settings page.

![Import SKOS taxonomies](/images/tfc/1.png "When no taxonomies are imported, a prompt to import a taxonomy is displayed.")

To import SKOS vocabulary, taxonomy or thesaurus click **Upload SKOS taxonomy file** button and select the file. [RDF/XML](http://www.w3.org/TR/rdf-syntax-grammar/), [N-Triples](http://www.w3.org/TR/n-triples/), [Turtle](https://www.w3.org/TR/turtle/), Turtle-star, [N3/Notation3](http://www.w3.org/TeamSubmission/n3/), [TriX](http://swdev.nokia.com/trix/), [TriG](http://www.w3.org/TR/trig/), TriG-star, [binary RDF](http://rivuli-development.com/2011/11/binary-rdf-in-sesame/), [N-Quads](http://www.w3.org/TR/n-quads/), [JSON-LD](http://www.w3.org/TR/json-ld/), [RDF/JSON](http://www.w3.org/TR/rdf-json/), [RDFa](http://www.w3.org/TR/rdfa-syntax/) and [HDT](http://www.rdfhdt.org/hdt-binary-format/) formats are supported detected from the file extension. The upload will start automatically once the file is selected. When the upload completes, an updated list of taxonomies is displayed. You can explore their structure by expanding concept schemes to reveal top concepts, and expanding concepts to reveal narrower concepts and Confluence content.

![Explore SKOS imported taxonomies](/images/tfc/2.png "When one or more taxonomies are imported, you can explore their structure by expanding concept schemes to reveal top concepts, and expanding concepts to reveal narrower concepts and Confluence content.")

### Index Confluence pages

Once Taxonomies for Confluence add-on is installed, new **Subject** byline and **Related Concept** macro are made available to Confluence users. It lets you index Confluence pages and blog posts using imported SKOS concepts and track their alignment to imported taxonomies.

#### Selecting SKOS concept as the subject of a page or a blog post

Click on the **Subject** byline, search for and click on the concept to index the page.

![Index Confluence Pages](/images/tfc/6.png "Expanded Subject Byline showing concepts matching the search for the role. TOGAF Role concept is selected as the subject of the page.")

#### Inserting related SKOS concept into a page or a blog post

Start typing `/related` anywhere in the body of the page and pick **Related Concept** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **Related Concept** from the Macro menu at the top.

![Index Confluence Pages](/images/tfc/7.png "Related Concept macro is being selected from the list of macros.")

Search for the concept to insert and select the concept from the search results.

![Index Confluence Pages](/images/tfc/11.png "Related Concept macro showing concepts matching the search for data quality. APRA CPG 235 Data Quality concept is selected to be inserted into the page.")

Click **Insert** to insert the relation. Once relation is inserted, the URI of the concept, `skos:prefLabel`, `skos:altLabel` and `skos:notation` can be used in Confluence search.

![Index Confluence Pages](/images/tfc/13.png "APRA CPG 235 Data Quality concept is inserted into the Confluence page.")

### Track alignment and gaps

Once Taxonomies for Confluence add-on is installed, the new **Taxonomies** App and **About and Related** macro are made available to Confluence users. They let you track the alignment of Confluence pages and blog posts to controlled vocabularies, taxonomies and thesauri developed internally, by regulators or standards-setting organisations.

#### Navigating taxonomies

Select **Taxonomies** item from the **Apps** menu to navigate to the taxonomies page.

![Taxonomies menu item](/images/tfc/22.png "Taxonomies item is being selected from the Confluence Apps menu.")

Expand concepts to see narrower concepts or pages and blog posts that are about or related to these concepts.

![Track Alignment](/images/tfc/23.png "Taxonomies page showing imported SKOS concept schemes. APRA CPG 235 concept scheme is expanded to reveal top concepts, narrower concepts of Data and data risk concept, and narrower concepts and related Confluence content of the Data quality concept.")

#### Inserting table of contents that are about or related to taxonomy concepts

Start typing `/about` anywhere in the body of the page where you want to insert the table of contents and pick **About and Related** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **About and Related** from the Macro menu at the top.

![Insert Table of Contents](/images/tfc/14.png "About and Related macro is being selected from the list of macros.")

Build a set of criteria for pages and blog posts to be included in the table of contents by selecting whether a concept is a subject or a relation of a page or blog post, and specifying whether narrower concepts need to be included.

![Insert Table of Contents](/images/tfc/16.png "About and Related macro editor to specify criteria for the table of contents that is about or related to concepts.")

For example, if you imported [TOGAF 9.2](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology) and [CPG 235](https://github.com/cadmiumkitty/cpg235-taxonomy) taxonomies and indexed Confluence pages with concepts from these taxonomies, creating the table of contents that includes pages about Roles related to Data Quality requires the following set of criteria:

![Insert Table of Contents](/images/tfc/19.png "About and Related macro editor with criteria specified to include Confluence pages and blog posts about TOGAF Role concept and related to APRA CPG 235 Data Quality concept.")

Click **Insert** to insert the table of contents.

![Insert Table of Contents](/images/tfc/21.png "Table of Confluence content about TOGAF Role concept and related to APRA CPG 235 Data Quality concept is inserted.")

### Use CQL for reporting and integration

Once Taxonomies for Confluence add-on is installed, three additional properties become available in Confluence pages and blog posts: `subjectUri` (populated with the URI of SKOS concept), `subjectPrefLabel` (populated from `skos:prefLabel`) and `subjectNotation` (populated from `skos:notation`). These properties can be used in CQL queries allowing you to integrate content or implement reporting using Confluence APIs.

For example, you can use [ANZSIC](https://www.abs.gov.au/ausstats/abs@.nsf/Latestproducts/1292.0Search12006%20(Revision%202.0)) codes in CQL search.

Request:

```
GET https://dalstonsemantics.atlassian.net/wiki/rest/api/search?cql=subjectNotation=0806&limit=25
```

Response:

```
{
  "results": [
    {
      "content": {
        "id": "1194950668",
        "type": "page",
        "status": "current",
        "title": "BHP",
        "childTypes": {},
        "macroRenderedOutput": {},
        "restrictions": {},
        "_expandable": {
          "container": "",
          "metadata": "",
          "extensions": "",
          "operations": "",
          "children": "",
          "history": "/rest/api/content/1194950668/history",
          "ancestors": "",
          "body": "",
          "version": "",
          "descendants": "",
          "space": "/rest/api/space/FI"
        },
        "_links": {
          "webui": "/spaces/FI/pages/1194950668/BHP",
          "self": "https://dalstonsemantics.atlassian.net/wiki/rest/api/content/1194950668",
          "tinyui": "/x/DIA5Rw"
        }
      },
      "title": "BHP",
      "excerpt": "BHP, formerly known as BHP Billiton, is the trading entity of BHP Group Limited and BHP Group plc, an Anglo-Australian multinational mining, metals and petroleum dual-listed public company headquartered in Melbourne, Victoria, Australia.\nThe Broken Hill Proprietary Company was founded on 16 July 1885 in the mining town",
      "url": "/spaces/FI/pages/1194950668/BHP",
      "resultGlobalContainer": {
        "title": "Fixed Income",
        "displayUrl": "/spaces/FI"
      },
      "breadcrumbs": [],
      "entityType": "content",
      "iconCssClass": "aui-iconfont-page-default",
      "lastModified": "2021-09-22T17:36:48.000Z",
      "friendlyLastModified": "Sep 22, 2021",
      "score": 0.0
    }
  ],
  "start": 0,
  "limit": 25,
  "size": 1,
  "totalSize": 1,
  "cqlQuery": "subjectNotation=0806",
  "searchDuration": 61,
  "_links": {
    "base": "https://dalstonsemantics.atlassian.net/wiki",
    "context": "/wiki",
    "self": "https://dalstonsemantics.atlassian.net/wiki/rest/api/search?cql=subjectNotation=0806"
  }
}
```

The excerpt above is from [Wikipedia BHP](https://en.wikipedia.org/wiki/BHP) article and is used under [Creative Commons Attribution-ShareAlike License](https://en.wikipedia.org/wiki/Wikipedia:Text_of_Creative_Commons_Attribution-ShareAlike_3.0_Unported_License).

## Solutions

[Talk to us](/contact) about the development of enterprise architecture vocabularies and regulatory and compliance taxonomies, and integrating Taxonomies for Confluence into your environment.