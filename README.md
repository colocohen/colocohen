# Aviv Cohen

Author of low-level libraries for Node.js. Pure-JavaScript implementations of core internet protocols - QUIC/HTTP3, TLS, DNSSEC, STUN/TURN, WebRTC, SMTP - alongside supporting libraries for real-time media, data formats, storage, and runtime utilities.

These libraries share a single principle: every layer of the stack should be controllable from code. Running nginx, BIND, Postfix, or coturn next to your Node.js application is the standard answer - but it limits you to what their configuration files allow, makes the system hard to extend in directions the original authors didn't anticipate, and puts a process boundary between every layer. Each library here removes that compromise. The protocol becomes a function you write, not a config you maintain - DNS records computed at runtime per query, cryptographic keys held in your own code, every packet visible to your handler.

The libraries are also intentionally narrow. Each one implements its protocol and stops there. Every decision the protocol doesn't dictate - storage, business logic, signaling transport, architectural choices - stays in your code. They are libraries to compose, not frameworks to inherit.

When that's true, infrastructure stops being something you assemble around your code and becomes part of it. A two-person team can ship a system that used to require a dedicated SRE. Edge deployments don't have to ship without DNS, mail, or media handling. Geo-routing, canary releases, and health-driven failover stop being managed-service features and become a few lines of JavaScript. When something fails at the protocol level, you read source - your source. That's the Node.js these libraries are working toward.

## Projects

### Networking & internet protocols

| Project | Description |
|---|---|
| ⚡ [**quico**](https://github.com/colocohen/quico) | First full QUIC and HTTP/3 implementation in pure JavaScript for Node.js. |
| 🔐 [**lemon-tls**](https://github.com/colocohen/lemon-tls) | TLS 1.3 / 1.2 implementation with full control over cryptographic keys and the record layer. |
| 📜 [**cert-manager**](https://github.com/colocohen/cert-manager) | ACME client with automatic certificate management. Zero dependencies. |
| 🌐 [**dnssec-server**](https://github.com/colocohen/dnssec-server) | Handler-based authoritative DNS - answers computed per query in JavaScript, DNSSEC signed at runtime, no zone files. |
| 🛰️ [**turn-server**](https://github.com/colocohen/turn-server) | Embeddable STUN/TURN client and server. Full RFC coverage, zero dependencies. |
| 📧 [**email-server**](https://github.com/colocohen/email-server) | Full mail stack - SMTP, IMAP, and POP3 (server + client) with DKIM, SPF, DMARC, and MTA-STS built in. |

### Real-time communication & media

| Project | Description |
|---|---|
| 📡 [**stable-webrtc**](https://github.com/colocohen/stable-webrtc) | WebRTC for Node.js and browsers, focused on signaling reliability and connection state in production. |
| 🎥 [**webrtc-server**](https://github.com/colocohen/webrtc-server) | Server-side WebRTC stack with a browser-compatible API - SFU, RTP, data channels. |
| 🎙️ [**rtp-packet**](https://github.com/colocohen/rtp-packet) | RTP, RTCP, and SRTP packetization for Node.js. |
| 🎞️ [**media-processing**](https://github.com/colocohen/media-processing) | WebCodecs-compatible API for encoding, decoding, muxing, and demuxing - backed by FFmpeg subprocesses. |

### Data & storage

| Project | Description |
|---|---|
| 💾 [**uni-indexeddb**](https://github.com/colocohen/uni-indexeddb) | Unified key-value storage with the same API across browser (IndexedDB) and server (LevelDB). |
| 🗜️ [**litepack**](https://github.com/colocohen/litepack) | Schema-based binary encoding for JavaScript - compact, fast, zero dependencies. |
| 🗜️ [**compact-delta**](https://github.com/colocohen/compact-delta) | Generic optimal binary delta compression - auto-picks the smallest encoding (copy/insert, Myers LCS, or raw). |

### JavaScript primitives & utilities

| Project | Description |
|---|---|
| 📏 [**flat-ranges**](https://github.com/colocohen/flat-ranges) | Merge, subtract, and invert flat numeric ranges. |
| 🧮 [**bloom-filter-numbers**](https://github.com/colocohen/bloom-filter-numbers) | Bloom filter optimized for numeric IDs, using splitmix64 and XOR fingerprinting. |
| 🎲 [**pcg64dxsm**](https://github.com/colocohen/pcg64dxsm) | Bit-compatible PCG64-DXSM PRNG. WASM-accelerated, NumPy-compatible. |
| 🔔 [**deep-events**](https://github.com/colocohen/deep-events) | Path-based event system covering events, state, DOM, workers, and lifecycle cleanup. |
| 🌍 [**hint-locale**](https://github.com/colocohen/hint-locale) | Locale detection from browser signals and HTTP headers - country, language, confidence scoring. |
| 🧭 [**js-runtime-environment**](https://github.com/colocohen/js-runtime-environment) | Detect the JavaScript runtime - Browser, Node.js, Deno, Bun, Electron, and more. |

## Contributing

Building production-grade implementations of the entire internet stack in pure JavaScript is more work than one person can finish alone. These projects benefit from anyone willing to read an RFC closely, find the edge case nobody else has hit, or push a library in directions the original draft never imagined. Issues, pull requests, and design discussions are open on every repository - particularly welcome from protocol implementers, security researchers, and engineers running these stacks in production.

## Sponsorship

If your team relies on any of these libraries, sponsorship through [GitHub Sponsors](https://github.com/sponsors/colocohen) supports continued development and maintenance.
