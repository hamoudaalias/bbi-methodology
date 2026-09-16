# OSF Registry — BBI Methodology

## Registration

- **DOI:** [10.17605/OSF.IO/5RU96](https://doi.org/10.17605/OSF.IO/5RU96)
- **URL:** https://osf.io/5ru96/
- **Registration date:** 2026-09-13
- **Registered by:** Hamouda Alias (Independent Researcher)
- **License:** CC-BY 4.0 International

## Purpose

Timestamping of the BBI pre-registration protocol. Every sealed design
doc, verdict, and result JSON in this repository traces to a SHA-256
digest that is archived on OSF before the corresponding measurement.

## Components (5 child DOIs)

| Component | DOI | Node | Status |
|---|---|---|---|
| Main project (parent) | [10.17605/OSF.IO/5RU96](https://doi.org/10.17605/OSF.IO/5RU96) | 5ru96 | Public, immutable |
| Pre-registration Protocols | [10.17605/osf.io/8w5rs](https://doi.org/10.17605/osf.io/8w5rs) | 8w5rs | Public |
| Testbed Specifications | [10.17605/osf.io/w7mtq](https://doi.org/10.17605/osf.io/w7mtq) | w7mtq | Public |
| Domain Extensions | [10.17605/osf.io/fgv5r](https://doi.org/10.17605/osf.io/fgv5r) | fgv5r | Public |
| Future Extensions | [10.17605/osf.io/5aqnr](https://doi.org/10.17605/osf.io/5aqnr) | 5aqnr | Public |
| 49 Methodological Lessons | [10.17605/osf.io/kbrjx](https://doi.org/10.17605/osf.io/kbrjx) | kbrjx | Public |

> **Note:** the "49 Methodological Lessons" component reflects the lesson
> count at the time of registration (2026-09-13). The vault now contains
> **56 lessons** (as of 2026-09-16, incl. Lessons 54-56 from Phases 3-5).
> OSF registrations are immutable;
> a new registration or update is required to reflect the current count.

## Traceability rule

Each file under `specs/`, `verdicts/`, and `extensions/` cites the
SHA-256 digest of its sealed source artifact. A published number
without its digest is not a BBI claim.