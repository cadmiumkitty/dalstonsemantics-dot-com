---
title: "Taxonomies for Confluence"
featured: true
weight: 1
---

Increase the value of your investment in [Confluence](https://www.atlassian.com/software/confluence) by using it for enterprise architecture, data governance, regulatory compliance, risk management and more. Import [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/) controlled vocabularies, taxonomies and thesauri developed internally, by regulators or standards-setting organisations. Index Confluence pages and track alignment and gaps without complex and expensive specialised tools.

## Challenge

Organisations taking on the development of enterprise architecture, implementation of data governance or regulatory compliance may opt for expensive specialised software and neglect tools such as Atlassian Confluence and Jira that are already in place.

## Taxonomies for Confluence

### Getting started

Start with the development or adoption of an existing controlled vocabulary, taxonomy or thesaurus using SKOS.

For example, when developing enterprise architecture you may start with building a common vocabulary of terms such Business Capability and Business Service (here's [TOGAF 9.2 terms](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology) as an inspiration) and developing a taxonomy of business capabilities of your organisation (here's an example of [Investment Management Capabilities](https://github.com/cadmiumkitty/imc-taxonomy)). Similarly, you can build taxonomies from regulatory rulebooks when working on compliance projects (here's [taxonomy derived from APRA CPG 235 - Managing Data Risk](https://github.com/cadmiumkitty/cpg235-taxonomy)).

### Import SKOS concept schemes

Once Taxonomies for Confluence add-on is installed, new **Taxonomies** menu is added to the **Settings** page that is available to Confluence administrators. Select **Taxonomies** to navigate to the taxonomies settings page.

![Import SKOS taxonomies](/images/tfc/01-import-taxonomies.png)

To import SKOS vocabulary, taxonomy or thesaurus click **Upload SKOS taxonomy file** button and select the file (right now only [RDF Turtle](https://www.w3.org/TR/turtle/) format is supported). The upload will start automatically once the file is selected. When the upload completes, an updated list of taxonomies is displayed and you can explore their structure by clicking on the expansion button.

![Explore SKOS imported taxonomies](/images/tfc/03-imported-taxonomies-expanded.png)

### Index Confluence pages

Index Confluence pages by selecting concepts from imported SKOS concept schemes.

Click on the **Subject** byline, search for and click on the concept to index the page.

![Index Confluence Pages](/images/tfc/04-index.png)

### Track alignment and gaps

Track alignment of governance artefacts to controlled vocabularies, taxonomies and thesauri developed internally, by regulators or standards-setting organisations.

Once Taxonomies for Confluence add-on is installed, new **Taxonomies** item is added to the **Apps** menu.

![Taxonomies menu item](/images/tfc/05-apps.png)

Select **Taxonomies** to navigate to the taxonomies page.

![Track Alignment](/images/tfc/06-taxonomies-track.png)

### Use CQL for reporting and integration

Once Taxonomies for Confluence add-on is installed, three additional properties become available in Confluence pages and blog posts: `subjectUri` (populated with the URI of SKOS concept), `subjectPrefLabel` (populated from `skos:prefLabel`) and `subjectNotation` (populated from `skos:notation`).

Use these properties in CQL queries to integrate content or implement reporting using Confluence APIs.

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