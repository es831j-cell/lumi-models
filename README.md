# Lumi model assets

Public, download-only home for the on-device model files the Lumi app fetches at first run (voice and avatar assets).
No application source code lives here.

| Asset | Release | Licence | Notes |
|---|---|---|---|
| `model.fconv.onnx` | `kokoro-fconv-v1` | Apache-2.0 (Kokoro-82M v1.0; sherpa-onnx export) | Kokoro int8 export with its convolutions dequantised to float. Same weights, about 3× faster synthesis on mobile CPUs. SHA-256 `4f4c2f5140d9753f87eeb955d69bac87c6d3e2c2f12ac82b1d26ce1f388c880b`, 278,165,761 bytes. |
| `wardrobe.json` | `humanoid-pack-v2` | CC0 | Wardrobe catalogue (pieces, presets, backgrounds, credits). 17,768 bytes. SHA-256 `b954aa701c0e2f1603a0c06c32e494d7f38727e89d308059be26f3347ef65d7b` |
| `thumbs.jpg` | `humanoid-pack-v2` | CC0 + CC-BY (renders of the pack assets) | Wardrobe thumbnail atlas. 96,880 bytes. SHA-256 `56f192b12b4eb67e693b435034bf47fb4e882489de239d26138313b6a187ef81` |
| `lumi_humanoid.glb` | `humanoid-pack-v2` | CC0 + CC-BY 2.5 SE / CC BY 4.0 (MakeHuman community assets; see release notes) | Rigged, animated humanoid model with wardrobe pieces. 8,717,196 bytes. SHA-256 `a594428d305b75432dd8e2e7689dd28257e441876967cdf50b189374fe1b611f` |
| `bg_lounge_ibl.ktx` | `humanoid-pack-v2` | generated (own work), CC0 | Background lighting (Filament IBL). 522,620 bytes. SHA-256 `742efd31a181ef24c8ecb8b1340d771003af19dcfb24955d2e7ae6396136f096` |
| `bg_lounge_skybox.jpg` | `humanoid-pack-v2` | generated (own work), CC0 | Background backdrop. 75,460 bytes. SHA-256 `64e01bf3ef90aba92010009f0e4458c17e3685a50094e41100fe049b9a56c421` |
| `bg_city_ibl.ktx` | `humanoid-pack-v2` | Poly Haven shanghai_bund, CC0 | Background lighting (Filament IBL). 522,600 bytes. SHA-256 `66b77862deb3bfa4031f40b5ab8f075e1190a85704a4dc13c043948a8c1552df` |
| `bg_city_skybox.jpg` | `humanoid-pack-v2` | Poly Haven shanghai_bund, CC0 | Background backdrop. 100,007 bytes. SHA-256 `e931ecb942d0686be4303838f3fe274f8c3bcd1c92bcc3fa331406ef4e193bb9` |
| `bg_garden_ibl.ktx` | `humanoid-pack-v2` | Poly Haven chinese_garden, CC0 | Background lighting (Filament IBL). 522,616 bytes. SHA-256 `7db39a1886be11cdd03a60cb8a7455536962c540615a27a19c56dea92b1e9633` |
| `bg_garden_skybox.jpg` | `humanoid-pack-v2` | Poly Haven chinese_garden, CC0 | Background backdrop. 106,505 bytes. SHA-256 `162a2d3e59f00f647b8affbd43d6eb03224c07b28b2530d8e4d8b45e8eb06eae` |
| `bg_studio_ibl.ktx` | `humanoid-pack-v2` | Poly Haven monochrome_studio_02, CC0 | Background lighting (Filament IBL). 522,608 bytes. SHA-256 `2117fafee0d8d2143aa66e7fc3b4a1f76fe6e7de3f7b0e6742269ad99ef3dcc1` |
| `bg_studio_skybox.jpg` | `humanoid-pack-v2` | Poly Haven monochrome_studio_02, CC0 | Background backdrop. 68,613 bytes. SHA-256 `a2b03c43b00ac9a73139a971b532778cac46837d81165c3f8b192edc5bcb527b` |
| `bg_dusk_ibl.ktx` | `humanoid-pack-v2` | generated (own work), CC0 | Background lighting (Filament IBL). 522,628 bytes. SHA-256 `ef8f659b25b8c1de2b84a519286a814f6a1c7fbb757895da6580401f4361162c` |
| `bg_dusk_skybox.jpg` | `humanoid-pack-v2` | generated (own work), CC0 | Background backdrop. 50,056 bytes. SHA-256 `6159755b13557a3edaa38922cf081439097ebf9853b64cdb330800fc8c1a3a13` |

Every file is pinned by SHA-256 in the app, and the app refuses anything that doesn't match.
Upstream (voice): Kokoro-82M by hexgrad (Apache-2.0); int8 multi-language export by csukuangfj (sherpa-onnx, Apache-2.0).

Humanoid pack `humanoid-pack-v2` (`lumi-humanoid@fd536d486bf1636c`, 13 files, 11,845,557 bytes): MakeHuman base mesh, rig, skin, eyes, brows, lashes, teeth and face units are CC0 (MakeHuman system/community asset packs); five community garments and the hair are CC-BY (Elvaerwyn: elvs_50s_updo, elvs_hooded_sweat_jacket1, elvs_goddess_dress1; punkduck: punkduck_lace_up_blouse, CC BY 4.0; Mindfront: mindfront_cardigan_long_open_front, CC BY 4.0), credited in the app under Wardrobe > Credits; all other garments CC0; three backgrounds are Poly Haven HDRIs (CC0) and two are generated (CC0). No GPL, AGPL or non-commercial content. The full per-asset ledger is in the release notes.

## Other files the app downloads (not hosted here)

| Asset | Host (pinned commit) | Licence | SHA-256 |
|---|---|---|---|
| Kokoro int8 `model.int8.onnx`, `voices.bin`, `tokens.txt`, `lexicon-gb-en.txt`, `lexicon-us-en.txt` | huggingface.co/csukuangfj/kokoro-int8-multi-lang-v1_0 @ `2a360693d79b88b49b88e29aec2b53577f41f206` | Apache-2.0 | `4b86207e…`, `1c5a5b98…`, `6ebb6bb2…`, `c4cbb373…`, `7daaab53…` |
| Local brain (small) `Qwen2_0.5B_Instruct.litertlm` | huggingface.co/litert-community/Qwen2-0.5B-Instruct @ `13aab3e522828d85fa178d885716ab858a715149` | Apache-2.0 | `0f01cc004b8eb62b92ba6be85ed05a248ba0d2f78af94c4949b313eccfb4c157` |
| Local brain (large) `Qwen2.5-1.5B-Instruct_multi-prefill-seq_q8_ekv4096.litertlm` | huggingface.co/litert-community/Qwen2.5-1.5B-Instruct @ `19edb84c69a0212f29a6ef17ba0d6f278b6a1614` | Apache-2.0 | `faa60663b333290c1496c499828b21d3e3254a788cacd8cce917ce0f761a2dc9` |
| Meaning model `onnx/model_qint8_arm64.onnx`, `vocab.txt` | huggingface.co/sentence-transformers/all-MiniLM-L6-v2 @ `1110a243fdf4706b3f48f1d95db1a4f5529b4d41` | Apache-2.0 | `4278337fd0ff3c68bfb6291042cad8ab363e1d9fbc43dcb499fe91c871902474`, `07eced375cec144d27c900241f3e339478dec958f92fddbc551f295c992038a3` |

The wake word model ships inside the app and is not downloaded.
