# Lumi model assets

Public, download-only home for the on-device model files the Lumi app fetches at first run (voice and avatar assets).
No application source code lives here.

| Asset | Release | Licence | Notes |
|---|---|---|---|
| `model.fconv.onnx` | `kokoro-fconv-v1` | Apache-2.0 (Kokoro-82M v1.0; sherpa-onnx export) | Kokoro int8 export with its convolutions dequantised to float. Same weights, about 3× faster synthesis on mobile CPUs. SHA-256 `4f4c2f5140d9753f87eeb955d69bac87c6d3e2c2f12ac82b1d26ce1f388c880b`, 278,165,761 bytes. |

Every file is pinned by SHA-256 in the app, and the app refuses anything that doesn't match.
Upstream: Kokoro-82M by hexgrad (Apache-2.0); int8 multi-language export by csukuangfj (sherpa-onnx, Apache-2.0).
