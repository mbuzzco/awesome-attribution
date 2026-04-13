# Awesome Attribution [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC0-1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

> A curated list of attribution, measurement, and marketing analytics resources — open-source libraries, commercial platforms, research papers, datasets, and the people thinking hard about which marketing dollar caused which revenue dollar.

Marketing attribution is the discipline of assigning credit for revenue to the channels, campaigns, and touchpoints that caused it. It is an unsolved problem, actively researched, and the subject of more vendor pitches than any other area of martech. This list aims to be a useful map — honest, alphabetical, and uninterested in rankings.

## Contents

- [Open-Source Attribution Libraries](#open-source-attribution-libraries)
- [Open-Source MMM & Incrementality](#open-source-mmm--incrementality)
- [Commercial Attribution Platforms](#commercial-attribution-platforms)
- [Commercial MMM & Incrementality Platforms](#commercial-mmm--incrementality-platforms)
- [Server-Side Tracking Infrastructure](#server-side-tracking-infrastructure)
- [Research & Papers](#research--papers)
- [Methodology Guides & Long-Form Writing](#methodology-guides--long-form-writing)
- [Datasets](#datasets)
- [Blogs & Newsletters](#blogs--newsletters)
- [Podcasts](#podcasts)
- [Communities](#communities)
- [Related Lists](#related-lists)
- [Contributing](#contributing)

---

## Open-Source Attribution Libraries

SDKs and libraries for tracking, modeling, and assigning credit in marketing data. Self-hostable where noted.

- [ChannelAttribution](https://cran.r-project.org/package=ChannelAttribution) — R package implementing Markov-chain and heuristic attribution models. Academic foundation for a lot of commercial tooling.
- [mbuzz-node](https://github.com/mbuzzco/mbuzz-node) — Node.js / TypeScript SDK for server-side multi-touch attribution, tied to the mbuzz hosted platform.
- [mbuzz-php](https://github.com/mbuzzco/mbuzz-php) — PHP SDK for server-side attribution with framework-agnostic core and Laravel/Symfony adapters.
- [mbuzz-python](https://github.com/mbuzzco/mbuzz-python) — Python SDK for server-side attribution with Flask middleware.
- [mbuzz-ruby](https://github.com/mbuzzco/mbuzz-ruby) — Ruby SDK for server-side attribution with Rails Railtie, middleware, and background-job support.
- [pychattr](https://github.com/jerednel/pychattr) — Python implementation of channel attribution, port of the R `ChannelAttribution` package.
- [Shapley value for attribution](https://github.com/mskelton/marketing-attribution-models) — Reference implementations of Shapley-value attribution alongside other heuristic models.

## Open-Source MMM & Incrementality

Marketing mix modeling and causal measurement, now mostly free.

- [CausalImpact](https://github.com/google/CausalImpact) — Google's R package for estimating causal effects using Bayesian structural time-series. The reference implementation behind most geo-test analysis.
- [GeoLift](https://github.com/facebookincubator/GeoLift) — Meta's R package for designing and analyzing geo-experiments to measure lift.
- [LightweightMMM](https://github.com/google/lightweight_mmm) — Google's Bayesian marketing mix modeling library in Python/JAX. Deprecated in favor of Meridian but still widely used.
- [Meridian](https://github.com/google/meridian) — Google's successor to LightweightMMM. Bayesian MMM with reach-and-frequency support, production-oriented.
- [Robyn](https://github.com/facebookexperimental/Robyn) — Meta's open-source semi-automated MMM framework in R. Heavily used in the Meta ecosystem.
- [PyMC Marketing](https://github.com/pymc-labs/pymc-marketing) — PyMC-based Bayesian marketing analytics library from PyMC Labs. MMM, CLV, and customer analytics.

## Commercial Attribution Platforms

Vendors that sell attribution as a product. Listed alphabetically with no ranking. Descriptions are intentionally flat.

- [Adjust](https://www.adjust.com) — Mobile measurement platform (MMP) focused on app install attribution and fraud prevention. Owned by AppLovin.
- [AppsFlyer](https://www.appsflyer.com) — Mobile measurement platform. Large independent MMP with strong agency and network integrations.
- [Attribution](https://attributionapp.com) — Multi-touch attribution for B2B SaaS. Long-standing independent vendor.
- [Branch](https://branch.io) — Mobile linking and attribution, cross-platform deep linking.
- [Cometly](https://www.cometly.com) — Attribution platform positioning around creative-level ROAS for DTC brands.
- [Dreamdata](https://dreamdata.io) — B2B revenue attribution platform focused on buyer journey and sales-pipeline contribution.
- [Factors.ai](https://www.factors.ai) — B2B marketing analytics and attribution, with LinkedIn ad retargeting integrations.
- [Fospha](https://www.fospha.com) — Full-funnel measurement for DTC brands, with MMP, MMM, and media planning in one stack.
- [Funnel.io](https://funnel.io) — Marketing data hub and reporting, recently extending into measurement and clarity products.
- [HockeyStack](https://hockeystack.com) — B2B analytics and attribution; has pivoted product positioning toward AI-driven GTM agents.
- [Kochava](https://www.kochava.com) — Mobile measurement and data marketplace.
- [mbuzz](https://mbuzz.co) — Server-side multi-touch attribution for technical marketers, with open-source SDKs and a custom Attribution DSL. Bootstrapped.
- [Mutinex](https://mutinex.co) — Continuous marketing mix modeling platform, ANZ-founded.
- [Rockerbox](https://www.rockerbox.com) — Multi-touch attribution for DTC and retail, with MMM features layered on top.
- [Ruler Analytics](https://www.ruleranalytics.com) — Marketing attribution with form-fill and phone-call tracking, UK-focused.
- [SegmentStream](https://segmentstream.com) — Probabilistic attribution and conversion modeling, ML-driven.
- [Triple Whale](https://www.triplewhale.com) — Ecommerce analytics and attribution centered on Shopify stores.

## Commercial MMM & Incrementality Platforms

Causal measurement vendors — MMM, geo-lift, and incrementality testing. Separated from MTA vendors because the methodology, price point, and buyer are different.

- [Analytic Partners](https://analyticpartners.com) — Enterprise marketing mix modeling consultancy and platform.
- [Haus](https://haus.io) — Incrementality testing via geo-experiments. Founded by ex-Google and Netflix economists.
- [Measured](https://www.measured.com) — Cross-channel incrementality testing and measurement, enterprise-focused.
- [Nielsen Marketing Mix](https://www.nielsen.com/solutions/media-planning/marketing-mix-modeling/) — Legacy MMM from Nielsen, enterprise.
- [Northbeam](https://www.northbeam.io) — MTA + MMM blended measurement for DTC and ecommerce brands.
- [Recast](https://getrecast.com) — Modern Bayesian MMM and incrementality platform for growth-stage brands. Also ships [GeoLift by Recast](https://getrecast.com/geolift) as a free tool.

## Server-Side Tracking Infrastructure

The data plane that feeds attribution. Without accurate upstream data, no attribution model outputs a truthful answer.

- [Google Tag Manager Server Container](https://developers.google.com/tag-platform/tag-manager/server-side) — Google's server-side GTM, runs in Google Cloud or self-hosted.
- [Jitsu](https://github.com/jitsucom/jitsu) — Open-source Segment alternative for event collection.
- [RudderStack](https://github.com/rudderlabs/rudder-server) — Open-source CDP and event pipeline, warehouse-first.
- [Segment](https://segment.com) — Customer data platform and event routing, now part of Twilio.
- [Snowplow](https://github.com/snowplow/snowplow) — Open-source behavioral data platform with strong schema enforcement.
- [Stape](https://stape.io) — Managed server-side GTM hosting with a large tag template marketplace.
- [TAGGRS](https://taggrs.io) — Managed server-side tagging, competitive with Stape.
- [Tealium](https://tealium.com) — Enterprise tag management and CDP.

## Research & Papers

Academic and applied research on attribution, lift, and causal measurement.

- [Causally Motivated Attribution for Online Advertising](https://dl.acm.org/doi/10.1145/2351356.2351363) — Dalessandro, Perlich, Stitelman, Provost (ADKDD 2012). Foundational paper arguing for causality over heuristics in attribution.
- [Data-driven Multi-touch Attribution Models](https://dl.acm.org/doi/10.1145/2020408.2020453) — Shao & Li (KDD 2011). Early influential paper on probabilistic and logistic attribution modeling.
- [From Attribution to Causality in Digital Advertising](https://ieeexplore.ieee.org/document/10915142) — Chivukula, Jin, Zhan, Dropbox Marketing Data Science (IEEE Access, 2026). Documents a $25M reallocation at Dropbox after moving from click attribution to causal incrementality. Click attribution found to overstate by 2–10x.
- [A Comparison of Attribution Models in Online Advertising](https://research.google/pubs/a-comparison-of-attribution-models-in-online-advertising/) — Berman (Marketing Science, 2018). Compares last-click, first-click, linear, and Shapley approaches.
- [Measuring Ad Effectiveness Using Geo Experiments](https://research.google/pubs/measuring-ad-effectiveness-using-geo-experiments/) — Vaver & Koehler, Google Research. Underpins most modern geo-lift methodology.
- [Bayesian Methods for Media Mix Modeling with Carryover and Shape Effects](https://research.google/pubs/bayesian-methods-for-media-mix-modeling-with-carryover-and-shape-effects/) — Jin, Wang, Sun, Chan, Koehler, Google Research. Methodological foundation for LightweightMMM and Meridian.
- [Challenges and Opportunities in Media Mix Modeling](https://research.google/pubs/challenges-and-opportunities-in-media-mix-modeling/) — Chan & Perry, Google Research. Honest discussion of MMM limitations.

## Methodology Guides & Long-Form Writing

Long-form explainers and guides that assume the reader is serious.

- [Avinash Kaushik — Modern Analytics Maturity Model](https://www.kaushik.net/avinash/) — Five-level maturity ladder from ad-hoc reporting to incrementality-led decision making.
- [Haus — Incrementality 101](https://haus.io/blog) — Applied writing on how incrementality tests actually get designed and read.
- [IAB Australia — The Future of Measurement](https://iabaustralia.com.au) — Industry body consolidating vendor methodology standards and practitioner education.
- [IAB US — State of Data](https://www.iab.com/insights/) — Annual state-of-measurement report from the US IAB.
- [Madison and Wall — Brian Wieser](https://www.madisonandwall.com) — Advertising economist commentary on measurement and media.
- [mbuzz MTA Academy](https://mbuzz.co/academy) — Practitioner-oriented guides on multi-touch attribution, server-side tracking, and model selection.
- [Mobile Dev Memo — Attribution Archives](https://mobiledevmemo.com/category/attribution/) — Eric Seufert's writing on mobile, ATT, and measurement post-privacy.
- [Recast Blog — MMM Methodology](https://getrecast.com/blog) — Michael Kaminsky's writing on Bayesian MMM, geo-experiments, and measurement philosophy.

## Datasets

Public datasets useful for training, benchmarking, or stress-testing attribution models.

- [Criteo Attribution Modeling for Bidding Dataset](https://ailab.criteo.com/criteo-attribution-modeling-bidding-dataset/) — 16.5 million impressions labeled for attribution research. Used in the Criteo attribution Kaggle challenge.
- [Criteo Uplift Modeling Dataset](https://ailab.criteo.com/criteo-uplift-prediction-dataset/) — 25 million rows for uplift and incrementality modeling research.
- [KDD Cup 2012 Track 2 — Click Prediction](https://www.kaggle.com/c/kddcup2012-track2) — Search advertising click data, historically used for attribution-adjacent modeling.
- [Google GeoLift sample datasets](https://github.com/facebookincubator/GeoLift/tree/main/data) — Geo-experiment datasets bundled with the GeoLift R package.

## Blogs & Newsletters

People publishing consistently and independently about measurement.

- [Avinash Kaushik — Marketing-Analytics Intersect](https://www.kaushik.net/avinash/newsletter/) — 16 years at Google, former head of strategy for Adobe Marketing Cloud, now strategy leadership at Human Made Machine and Tapestry.
- [Haus Blog](https://haus.io/blog) — Incrementality-first, economist-driven writing.
- [Madison and Wall](https://www.madisonandwall.com) — Brian Wieser's advertising industry analysis, with strong measurement coverage.
- [mbuzz Academy](https://mbuzz.co/academy) — Server-side attribution, DSL design, and measurement-methodology writing.
- [MineThatData](https://minethatdata.com) — Kevin Hillstrom's long-running newsletter on retail, direct response, and attribution skepticism.
- [Mobile Dev Memo](https://mobiledevmemo.com) — Eric Seufert on mobile measurement, ATT, and the privacy-era advertising economy.
- [Recast Blog](https://getrecast.com/blog) — Michael Kaminsky and team on Bayesian MMM.
- [SparkToro Blog](https://sparktoro.com/blog) — Rand Fishkin on audience research and marketing honesty.

## Podcasts

- [GTMnow Podcast](https://gtmnow.com) — B2B GTM operators discussing pipeline, measurement, and agency economics.
- [Marketing Analytics Show](https://marketinganalyticsshow.com) — Michael Loban on analytics and measurement in practice.
- [Mobile Dev Memo Podcast](https://mobiledevmemo.com/podcast/) — Eric Seufert interviews measurement practitioners and executives.
- [The Martech Podcast](https://martechpod.com) — Benjamin Shapiro's interviews across marketing technology, regular measurement coverage.

## Communities

- [MeasureCamp](https://www.measurecamp.org) — Worldwide unconference series for digital analytics and measurement practitioners.
- [Measure Slack](https://www.measure.chat) — The largest practitioner community for digital analytics and measurement.
- [r/analytics](https://www.reddit.com/r/analytics/) — Reddit community for analytics practitioners.
- [r/marketingresearch](https://www.reddit.com/r/marketingresearch/) — Reddit community for quantitative and qualitative marketing research.

## Related Lists

- [awesome-analytics](https://github.com/oxnr/awesome-analytics) — General analytics resources, broader scope than this list.
- [awesome-marketing-machine-learning](https://github.com/station-10/awesome-marketing-machine-learning) — ML methods applied to marketing problems.
- [awesome-gtm-engineering](https://github.com/marketinguys/awesome-gtm-engineering) — Go-to-market engineering tooling and resources.

## Contributing

Contributions are welcome. Please read [contributing.md](contributing.md) before opening a pull request.

The short version:

1. One entry per PR.
2. Alphabetical order within every section.
3. Honest one-line descriptions — no superlatives, no marketing copy.
4. No ranking, no "best of" commentary.
5. Commercial tools must have a live homepage. Open-source projects must have commits in the last 12 months.
6. Self-listing is allowed under the same bar as any other entry.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related or neighboring rights to this work.
