# Rijksmuseum (rijksmuseum)

Rijksmuseum is the Dutch national museum dedicated to Dutch arts and history, located in Amsterdam. Its RijksData open-data programme exposes more than 800,000 collection object metadata records, 600,000+ public-domain images, 320,000 bibliographic records, 160,000 actor / institution records, and 70,000 controlled-vocabulary terms through a family of JSON-based REST APIs, an OAI-PMH harvesting endpoint, IIIF tile services, and linked-data dumps.

**URL:** [Visit APIs.json URL](https://data.rijksmuseum.nl/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Type

- **x-type:** opensource
- **x-tier:** 2 (museum open data with API key and rich public-domain content)
- **x-governance:** open-data
- **x-license-policy:** cc0-or-public-domain-for-most-images
- **x-source:** [public-apis/public-apis](https://github.com/public-apis/public-apis) — category: Art & Design

## Tags

Art And Design, Museums, Cultural Heritage, Open Data, Linked Data, OAI-PMH, IIIF, Dutch Heritage, Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### Collection Search API

Returns a paginated list of objects in the Rijksmuseum collection. Mirrors the museum's own advanced-search experience and supports rich filters by maker, type, material, technique, century, dominant colour, image availability, and top-piece status. Results are language-localised via the culture path segment (`nl` or `en`) and capped at 10,000 objects per query (page * pageSize <= 10,000).

**Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)

**Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

Collection, Search, Art And Design

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml)
- [JSON Schema — Art Object Summary](json-schema/rijksmuseum-art-object-summary-schema.json)
- [Naftiko Capability — Collection](capabilities/collection-collection.yaml)

### Collection Details API

Returns the full record for a single object identified by its object-number (e.g. `SK-C-5`). Includes title, descriptions, principal maker biography, dating, dimensions, materials, techniques, classification (Iconclass), colours, plaque text in both Dutch and English, acquisition history, exhibitions, and the web image with offset percentages.

**Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)

**Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

Collection, Object Details, Art And Design

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml)
- [JSON Schema — Art Object](json-schema/rijksmuseum-art-object-schema.json)
- [Naftiko Capability — Object Details](capabilities/collection-object-details.yaml)

### Collection Image Tiles API

Returns a tile-pyramid description for an object's web image to power deep zoom experiences (the same scheme used on rijksmuseum.nl). Each level (z0 to z6) lists tile URLs with x/y coordinates and the level's total width/height. JSON-only.

**Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)

**Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

Collection, Images, Deep Zoom, IIIF Adjacent

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml)
- [JSON Schema — Image Tiles](json-schema/rijksmuseum-image-tiles-schema.json)
- [Naftiko Capability — Images](capabilities/collection-images.yaml)

### Usersets API

Lists user-generated sets ("Rijksstudio sets") of objects curated by Rijksstudio members. Each set has an owner, name, slug, object count, and created/updated timestamps. Useful for surfacing community-curated mini exhibitions and personal collections.

