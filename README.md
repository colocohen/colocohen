# Aviv Cohen

Author of low-level libraries for Node.js. Pure-JavaScript implementations of core internet protocols - QUIC/HTTP3, TLS, DNSSEC, STUN/TURN, WebRTC, SMTP - alongside supporting libraries for real-time media, data formats, storage, and runtime utilities.

## Projects

### Networking & internet protocols

| Project | Description |
|---|---|
| ⚡ [**quico**](https://github.com/colocohen/quico) | First full QUIC and HTTP/3 implementation in pure JavaScript for Node.js. |
| 🔐 [**lemon-tls**](https://github.com/colocohen/lemon-tls) | TLS 1.3 / 1.2 implementation with full control over cryptographic keys and the record layer. |
| 📜 [**cert-manager**](https://github.com/colocohen/cert-manager) | ACME client with automatic certificate management. Zero dependencies. |
| 🌐 [**dnssec-server**](https://github.com/colocohen/dnssec-server) | Authoritative DNS server with built-in DNSSEC, dynamic zones, and modern record types. |
| 🛰️ [**turn-server**](https://github.com/colocohen/turn-server) | Embeddable STUN/TURN client and server. Full RFC coverage, zero dependencies. |
| 📧 [**email-server**](https://github.com/colocohen/email-server) | Complete mail server in a single Node.js package — SMTP and IMAP. |

### Real-time communication & media

| Project | Description |
|---|---|
| 📡 [**stable-webrtc**](https://github.com/colocohen/stable-webrtc) | WebRTC for Node.js and browsers, focused on signaling reliability and connection state in production. |
| 🎥 [**webrtc-server**](https://github.com/colocohen/webrtc-server) | Server-side WebRTC stack with a browser-compatible API — SFU, RTP, data channels. |
| 🎙️ [**rtp-packet**](https://github.com/colocohen/rtp-packet) | RTP, RTCP, and SRTP packetization for Node.js. |
| 🎞️ [**media-processing**](https://github.com/colocohen/media-processing) | WebCodecs-compatible API for encoding, decoding, muxing, and demuxing — backed by FFmpeg subprocesses. |

### Data & storage

| Project | Description |
|---|---|
| 💾 [**uni-indexeddb**](https://github.com/colocohen/uni-indexeddb) | Unified key-value storage with the same API across browser (IndexedDB) and server (LevelDB). |
| 🗜️ [**litepack**](https://github.com/colocohen/litepack) | Schema-based binary encoding for JavaScript — compact, fast, zero dependencies. |

### JavaScript primitives & utilities

| Project | Description |
|---|---|
| 🧮 [**bloom-filter-numbers**](https://github.com/colocohen/bloom-filter-numbers) | Bloom filter optimized for numeric IDs, using splitmix64 and XOR fingerprinting. |
| 📏 [**flat-ranges**](https://github.com/colocohen/flat-ranges) | Merge, subtract, and invert flat numeric ranges. |
| 🎲 [**pcg64dxsm**](https://github.com/colocohen/pcg64dxsm) | Bit-compatible PCG64-DXSM PRNG. WASM-accelerated, NumPy-compatible. |
| 🔔 [**deep-events**](https://github.com/colocohen/deep-events) | Path-based event system covering events, state, DOM, workers, and lifecycle cleanup. |
| 🌍 [**hint-locale**](https://github.com/colocohen/hint-locale) | Locale detection from browser signals and HTTP headers — country, language, confidence scoring. |
| 🧭 [**js-runtime-environment**](https://github.com/colocohen/js-runtime-environment) | Detect the JavaScript runtime — Browser, Node.js, Deno, Bun, Electron, and more. |

## Contributing

Issues, pull requests, and design discussions are welcome on every repository. Particular interest: protocol-level review, edge-case reports, and collaboration with teams running these stacks in production.

## Sponsorship

If your team relies on any of these libraries, sponsorship through [GitHub Sponsors](https://github.com/sponsors/colocohen) supports continued development and maintenance.
