# WASI proposals

WASI APIs are developed as proposals. These proposals go through 5 phases of development (following the [WebAssembly CG's Phase Process]).

You can learn more about contributing new proposals (and other ways to contribute) in our [Contributing] guide.

[WebAssembly CG's Phase Process]: https://github.com/WebAssembly/meetings/blob/main/process/phases.md
[Contributing]: https://github.com/WebAssembly/WASI/blob/main/Contributing.md

## Active Proposals

### Phase 5 - The Feature is Standardized (WG)

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |

### Phase 4 - Standardize the Feature (WG)

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |

### Phase 3 - Implementation Phase (CG + WG)

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |

### Phase 2 - Proposed Spec Text Available (CG + WG)

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |
| [I/O][wasi-io]                                                                 | Dan Gohman                             |          |
| [Filesystem][wasi-filesystem]                                                  | Dan Gohman                             |          |
| ["Classic" Command-Line][wasi-classic-command] (Legacy, to be deprecated in Q4 2022)| Dan Gohman                             |          |
| [Clocks][wasi-clocks]                                                          | Dan Gohman                             |          |
| [Random][wasi-random]                                                          | Dan Gohman                             |          |
| [Handle Index][wasi-handle-index]                                              | Dan Gohman                             |          |
| [Poll][wasi-poll]                                                              | Dan Gohman                             |          |
| [Machine Learning (wasi-nn)][wasi-nn]                                          | Andrew Brown and Mingqiu Sun           |          |

### Phase 1 - Feature Proposal (CG)

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |
| [Blob Store][wasi-blob-store]                                                  | Jiaxiao Zhou, Dan Chiarlone, David Justice |          | 
| [Crypto][wasi-crypto]                                                          | Frank Denis and Daiki Ueno             |          |
| [Distributed Lock Service][wasi-distributed-lock-service]                      | Jiaxiao Zhou, Dan Chiarlone, David Justice |          |
| [gRPC][wasi-grpc]                                                              | Jiaxiao Zhou, Dan Chiarlone, David Justice, Piotr Sikora |          |
| [HTTP][wasi-http]                                                              | Piotr Sikora, Jiaxiao Zhou, Dan Chiarlone, David Justice |          |
| [Key-value Store][wasi-kv-store]                                               | Jiaxiao Zhou, Dan Chiarlone, David Justice |          |
| [Message Queue][wasi-message-queue]                                            | Jiaxiao Zhou, Dan Chiarlone, David Justice |          |
| [Parallel][wasi-parallel]                                                      | Andrew Brown                           |          |
| [Pub/sub][wasi-pubsub]                                                         | Jiaxiao Zhou, Dan Chiarlone, David Justice |          | 
| [Runtime Config][wasi-runtime-config]                                          | Jiaxiao Zhou, Dan Chiarlone, David Justice |          | 
| [Sockets][wasi-sockets]                                                        | Dave Bakker                            |          |
| [SQL][wasi-sql]                                                                | Jiaxiao Zhou, Dan Chiarlone, David Justice |          |
| [Threads][wasi-threads]                                                        | Alexandru Ene, Marcin Kolny, Andrew Brown |          |
| [URL][wasi-url]                                                                | George Kulakowski and Radu Matei       |          |

### Phase 0 - Pre-Proposal (CG)

**Note:** The pre-proposal phase is simply meant as a way to share ideas. This means that there may be overlap between pre-proposals. It also means that the WASI subgroup has not yet decided that the pre-proposal is in scope for WASI.

| Proposal                                                                       | Champion                               | Versions |
| ------------------------------------------------------------------------------ | -------------------------------------- | -------- |
| [singlestore-labs/wasi-data][wasi-data]                                        | Bailey Hayes                           |          |
| [proxy-wasm/spec][wasi-proxy-wasm] (will advance as multiple, smaller proposals)    | Piotr Sikora                           |          |

## Versioning

Once a proposal reaches Phase 3, we expect the champions to start creating releases, following the conventions of semantic versioning (semver). Releases for active proposals are linked in the chart above.

Proposals remain in the 0.x semver range until they reach Phase 5 and are fully standardized. At that point, a 1.0 release should be made available.

For some APIs, it makes sense to add new features after the API itself has reached Phase 5. These feature additions should go through the same standardization process. Once they have reached Phase 5, the minor version number of the release should be incremented.

Some APIs may require backwards-incompatible changes over time. In these cases, we allow proposals to increment the major version number _only if_ the old API can be implmented in terms of the new API. As part of the new version, champions are expected to provide a tool that enables this backwards-compatibility. If that is not possible, then a new API proposal with a new name should be started. The original API can then be deprecated over time if it makes sense to do so.

[WebAssembly CG Phases process]: https://github.com/WebAssembly/meetings/blob/master/process/phases.md
[witx]: https://github.com/WebAssembly/WASI/blob/main/tools/witx-docs.md
[ephemeral/snapshot/old process]: https://github.com/WebAssembly/WASI/blob/master/phases/README.md

[wasi-blob-store]: https://github.com/WebAssembly/wasi-blob-store
[wasi-clocks]: https://github.com/WebAssembly/wasi-clocks
[wasi-classic-command]: https://github.com/WebAssembly/wasi-classic-command
[wasi-crypto]: https://github.com/WebAssembly/wasi-crypto
[wasi-data]: https://github.com/singlestore-labs/wasi-data
[wasi-distributed-lock-service]: https://github.com/WebAssembly/wasi-distributed-lock-service
[wasi-filesystem]: https://github.com/WebAssembly/wasi-filesystem
[wasi-grpc]: https://github.com/WebAssembly/wasi-grpc
[wasi-handle-index]: https://github.com/WebAssembly/wasi-handle-index
[wasi-http]: https://github.com/WebAssembly/wasi-http
[wasi-io]: https://github.com/WebAssembly/wasi-io
[wasi-kv-store]: https://github.com/WebAssembly/wasi-kv-store
[wasi-message-queue]: https://github.com/WebAssembly/wasi-message-queue
[wasi-misc]: https://github.com/WebAssembly/wasi-misc
[wasi-threads]: https://github.com/WebAssembly/wasi-native-threads
[wasi-nn]: https://github.com/WebAssembly/wasi-nn
[wasi-random]: https://github.com/WebAssembly/wasi-random
[wasi-parallel]: https://github.com/WebAssembly/wasi-parallel
[wasi-poll]: https://github.com/WebAssembly/wasi-poll
[wasi-proxy-wasm]: https://github.com/proxy-wasm/spec
[wasi-pubsub]: https://github.com/WebAssembly/wasi-pubsub
[wasi-runtime-config]: https://github.com/WebAssembly/wasi-runtime-config
[wasi-sockets]: https://github.com/WebAssembly/wasi-sockets
[wasi-sql]: https://github.com/WebAssembly/wasi-sql
[wasi-url]: https://github.com/WebAssembly/wasi-url
