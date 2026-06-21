# ELSA (elsa)

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
