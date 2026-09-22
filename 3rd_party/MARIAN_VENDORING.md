# Vendored Marian sources

Marian and its nested dependencies are tracked directly by this repository.
Preserve each dependency’s license when modifying or redistributing these sources.

## Upstream revisions

Paths below are relative to `3rd_party/marian-dev`.

| Path | Repository | Commit |
| --- | --- | --- |
| `.` | https://github.com/browsermt/marian-dev | `2781d735d4a10dca876d61be587afdab2726293c` |
| `examples` | https://github.com/marian-nmt/marian-examples | `c19b7814d71febf1053bd93af6ac314b46204092` |
| `regression-tests` | https://github.com/marian-nmt/marian-regression-tests | `16914ae94c80f338c678f0461c4e45965149f6aa` |
| `src/3rd_party/fbgemm` | https://github.com/marian-nmt/FBGEMM | `0e33146d3e7f070c7de9494efef49147a9d20558` |
| `src/3rd_party/fbgemm/third_party/asmjit` | https://github.com/asmjit/asmjit.git | `4da474ac9aa2689e88d5e40a2f37628f302d7e3c` |
| `src/3rd_party/fbgemm/third_party/cpuinfo` | https://github.com/pytorch/cpuinfo | `d5e37adf1406cf899d7d9ec1d317c47506ccb970` |
| `src/3rd_party/fbgemm/third_party/googletest` | https://github.com/google/googletest | `0fc5466dbb9e623029b1ada539717d10bd45e99e` |
| `src/3rd_party/intgemm` | https://github.com/kpu/intgemm | `f7401513da71758dacce52fed1c7855549abee59` |
| `src/3rd_party/nccl` | https://github.com/marian-nmt/nccl | `7d3486128ebc865b9f2cad63a5cfd3a8f6abcb5a` |
| `src/3rd_party/onnxjs` | https://github.com/browsermt/onnxjs | `924924b08e9596b41aeebada4a172f026be95f5a` |
| `src/3rd_party/onnxjs/deps/eigen` | https://github.com/abhi-agg/eigen-git-mirror.git | `fff37f4ca0397af9ed7e04f3bd6b893a1ea2b08e` |
| `src/3rd_party/ruy` | https://github.com/google/ruy | `2d950b3bfa7ebfbe7a97ecb44b1cc4da5ac1d6f0` |
| `src/3rd_party/ruy/third_party/cpuinfo` | https://github.com/pytorch/cpuinfo | `5916273f79a21551890fd3d56fc5375a78d1598d` |
| `src/3rd_party/ruy/third_party/googletest` | https://github.com/google/googletest | `6c58c11d5497b6ee1df3cb400ce30deb72fc28c0` |
| `src/3rd_party/sentencepiece` | https://github.com/browsermt/sentencepiece | `ae41b7740d7006596bb9257e83340b2620db9d00` |
| `src/3rd_party/simd_utils` | https://github.com/browsermt/simd_utils.git | `d0793d86aea9036a5bc77b9ca7791dff024168ca` |
| `src/3rd_party/simple-websocket-server` | https://github.com/marian-nmt/Simple-WebSocket-Server | `417a2a9e9dbd720b8d2dfa1dafe57cf1b37ca0d7` |

## Local changes

- zlib: exclude modern Apple platforms from the classic Mac OS `fdopen` fallback.
- SentencePiece: store the script sentinel in an integer instead of an out-of-range enum.
- Marian: use compile-time constants for stack trace buffer sizes.
- CMake: use the recorded Marian revision and do not update vendored dependencies through Git.

Edit and commit these sources in the main repository. To import an upstream update,
review the source changes, retain the local fixes, and update this record and
`marian-dev/UPSTREAM_REVISION` as applicable.
