# Market Data Input V1.8

## Purpose
Capture date-sensitive Bursa security and valuation inputs. V1.8 does not require live market data. An absent, stale or inaccessible observation is MISSING/N/A or REQUIRES_VERIFICATION; do not supply a fabricated or remembered price.

## Market record fields
Use the full ingestion record in company_data_input.md and add:
- Market observation date/time and timezone.
- Venue/provider and exact URL/series/document reference.
- Price basis: open/close/intraday/VWAP, adjusted/unadjusted.
- Bursa ticker/security class and currency.
- Shares basis: issued, treasury-adjusted, basic/diluted and share-count date.
- Corporate-action adjustment details and linked action record.
- Market session/trading status, stale/current flag and retrieval date.
- Formula/source lineage for calculated market capitalization and enterprise value.

## Standard market fields
| Metric | Required treatment |
|---|---|
| Share price | Per-share currency, date/time, venue, closing/intraday and adjusted/unadjusted basis |
| Market capitalization | Dated price × defined shares or provider value with provider definition; retain inputs |
| Shares outstanding | Exact date, class, issued/treasury/diluted basis and source |
| Trading volume | Trading date/period, shares/lots unit, adjusted basis if applicable |
| 52-week high | Lookback end date, security class, adjusted/unadjusted basis, source |
| 52-week low | Lookback end date, security class, adjusted/unadjusted basis, source |
| P/E | Price date, trailing/forward basis, EPS definition, period and provider/calculation |
| P/B | Price date, book-value period and equity/share basis |
| Dividend yield | Price date, DPS period/status, trailing/forward calculation convention |
| Enterprise value | Date and bridge for market cap, debt, cash, leases, NCI and other included claims |

Valuation ratios may be provider-derived; identify denominator period and methodology. If definitions cannot be verified, use REQUIRES_VERIFICATION, not AVAILABLE.

## Freshness and historical data
Record both observation time and extraction time. Label an observation CURRENT only when its date is suitable for the analysis date; otherwise label STALE and state the age/impact. Never carry forward an old quote without disclosure. Preserve historical market snapshots and adjusted/unadjusted series. Do not silently recalculate past values after a corporate action; create an adjusted series linked to the original and adjustment source.

If market data are unavailable, V1.4 outputs requiring price, share count, market capitalization or EV may remain N/A; do not invent a live value.
