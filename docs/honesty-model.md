# The honesty model

Vestige's core promise: **it never claims more than its sources do.** Four facts travel with every
event as first-class data, not footnotes.

## 1. Geometry precision
Sources locate events very differently — a USGS earthquake is a precise point; a cyclone is a
best-track *line*; a flood recorded by forecast zone attaches to a *county*, not a pinpoint. Vestige
labels each event's `geom_precision` and **never renders a low-precision event as a pinpoint**. A
line is drawn as a line; a county event covers its county — never a dot pretending to be exact.

## 2. Impact absence is data, not zero
Most sources record *where* and *how strong*, not *what it did*. USGS gives magnitude, not
casualties; IBTrACS gives track and wind, not losses. When impact isn't recorded, Vestige says so
explicitly — **"not recorded by this source"** — never an implied zero.

## 3. No invented totals
Vestige never sums per-event figures into a place-level total. A summed total is a number that
exists in no source. Itemized, sourced figures only.

## 4. Generated text is labeled
Event summaries are deterministic — templated from the recorded fields — and marked as generated.
No free-form model prose is presented as if it were the source record.
