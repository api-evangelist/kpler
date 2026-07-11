# Kpler (kpler)

Kpler is a commodities intelligence and maritime data platform that tracks cargoes, vessels, and trade flows across oil, refined products, LNG, LPG, and dry bulk markets. Kpler owns MarineTraffic and FleetMon (acquired 2023) and acquired Spire's maritime AIS business (2025), making it one of the largest vessel tracking operations in the world — a 9,000+ station terrestrial, satellite, and roaming AIS network tracking 350,000+ vessels daily.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kpler/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kpler/refs/heads/main/apis.yml)

## Access Model (Read This First)

Kpler's APIs are **real, publicly documented, but customer-gated**. There is no self-serve signup or published pricing:

- The Direct Access user guides (`liquids.dev.kpler.com`, `lng.dev.kpler.com`, `lpg.dev.kpler.com`, `coal.dev.kpler.com`, `freight.dev.kpler.com`), the developer portal (`developers.kpler.com`), the [Python SDK docs](https://python-sdk.dev.kpler.com/), and a [public Postman workspace](https://www.postman.com/kplerdev) are all publicly visible.
- Actually **calling** the APIs requires client credentials issued with a commercial Kpler subscription (Basic Auth, or a bearer token from `POST /login`).
- The OpenAPI document in this repo ([openapi/kpler-openapi.yml](openapi/kpler-openapi.yml)) is flagged `x-endpoints-modeled` — it covers only endpoints and parameters confirmed from public sources (including the documented example `https://api-dry.kpler.com/v1/trades?size=6&columns=trade_id,vessel_name,start,end&fromZones=Europe&toZones=Asia`), and does not fabricate the full gated surface.

## Tags

- Vessel Tracking
- Maritime
- Commodities
- Supply Chain
- AIS
- Trade Flows
- Shipping
- Energy

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Kpler Liquids API

Direct Access REST API for the Liquids platform (crude oil, CPP, DPP) — trades, flows, vessels, port calls, ship-to-ship transfers, storage/inventories, contracts, prices, and outages.

- **Human URL:** [https://liquids.dev.kpler.com/](https://liquids.dev.kpler.com/)
- **Base URL:** `https://api.kpler.com`

### Kpler LNG API

Direct Access REST API for the LNG platform — liquefied natural gas trades, cargo flows, vessels, and port calls.

- **Human URL:** [https://lng.dev.kpler.com/](https://lng.dev.kpler.com/)
- **Base URL:** `https://api-lng.kpler.com`

### Kpler LPG API

Direct Access REST API for the LPG platform.

- **Human URL:** [https://lpg.dev.kpler.com/](https://lpg.dev.kpler.com/)
- **Base URL:** `https://api-lpg.kpler.com`

### Kpler Dry Bulk API

Direct Access REST API for the Dry platform — coal and dry bulk trades, flows, and vessel movements.

- **Human URL:** [https://coal.dev.kpler.com/](https://coal.dev.kpler.com/)
- **Base URL:** `https://api-dry.kpler.com`

### Kpler Freight API

Freight analytics across the Liquids, Gas, and Dry platforms — freight metrics, fleet metrics, congestion, and ballast capacity.

- **Human URL:** [https://freight.dev.kpler.com/](https://freight.dev.kpler.com/)
- **Base URL:** `https://api.kpler.com`

### MarineTraffic API

Real-time and historical vessel tracking — vessel and fleet positions, historical tracks, port calls, expected arrivals, voyage forecasts and ETAs, port congestion, vessel particulars, photos, search, and reverse geocoding. `api_key` auth, credit-metered.

- **Human URL:** [https://servicedocs.marinetraffic.com/](https://servicedocs.marinetraffic.com/)
- **Base URL:** `https://services.marinetraffic.com/api`

### MarineTraffic Vessels API

GraphQL vessel intelligence on 220,000+ vessels — particulars plus six levels of ownership for due diligence and compliance. Contact-sales; reference docs delivered to customers.

- **Human URL:** [https://www.kpler.com/product/maritime/vessels-api](https://www.kpler.com/product/maritime/vessels-api)

### Kpler AIS Data Feed

Global AIS vessel-position feed (launched September 2025, replacing MarineTraffic AIS and Spire Maritime feeds) at ~5-second average latency. Delivered via API, NMEA (TCP), Kafka, or custom extract under enterprise contract. **No public WebSocket** — see [review.yml](review.yml).

- **Human URL:** [https://www.kpler.com/product/maritime/kplerais](https://www.kpler.com/product/maritime/kplerais)

## Common Properties

- [Website](https://www.kpler.com)
- [LinkedIn](https://www.linkedin.com/company/kpler)
- [Documentation](https://developers.kpler.com/)
- [Python SDK](https://python-sdk.dev.kpler.com/)
- [Postman Public Workspace](https://www.postman.com/kplerdev)
- [Plans](plans/kpler-plans-pricing.yml)
- [Rate Limits](rate-limits/kpler-rate-limits.yml)
- [FinOps](finops/kpler-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
