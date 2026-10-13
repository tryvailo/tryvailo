# Cognac Nation

**Specialist product discovery, collections and community**

[Explore Cognac Nation](https://cognacnation.com/) · [Browse the catalogue](https://cognacnation.com/cognacs) · [Back to portfolio](../README.md)

## The product problem

Specialist discovery needs more than a product list. Enthusiasts want to understand bottles, brands and regions, keep track of their own collection, read reviews and compare available offers. Maintaining the catalogue and community also needs workable editorial, contribution and administration tools.

Cognac Nation connects those consumer and operational journeys in one platform.

## What the product does

- Supports structured bottle, brand and region discovery, with search and catalogue detail pages.
- Provides ratings, reviews, personal collections and wishlists.
- Connects catalogue records with seller offer feeds and enrichment workflows.
- Supports community activity and editorial content.
- Includes creator submissions, draft and media workflows, merchant workspaces and administrative review tools.

The public catalogue and community are live. Some operational workflows require authenticated roles and are not visible to anonymous visitors.

## Product and technical work

This project represents my hands-on product development and technical implementation work across a specialist consumer platform and its operational tools. It connects catalogue data, user contributions and editorial workflows to the experience people use to discover and organise products.

The implementation contains domain services, loaders, actions and validation schemas, alongside reusable consumer components. Feed adapters separate external offers from catalogue operations. Creator and merchant journeys have their own submission and review flows.

**Technology:** TypeScript, Next.js, React, Supabase/PostgreSQL, Tailwind CSS and Vercel.

## Implementation scale

| Measure                                               |                Count |
| ----------------------------------------------------- | -------------------: |
| Selected catalogue, community and operational modules |  52,556 source lines |
| Application source, including shared foundation       | 200,501 source lines |
| Separate test source                                  |  61,793 source lines |

The measured snapshot was committed on 5 October 2026. Selected modules cover the domain library and reusable product components; route-level interfaces, SQL definitions and shared infrastructure are outside that subset.

[Read the measurement methodology](../metrics/README.md). These figures describe implementation size and do not imply catalogue leadership, user numbers, revenue or individual authorship. The implementation repository is private.
