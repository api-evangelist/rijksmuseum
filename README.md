# Rijksmuseum (rijksmuseum)

Rijksmuseum is the Dutch national museum dedicated to Dutch arts and history, located in Amsterdam. Its RijksData open-data programme exposes more than 800,000 collection object metadata records, 600,000+ public-domain images, 320,000 bibliographic records, 160,000 actor / institution records, and 70,000 controlled-vocabulary terms through a family of JSON-based REST APIs, an OAI-PMH harvesting endpoint, IIIF tile services, and linked-data dumps.

**APIs.json:** [https://data.rijksmuseum.nl/](https://data.rijksmuseum.nl/)

## Tags

- Art And Design
- Museums
- Cultural Heritage
- Open Data
- Linked Data
- OAI-PMH
- IIIF
- Dutch Heritage
- Public APIs

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-29

## APIs

### Collection Search API

Returns a paginated list of objects in the Rijksmuseum collection. Mirrors the museum's own advanced-search experience and supports rich filters by maker, type, material, technique, century, dominant colour, image availability, and top-piece status. Results are language-localised via the culture path segment (`nl` or `en`) and capped at 10,000 objects per query (page * pageSize <= 10,000).

- **Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)
- **Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

- Collection
- Search
- Art And Design

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rijksmuseum-collection.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-collection.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rijksmuseum-art-object-summary-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Collection Details API

Returns the full record for a single object identified by its object-number (e.g. `SK-C-5`). Includes title, descriptions, principal maker biography, dating, dimensions, materials, techniques, classification (Iconclass), colours, plaque text in both Dutch and English, acquisition history, exhibitions, and the web image with offset percentages.

- **Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)
- **Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

- Collection
- Object Details
- Art And Design

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rijksmuseum-collection.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-collection.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rijksmuseum-art-object-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Collection Image Tiles API

Returns a tile-pyramid description for an object's web image to power deep zoom experiences (the same scheme used on rijksmuseum.nl). Each level (z0 to z6) lists tile URLs with x/y coordinates and the level's total width/height. JSON-only.

- **Human URL:** [https://data.rijksmuseum.nl/object-metadata/api/](https://data.rijksmuseum.nl/object-metadata/api/)
- **Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

- Collection
- Images
- Deep Zoom
- IIIF Adjacent

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/api/)
- [OpenAPI](openapi/rijksmuseum-collection-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rijksmuseum-collection.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-collection.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rijksmuseum-image-tiles-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Usersets API

Lists user-generated sets ("Rijksstudio sets") of objects curated by Rijksstudio members. Each set has an owner, name, slug, object count, and created/updated timestamps. Useful for surfacing community-curated mini exhibitions and personal collections.

- **Human URL:** [https://data.rijksmuseum.nl/user-generated-content/api/](https://data.rijksmuseum.nl/user-generated-content/api/)
- **Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

- User Generated Content
- Sets
- Rijksstudio

#### Properties

- [Documentation](https://data.rijksmuseum.nl/user-generated-content/api/)
- [OpenAPI](openapi/rijksmuseum-user-sets-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rijksmuseum-user-sets.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-user-sets.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rijksmuseum-user-set-summary-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Userset Details API

Returns the full contents of a single Rijksstudio set including the owner profile, the ordered list of set items (each linking to a Collection object and image), and crop metadata for cover images.

- **Human URL:** [https://data.rijksmuseum.nl/user-generated-content/api/](https://data.rijksmuseum.nl/user-generated-content/api/)
- **Base URL:** `https://www.rijksmuseum.nl/api`

#### Tags

- User Generated Content
- Sets
- Rijksstudio

#### Properties

- [Documentation](https://data.rijksmuseum.nl/user-generated-content/api/)
- [OpenAPI](openapi/rijksmuseum-user-sets-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rijksmuseum-user-sets.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-user-sets.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rijksmuseum-user-set-schema.json) — [JSON Schema](https://json-schema.org/specification)

### OAI-PMH Harvesting API

Standards-based bulk harvesting endpoint implementing the Open Archives Initiative Protocol for Metadata Harvesting (OAI-PMH 2.0). Supports ListRecords, GetRecord, ListMetadataFormats, ListSets, and ListIdentifiers verbs across the Dublin Core (dc), Europeana Data Model (edm_dc), and LIDO metadata formats. Use this — not the Collection Search API — to mirror more than 600,000 object records beyond the 10,000-object search ceiling.

- **Human URL:** [https://data.rijksmuseum.nl/object-metadata/harvest/](https://data.rijksmuseum.nl/object-metadata/harvest/)
- **Base URL:** `https://www.rijksmuseum.nl/api/oai`

#### Tags

- OAI-PMH
- Harvesting
- Bulk Data
- Dublin Core
- Europeana
- LIDO

#### Properties

- [Documentation](https://data.rijksmuseum.nl/object-metadata/harvest/)
- [Code Examples](https://github.com/Q42/SimpleOAIHarvester)
- [Postman Collection](collections/rijksmuseum-collection.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-collection.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/rijksmuseum-user-sets.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rijksmuseum-user-sets.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.rijksmuseum.nl/en)
- [Documentation](https://data.rijksmuseum.nl/)
- [Documentation](https://rijksmuseum.github.io/)
- [GitHub Organization](https://github.com/Rijksmuseum)
- [Sign Up](https://www.rijksmuseum.nl/en/rijksstudio)
- [Authentication](https://data.rijksmuseum.nl/object-metadata/api/#access-to-apis)
- [Plans](plans/rijksmuseum-plans-pricing.yml)
- [Rate Limits](rate-limits/rijksmuseum-rate-limits.yml)
- [Terms of Service](https://www.rijksmuseum.nl/en/data/policy)
- [License](https://creativecommons.org/publicdomain/mark/1.0/)
- [License](https://creativecommons.org/licenses/by/4.0/)
- [Knowledge](https://www.rijksmuseum.nl/en/data/policy)
- [Vocabulary](vocabulary/rijksmuseum-vocabulary.yml)
- [Discovery](https://data.rijksmuseum.nl/controlled-vocabularies/)
- [Discovery](https://data.rijksmuseum.nl/bibliographic-data/)
- [Integrations](https://lido-schema.org/)
- [Integrations](https://pro.europeana.eu/edm-documentation)
- [Integrations](https://www.dublincore.org/specifications/dublin-core/)
- [Integrations](https://linked.art/)
- [Integrations](https://iiif.io/)
- [Tools](https://github.com/Rijksmuseum/aio_oai_repo)
- [Tools](https://github.com/r-huijts/rijksmuseum-mcp)
- [Tools](https://github.com/kintopp/rijksmuseum-mcp-plus)
- [Tools](https://github.com/kintopp/rijksmuseum-mcp-client)
- [Tools](https://github.com/lwsinclair/rijksmuseum-mcp-oaipmh)
- [Tools](https://github.com/kintopp/rijksmuseum-iconclass-mcp)
- [Tools](https://github.com/chandhoke/archival-imagery-mcp)
- [SDK](https://github.com/hay/rijksmuseumapi)
- [SDK](https://github.com/yutongquan/rijksmuseum_py)
- [Code Examples](https://github.com/Q42/SimpleOAIHarvester)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
