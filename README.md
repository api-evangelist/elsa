# ELSA (elsa)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ELSA (English Language Speech Assistant) builds AI speech-recognition and pronunciation-assessment technology for non-native English speakers, powering the ELSA Speak consumer app. The ELSA API is a partner/B2B speech-assessment service that scores recorded or streamed English audio across pronunciation, fluency, intonation, grammar, and vocabulary, returning sentence, word, and phoneme-level feedback.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/elsa/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/elsa/refs/heads/main/apis.yml)

> Disambiguation: This catalog covers ELSA Speak / ELSA Corp (elsaspeak.com, elsanow.io) — the AI English pronunciation and speech-assessment platform. It is unrelated to "Elsa", the open-source .NET workflows / workflow-engine library.

## Tags

- Speech Assessment
- Pronunciation
- Speech Recognition
- Language Learning
- AI

## Timestamps

- **Created:** 2026-06-21
- **Modified:** 2026-06-21

## APIs

### ELSA Pronunciation Assessment API (Scripted)

Scripted speech scoring. The caller submits an audio recording together with the expected script/sentence and receives sentence, word, and phoneme-level pronunciation scores, mispronunciation hints, word stress, reading speed, pausing, fluency, and intonation. Batch scoring is a POST to /score_audio; a realtime variant streams audio over a WebSocket to /ws/score_audio.

- **Human URL:** [https://api-external-doc.elsanow.co/](https://api-external-doc.elsanow.co/)
- **Base URL:** `https://api.elsanow.io/api/v2`

#### Tags

- Pronunciation
- Speech Assessment
- Scripted
- Phoneme Scoring

#### Properties

- [Documentation](https://api-external-doc.elsanow.co/)
- [API Reference](https://api-external-doc.elsanow.co/category/api)
- [OpenAPI](openapi/elsa-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elsa.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elsa.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ELSA Realtime Streaming Speech API

Realtime, packet-by-packet audio scoring over WebSocket. Scripted streaming connects to wss://api.elsanow.io/api/v2/ws/score_audio and unscripted (open-ended) streaming connects to wss://api.elsanow.io/api/v1/ws/score_audio_plus, delivering incremental pronunciation, fluency, intonation, grammar, and vocabulary feedback.

- **Human URL:** [https://api-external-doc.elsanow.co/websocket-scripted](https://api-external-doc.elsanow.co/websocket-scripted)
- **Base URL:** `wss://api.elsanow.io`

#### Tags

- Realtime
- Streaming
- WebSocket
- Unscripted

#### Properties

- [Documentation](https://api-external-doc.elsanow.co/websocket-scripted)
- [Documentation](https://api-external-doc.elsanow.co/websocket-unscripted)
- [OpenAPI](openapi/elsa-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elsa.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elsa.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ELSA Unscripted Speech Assessment API

Open-ended (unscripted) speech assessment. The caller submits spontaneous English audio with no reference script and receives a spoken transcript plus pronunciation, prosody/intonation, fluency, grammar, and vocabulary analysis with improvement suggestions. Batch scoring is a POST to /score_audio_plus.

- **Human URL:** [https://api-external-doc.elsanow.co/elsa/unscripted](https://api-external-doc.elsanow.co/elsa/unscripted)
- **Base URL:** `https://api.elsanow.io/api/v1`

#### Tags

- Unscripted
- Fluency
- Grammar
- Vocabulary

#### Properties

- [Documentation](https://api-external-doc.elsanow.co/elsa/unscripted)
- [API Reference](https://api-external-doc.elsanow.co/category/api)
- [OpenAPI](openapi/elsa-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elsa.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elsa.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/elsa)
- [LinkedIn](https://www.linkedin.com/company/elsacorp)
- [Website](https://www.elsaspeak.com)
- [Documentation](https://api-external-doc.elsanow.co/)
- [Plans](plans/elsa-plans-pricing.yml)
- [Rate Limits](rate-limits/elsa-rate-limits.yml)
- [Fin Ops](finops/elsa-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