**Human URL:** [https://data.rijksmuseum.nl/user-generated-content/api/](https://data.rijksmuseum.nl/user-generated-content/api/)

**Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

User Generated Content, Sets, Rijksstudio

#### Properties

- [Documentation](https://data.rijksmuseum.nl/user-generated-content/api/)
- [OpenAPI](openapi/rijksmuseum-user-sets-openapi.yml)
- [JSON Schema — User Set Summary](json-schema/rijksmuseum-user-set-summary-schema.json)
- [Naftiko Capability — User Generated Content](capabilities/user-sets-user-generated-content.yaml)

### Userset Details API

Returns the full contents of a single Rijksstudio set including the owner profile, the ordered list of set items (each linking to a Collection object and image), and crop metadata for cover images.

**Human URL:** [https://data.rijksmuseum.nl/user-generated-content/api/](https://data.rijksmuseum.nl/user-generated-content/api/)

**Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

User Generated Content, Sets, Rijksstudio

#### Properties

- [Documentation](https://data.rijksmuseum.nl/user-generated-content/api/)
- [OpenAPI](openapi/rijksmuseum-user-sets-openapi.yml)
- [JSON Schema — User Set](json-schema/rijksmuseum-user-set-schema.json)
- [Naftiko Capability — User Generated Content](capabilities/user-sets-user-generated-content.yaml)

### OAI-PMH Harvesting API

Standards-based bulk harvesting endpoint implementing the Open Archives Initiative Protocol for Metadata Harvesting (OAI-PMH 2.0). Supports `ListRecords`, `GetRecord`, `ListMetadataFormats`, `ListSets`, and `ListIdentifiers` verbs across the Dublin Core (`dc`), Europeana Data Model (`edm_dc`), and LIDO (`lido`) metadata formats. Use this — not the Collection Search API — to mirror more than 600,000 object records beyond the 10,000-object search ceiling.

**Human URL:** [https://data.rijksmuseum.nl/object-metadata/harvest/](https://data.rijksmuseum.nl/object-metadata/harvest/)

**Base URL:** `https://www.rijksmuseum.nl/api/oai`

#### Tags

OAI-PMH, Harvesting, Bulk Data, Dublin Core, Europeana, LIDO

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/harvest/)
- [Reference Harvester — Q42/SimpleOAIHarvester](https://github.com/Q42/SimpleOAIHarvester)

## Common Properties

- [Website](https://www.rijksmuseum.nl/en)
- [Documentation — RijksData](https://data.rijksmuseum.nl/)
- [Legacy API Documentation (Archived)](https://rijksmuseum.github.io/)
- [GitHub Organization](https://github.com/Rijksmuseum)
- [Sign Up — Rijksstudio Account For API Key](https://www.rijksmuseum.nl/en/rijksstudio)
- [Authentication](https://data.rijksmuseum.nl/object-metadata/api/#access-to-apis)
- [Plans / Pricing](plans/rijksmuseum-plans-pricing.yml)
- [Rate Limits](rate-limits/rijksmuseum-rate-limits.yml)
- [Terms Of Service — Information And Data Policy](https://www.rijksmuseum.nl/en/data/policy)
- [License — Public Domain Mark (most object images)](https://creativecommons.org/publicdomain/mark/1.0/)
- [License — CC-BY (modern works and museum photography)](https://creativecommons.org/licenses/by/4.0/)
- [Open Data Policy](https://www.rijksmuseum.nl/en/data/policy)
- [Vocabulary](vocabulary/rijksmuseum-vocabulary.yml)
- [Controlled Vocabularies (Actors, Places, Concepts, Events)](https://data.rijksmuseum.nl/controlled-vocabularies/)
- [SRU Bibliographic Catalogue](https://data.rijksmuseum.nl/bibliographic-data/)
- [Integration — LIDO](https://lido-schema.org/)
- [Integration — Europeana Data Model](https://pro.europeana.eu/edm-documentation)
- [Integration — Dublin Core](https://www.dublincore.org/specifications/dublin-core/)
- [Integration — Linked Art](https://linked.art/)
- [Integration — IIIF](https://iiif.io/)
- [Tools — aio_oai_repo (Configurable OAI-PMH Repository Library)](https://github.com/Rijksmuseum/aio_oai_repo)
- [MCP Server — Community — Artwork Exploration And Analysis](https://github.com/r-huijts/rijksmuseum-mcp)
- [MCP Server — Community — Semantic Search, Provenance, Similarity, Spatial Reasoning](https://github.com/kintopp/rijksmuseum-mcp-plus)
- [MCP Client — Community — Web Client For MCP+ Server](https://github.com/kintopp/rijksmuseum-mcp-client)
- [MCP Server — Community — OAI-PMH Harvesting](https://github.com/lwsinclair/rijksmuseum-mcp-oaipmh)
- [MCP Server — Community — Iconclass Semantic Search](https://github.com/kintopp/rijksmuseum-iconclass-mcp)
- [MCP Server — Community — Multi-Museum Imagery](https://github.com/chandhoke/archival-imagery-mcp)
- [SDK — PHP Client (Community)](https://github.com/hay/rijksmuseumapi)
- [SDK — Python Client (Community)](https://github.com/yutongquan/rijksmuseum_py)
- [Code Examples — SimpleOAIHarvester](https://github.com/Q42/SimpleOAIHarvester)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Rijksmuseum Collection API](openapi/rijksmuseum-collection-openapi.yml)
- [Rijksmuseum Usersets API](openapi/rijksmuseum-user-sets-openapi.yml)

### JSON Schema

- [Art Object Summary](json-schema/rijksmuseum-art-object-summary-schema.json)
- [Art Object (full record)](json-schema/rijksmuseum-art-object-schema.json)
- [Image Tiles](json-schema/rijksmuseum-image-tiles-schema.json)
- [Userset Summary](json-schema/rijksmuseum-user-set-summary-schema.json)
- [Userset (full)](json-schema/rijksmuseum-user-set-schema.json)

### JSON Structure

- [Art Object Summary](json-structure/rijksmuseum-art-object-summary-structure.json)
- [Art Object (full record)](json-structure/rijksmuseum-art-object-structure.json)
- [Image Tiles](json-structure/rijksmuseum-image-tiles-structure.json)
- [Userset Summary](json-structure/rijksmuseum-user-set-summary-structure.json)
- [Userset (full)](json-structure/rijksmuseum-user-set-structure.json)

### JSON-LD

- [Rijksmuseum Context](json-ld/rijksmuseum-context.jsonld)

### Examples

- [Search Collection](examples/rijksmuseum-search-collection-example.json)
- [Get Collection Object](examples/rijksmuseum-get-collection-object-example.json)
- [Get Collection Object Tiles](examples/rijksmuseum-get-collection-object-tiles-example.json)
- [List User Sets](examples/rijksmuseum-list-user-sets-example.json)
- [Get User Set](examples/rijksmuseum-get-user-set-example.json)

## Capabilities

Naftiko capabilities — one self-contained file per business surface (OpenAPI tag), each bundling consumes + REST + MCP exposers inline.

### Collection Search API

- [Collection](capabilities/collection-collection.yaml) — 1 operation: Search The Rijksmuseum Collection

### Collection Details API

- [Object Details](capabilities/collection-object-details.yaml) — 1 operation: Get Collection Object Details

### Collection Image Tiles API

- [Images](capabilities/collection-images.yaml) — 1 operation: Get Collection Object Image Tiles

### Usersets API / Userset Details API

- [User Generated Content](capabilities/user-sets-user-generated-content.yaml) — 2 operations: List Rijksstudio User Sets, Get Rijksstudio User Set Details

## Vocabulary

- [Rijksmuseum Vocabulary](vocabulary/rijksmuseum-vocabulary.yml) — Operational, capability, and semantic dimensions aligned with Dublin Core, EDM, LIDO, Linked Art, Iconclass, and schema.org

## Rules

- [Rijksmuseum Spectral Rules](rules/rijksmuseum-rules.yml) — 16 rules enforcing Rijksmuseum API conventions (Title-Case summaries, culture-prefixed paths, API-key security, microcks extension, locale-scoped routes, pagination cap documentation)

## Plans

- [Plans / Pricing](plans/rijksmuseum-plans-pricing.yml) — Single open-data freemium plan, free API key via Rijksstudio account

## Rate Limits

- [Rate Limits](rate-limits/rijksmuseum-rate-limits.yml) — 10,000 requests per API key per day, 10,000-result search window, OAI-PMH resumption token pacing

## Notes

This entry was originally bulk-registered from the public-apis catalog on 2026-05-28 and enriched on 2026-05-29 via the API Evangelist opensource pipeline (17 of 18 steps; FinOps step skipped as the museum offers no commercial billing surface). All artifacts were generated from the Rijksmuseum's archived developer documentation at `github.com/Rijksmuseum/rijksmuseum.github.io` and validated against published examples.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
