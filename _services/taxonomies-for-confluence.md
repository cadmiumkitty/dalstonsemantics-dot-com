---
title: "Taxonomies for Confluence"
description: "Taxonomies for Confluence add-on user guide. Quickly adapt Confluence to managing software development lifecycle, enterprise architecture, data governance, regulatory compliance, and risk management documentation. Taxonomies for Confluence enables: page classification in Confluence by type, subject and related concepts; use of existing controlled vocabularies and reference data such as capability models, industry classifications, risk and control, or other corporate taxonomies for page classification; creation of tables of contents based on type, subject and related concepts; improved search by using preferred and alternative concept labels to search for Confluence content; tracking of documentation coverage; integration of Confluence into knowledge graphs by linking information assets across several sources using structured data and SPARQL federated queries."
featured: true
weight: 2
---

Classify [Confluence](https://www.atlassian.com/software/confluence) pages using existing controlled vocabularies, improve search, build better tables of contents and integrate Confluence into knowledge graphs.

Organizations taking on the development of enterprise architecture or implementation of data governance and regulatory compliance may opt for new and expensive specialized documentation management software that requires adoption. They often neglect the existing tools, such as Atlassian Confluence and Jira, already widely used by their teams.

## Taxonomies for Confluence

Increase the value of your investment in Confluence by quickly adapting it to software development lifecycle, enterprise architecture, data governance, risk and regulatory compliance documentation management. Taxonomies for Confluence add-on enables: 
 * Page classification in Confluence by type, subject and related concepts
 * Use of existing controlled vocabularies and reference data such as capability models, industry classifications, risk and control, or other corporate taxonomies for page classification
 * Tables of contents with type, subject and related concepts
 * Improved search by using preferred and alternative concept labels to search for Confluence content
 * Tracking of documentation coverage
 * Integration of Confluence into knowledge graphs using structured data and SPARQL federated queries.

### Frequently asked questions

See [Frequently Asked Questions](/taxonomies-for-confluence-faq) for questions about using existing controlled vocabularies, such as corporate taxonomies, with Confluence, dealing with several user groups using different terms for the same concept, and implementing faceted classification of Confluence pages and blog posts.

### Getting started

Start with the development or adoption of existing controlled vocabularies - dictionaries, taxonomies or thesauri - using [Simple Knowledge Organization System (SKOS)](https://www.w3.org/2004/02/skos/).

For example, when developing an enterprise architecture, you may start with building a common vocabulary of terms such as Business Capability and Business Service (here's [TOGAF 9.2 terms](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology) as an inspiration) and developing a taxonomy of business capabilities of your organization (here's an example of [Investment Management Capabilities](https://github.com/cadmiumkitty/imc-taxonomy)). Similarly, you can build taxonomies from regulatory rulebooks when working on compliance projects (here's [taxonomy derived from APRA CPG 235 - Managing Data Risk](https://github.com/cadmiumkitty/cpg235-taxonomy)).

### Import SKOS concept schemes

Once the Taxonomies for Confluence add-on is installed, new **Taxonomies** menu is added to the **Settings** page available to Confluence administrators. It lets you import developed or adopted SKOS taxonomies and use them with Confluence.

Select **Taxonomies** to navigate to the taxonomies settings page.

![Empty snapshots](/images/tfc/4-11-0-1.png "When no taxonomies are imported, a list of empty snapshots is displayed.")

##### Importing SKOS taxonomies from catalog

To import open-source SKOS taxonomies from the curated catalog, select **Import SKOS taxonomies from catalog** from the Actions menu. In the **Import SKOS taxonomies from catalog** dialog select the taxonomies file and click **Import selected taxonomies**.

Taxonomies currently included in catalog:
 1. [Australian and New Zealand Standard Industrial Classification (ANZSIC)](https://github.com/cadmiumkitty/anzsic-taxonomy)
 1. [Taxonomy for Policy](https://github.com/cadmiumkitty/policy-taxonomy)
 1. [Software Development Lifecycle (SDLC) Document Types Taxonomy](https://github.com/cadmiumkitty/sdlc-document-types-taxonomy)
 1. [TOGAF® 9.2 Architecture Repository Document Types Taxonomy](https://github.com/cadmiumkitty/togaf-architecture-repository-document-types-taxonomy)
 1. [TOGAF® 9.2 Content Metamodel Vocabulary](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology)

![Import SKOS taxonomies from catalog](/images/tfc/4-11-0-2.png "In the Import SKOS taxonomies from catalog dialog select the taxonomies file and click Import selected taxonomies.")

##### Importing SKOS taxonomies from file

To import SKOS taxonomies from file, select **Import SKOS taxonomies from file** from the Actions menu. In the **Import SKOS taxonomies from file** dialog select the file and click **Upload and import file**. [RDF/XML](http://www.w3.org/TR/rdf-syntax-grammar/), [N-Triples](http://www.w3.org/TR/n-triples/), [Turtle](https://www.w3.org/TR/turtle/), Turtle-star, [N3/Notation3](http://www.w3.org/TeamSubmission/n3/), [TriX](http://swdev.nokia.com/trix/), [TriG](http://www.w3.org/TR/trig/), TriG-star, [binary RDF](http://rivuli-development.com/2011/11/binary-rdf-in-sesame/), [N-Quads](http://www.w3.org/TR/n-quads/), [JSON-LD](http://www.w3.org/TR/json-ld/), [RDF/JSON](http://www.w3.org/TR/rdf-json/), [RDFa](http://www.w3.org/TR/rdfa-syntax/) and [HDT](http://www.rdfhdt.org/hdt-binary-format/) formats are supported detected from the file extension.

![Import SKOS taxonomies from file](/images/tfc/4-11-0-3.png "In the Import SKOS taxonomies from file dialog select the file and click Upload and import file.")

##### Managing snapshots

The difference between draft and current snapshots is calculated when the upload completes, and updated statistics are displayed in the snapshot table. You can explore the contents of each snapshot by clicking on the corresponding row of the snapshot table.

![Explore imported SKOS taxonomies](/images/tfc/4-11-0-4.png "When one or more taxonomies are imported, you can explore their structure by expanding concept schemes to reveal top concepts, and expanding concepts to reveal narrower concepts.")

To clear the draft snapshot, select **Clear draft snapshot** from the Actions menu. In the **Clear draft snapshot** dialog, confirm that you want to clear the draft snapshot. When the request completes, the difference between cleared draft and current snapshots is calculated, and updated statistics are displayed in the snapshot table.

![Clear draft snapshot](/images/tfc/4-11-0-5.png "To clear the draft snapshot, select Clear draft snapshot from the Actions menu.")

When you are ready to start using the taxonomies in the draft snapshot with Confluence content, select **Start switching to draft snapshot** from the Actions menu. In the **Start switching to draft snapshot** dialog confirm that you want to start switching. When the request completes, the impact on the Confluence content is checked and reported in the snapshot table.

![Start switching to draft snapshot](/images/tfc/4-11-0-6.png "In the Start switching to draft snapshot dialog confirm that you want to start switching.")

To complete the switch, click the **Complete switch** button. In the case of Confluence content impact, the following actions are taken during the switch to update Confluence content.

| SKOS Concept changes      | Confluence content actions |
| ------------------------- | -------------------------- |
| Concept is removed | **Type** and **Subject** Confluence content property is removed, and **Related Concept** macro is replaced with the plain text content of `skos:prefLabel` property of the SKOS Concept. |
| Concept is removed with replacement Concept specified using `dcterms:replaces` property | **Type** and **Subject** content property and **Related Concept** macro are updated to reflect URI, `skos:prefLabel`, `skos:altLabel` and `skos:notation` of the replacement SKOS Concept. |
| Concept properties such as `skos:prefLabel`, `skos:altLabel` and `skos:notation` are updated | **Type** and **Subject** content property and **Related Concept** macro are updated to reflect the change in `skos:prefLabel`, `skos:altLabel` and `skos:notation` of the SKOS Concept. |

![Complete switch](/images/tfc/4-11-0-7.png "Complete or cancel the switch to the draft snapshot.")

When the snapshot switch and Confluence content migration are complete, the updated statistics are displayed in the snapshot table.

![Snapshots](/images/tfc/4-11-0-8-1.png "Updated statistics are displayed in the snapshot table.") 

### Classify Confluence pages

Once Taxonomies for Confluence add-on is installed, new **Type** and **Subject** bylines and **Related Concept** macro are made available to Confluence users. It enables classification of Confluence pages and blog posts using concepts from imported SKOS taxonomies.

#### Page classification using type

To classify Confluence page by type, click on the **Type** byline, search for and click on the concept corresponding to the type of the page (e.g. role description, performance requirements).

![Index Confluence Pages](/images/tfc/4-11-0-9.png "Expanded Type Byline showing concepts matching the search for the role. TOGAF Role concept is selected as the type of the page.")

#### Page classification using subject

To classify Confluence page by subject, click on the **Subject** byline, search for and click on the concept corresponding to the subject of the page (e.g. regulatory requirement, capability, service, system).

![Index Confluence Pages](/images/tfc/4-11-0-10.png "Expanded Subject Byline showing concepts matching the search for the data-specific roles. APRA CPG 235 guidance to define data-specific roles is selected.")

#### Page classification using related concepts

To classify Confluence page by related concepts, start typing `/related` anywhere in the body of the page and pick **Related Concept** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **Related Concept** from the Macro menu at the top.

![Index Confluence Pages](/images/tfc/4-11-0-11.png "Related Concept macro is being selected from the list of macros.")

Search for the related concept (e.g. data criticality classification, industry sector) to insert and select the concept from the search results.

![Index Confluence Pages](/images/tfc/4-11-0-12.png "Related Concept macro showing concepts matching the search for data quality. APRA CPG 235 Data Quality concept is selected to be inserted into the page.")

Click **Insert** to insert the relation. Once the relation is inserted, the URI of the concept, `skos:prefLabel`, `skos:altLabel` and `skos:notation` can be used in Confluence search.

![Index Confluence Pages](/images/tfc/4-11-0-13.png "APRA CPG 235 Data Quality concept is inserted into the Confluence page.")

#### Inserting table of contents

Start typing `/about` anywhere in the body of the page where you want to insert the table of contents and pick **About and Related** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **About and Related** from the Macro menu at the top.

![Insert Table of Contents](/images/tfc/4-11-0-14.png "About and Related macro is being selected from the list of macros.")

Build a set of criteria for pages to be included in the table of contents by selecting whether a concept is a type, subject or a relation of a page, and specifying whether narrower concepts need to be included.

For example, if you imported [TOGAF 9.2](https://github.com/cadmiumkitty/togaf-content-metamodel-ontology) and [CPG 235](https://github.com/cadmiumkitty/cpg235-taxonomy) taxonomies and classified Confluence pages using concepts from these taxonomies, creating the table of contents that includes pages that are Role descriptions, are about Data-specific roles and responsibilities and are related to concept of Data quality requires the following set of criteria:

![Insert Table of Contents](/images/tfc/4-11-0-15.png "About and Related macro editor with criteria specified to include Confluence pages that are Role descriptions, are about Data-specific roles and responsibilities and are related to concept of Data quality.")

Click **Insert** to insert the table of contents.

![Insert Table of Contents](/images/tfc/4-11-0-16.png "Table of Confluence pages and blog posts that are Role descriptions, are about Data-specific roles and responsibilities and are related to the concept of Data quality.")

### Track alignment and gaps

Once the Taxonomies for Confluence add-on is installed, the new **Taxonomies** App and **About and Related** macro are made available to Confluence users. They let you track the alignment of Confluence pages and blog posts to controlled vocabularies - dictionaries, taxonomies and thesauri - developed internally, by regulators or standards-setting organizations.

#### Navigating taxonomies and pages related to concepts

Select **Taxonomies** item from the **Apps** menu to navigate to the taxonomies page.

![Taxonomies menu item](/images/tfc/4-11-0-17.png "Taxonomies item is being selected from the Confluence Apps menu.")

Expand concepts to see narrower concepts or pages and blog posts that are about or related to these concepts.

![Track Alignment](/images/tfc/4-11-0-18.png "Taxonomies page showing imported SKOS concept schemes. APRA CPG 235 concept scheme is expanded to reveal top concepts, narrower concepts of Data and data risk concept, and narrower concepts and related Confluence content of the Data quality concept.")

### Creating statements about a page using RDFS Properties and Confluence tables

Once the Taxonomies for Confluence add-on is installed, the new **Resource** macro is made available to Confluence users. Resource references can be inserted anywhere on the page. When RDFS Property is placed in the first column of a table without a header row, and RDFS Classes, SKOS Concepts or other resources, macros (dates, links and mentions) and text are placed in subsequent columns, each row is translated into an RDF Statement about the page.

To insert a Resource reference (SKOS Concept, RDFS Class or RDFS Property), start typing `/resource` anywhere in the body of the page and pick **Resource** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **Resource** from the Macro menu at the top.

![Insert resource reference](/images/tfc/4-11-0-30.png "Resource macro is being selected from the list of macros.")

Search for the resource to insert the reference and select the resource from the search results.

![Selecting type property from RDF Vocabulary](/images/tfc/4-11-0-31.png "Type property is selected from RDF Vocabulary.")

Click **Insert** to insert the resource reference.

![Table to be translated into RDF Statements about the page](/images/tfc/4-11-0-33.png "Simple System entry to be used in data catalog.")

### Creating new statements using RDFS and Confluence tables

When RDFS Properties are placed in the header row of a table, and RDFS Classes, SKOS Concepts or other resources, macros (dates, links and mentions) and text are placed in rows, each row is translated into several RDF Statement about a new resource linked to a page.

![Table to be translated into RDF Statements](/images/tfc/4-11-0-34.png "Simple data catalog.")

### Querying pages and resources with SPARQL

Once the Taxonomies for Confluence add-on is installed, the new **SPARQL** macro is made available to Confluence users.

To insert a SPARQL query, start typing `/sparql` anywhere in the body of the page and pick **SPARQL** from the pop-up Macro menu. Alternatively, click `+` icon in the editor menu and pick **SPARQL** from the Macro menu at the top.

![Insert SPARQL querymacro](/images/tfc/4-11-0-40.png "SPARQL macro is being selected from the list of macros.")

Enter SPARQL query.

![Enter SPARQL query](/images/tfc/4-11-0-41.png "SPARQL syntax highlighting is supported.")

Click **Insert** to insert the SPARQL query and view results.

![SPARQL query results](/images/tfc/4-11-0-42.png "Querying simple data catalog.")

### Integrate Confluence into knowledge graphs using SPARQL federation

Use Taxonomies for Confluence [SPARQL](https://www.w3.org/TR/sparql11-overview/) endpoint to federate structured data across Confluence and other sources such as [GitHub](https://github.com/) or [Bitbucket](https://bitbucket.org/product). See [Knowledge Graph Descriptor](https://github.com/cadmiumkitty/kg-file) for a structured data example.

[Contact us](/contact) to request access.

![Federate structured data across several sources with SPARQL](/images/tfc/4-11-50.png "Federate structured data across several sources with SPARQL.")

### Use CQL for reporting and integration

Once Taxonomies for Confluence add-on is installed, three additional properties become available in Confluence pages and blog posts: `taxonomiesForConfluenceTypeUri` and `taxonomiesForConfluenceSubjectUri` (populated with the URI of SKOS concept set as type and subject respectively), `taxonomiesForConfluenceTypePreferredLabel` and `taxonomiesForConfluenceSubjectPreferredLabel` (populated from `skos:prefLabel`) and `taxonomiesForConfluenceTypeNotation` and `taxonomiesForConfluenceSubjectNotation` (populated from `skos:notation`). These properties can be used in CQL queries allowing you to integrate content or implement reporting using Confluence APIs.

For example, you can use [ANZSIC](https://www.abs.gov.au/ausstats/abs@.nsf/Latestproducts/1292.0Search12006%20(Revision%202.0)) codes in CQL search.

Request:

```
GET https://dalstonsemantics.atlassian.net/wiki/rest/api/search?cql=taxonomiesForConfluenceSubjectNotation=0806&limit=25
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
  "cqlQuery": "taxonomiesForConfluenceSubjectNotation=0806",
  "searchDuration": 61,
  "_links": {
    "base": "https://dalstonsemantics.atlassian.net/wiki",
    "context": "/wiki",
    "self": "https://dalstonsemantics.atlassian.net/wiki/rest/api/search?cql=taxonomiesForConfluenceSubjectNotation=0806"
  }
}
```

## Solutions

[Talk to us](/contact) about the development of enterprise architecture vocabularies and regulatory and compliance taxonomies, and integrating Taxonomies for Confluence into your environment.

## Attributions

This user guide uses material from the Wikipedia [Data Steward](https://en.wikipedia.org/wiki/Data_steward) and [BHP](https://en.wikipedia.org/wiki/BHP) articles, that are released under the [Creative Commons Attribution-Share-Alike License 3.0](https://creativecommons.org/licenses/by-sa/3.0/).