# Mac Studio field report - 2026-07-dry-run

Generated: 2026-07-01T00:00:00.000Z

## Verdict

No model recommendation is publishable from this release dataset. All four public-safe workload families contain current local evidence, but none has a row with complete claim provenance. The release therefore withholds recommendations rather than inferring missing quantization or treating incomplete workload coverage as complete.

The useful finding this cycle is about evidence readiness: the internal ranking surface has substantial scored evidence, while the release plane correctly refuses to turn opaque model names, runtime identifiers, filenames, or paths into public provenance.

## Interpretation boundaries

Readers may conclude that the release gate can represent current local evidence without promoting incomplete rows into recommendations. Readers may also conclude that explicit quantization provenance and complete workload coverage must be added upstream before these rows support public model recommendations.

Readers may not conclude that an unlisted model performed poorly, that the highest internal rank is a public recommendation, or that encoded strings in model and runtime identifiers establish quantization. This dry run makes no comparative model-quality claim.

## Recommendations by workload

| Workload | Recommended model | Runtime | Quantization | Hardware | Repeats |
| --- | --- | --- | --- | --- | ---: |
| harbor terminal workflow v1 | _no claim-ready recommendation this cycle_ | - | - | - | 0 |
| public anchor swebench holdout v1 | _no claim-ready recommendation this cycle_ | - | - | - | 0 |
| public anchor swebench mini v1 | _no claim-ready recommendation this cycle_ | - | - | - | 0 |
| swebench verified v1 | _no claim-ready recommendation this cycle_ | - | - | - | 0 |

## Challengers and limitations

### harbor terminal workflow v1

| Model | Rank | Claim-ready | Limitation |
| --- | ---: | --- | --- |
| Deepreinforce AI Ornith 1 0.397B | 1 | no | not claim-ready (quantization, hardwareProfile) |
| Prefeitura Rio Rio 3 5 Open 397B | 2 | no | not claim-ready (quantization, hardwareProfile) |
| Mimo V2 5 Coder (Q2) | 3 | no | not claim-ready (quantization, hardwareProfile) |
| Step3 7 Flash (BF16) | 4 | no | not claim-ready (quantization, hardwareProfile) |
| Kimi K2 7 Code | 5 | no | not claim-ready (quantization, hardwareProfile) |
| K Xl MiniMax M3 Ud Q8 K Xl | 6 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B (IQ4_XS) | 7 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.5 35B A3b (BF16) | 8 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Darwin 27B Opus I1 (Q6_K) | 9 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| GLM 5 2 (UD Q4_K_S) | 10 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| Qwopus3 6.27B V2 (Q8_0) | 11 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| Qwopus3 6.27B V2 Mtp (BF16) | 12 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| Qwopus3 6.35B A3b V1 (Q8_0) | 13 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| Gemma 4.12B It Ud Q8 K Xl | 14 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| GLM 5 1 (UD Q4_K_S) | 15 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 2/8 declared workloads |
| Kimi K2.6 RAM-344 GGUF (local) | 16 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B NEO-CODE IQ4 GGUF | 17 | no | not claim-ready (quantization, hardwareProfile) |
| Gemma 4.31B It Claude Opus Distill | 18 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| HY MT2 1.8B (Q8_0) | 19 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 2/8 declared workloads |
| HY MT2 7B (Q8_0) | 20 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Gemma 4.12B It (BF16) | 21 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Gemma 4.12B It Qat Ud Q4 K Xl | 22 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| Qwen3.5 397B A17b Mtp | 23 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Qwen3 Coder Next (UD IQ4_XS) | 24 | no | not claim-ready (quantization, hardwareProfile) |

### public anchor swebench holdout v1

| Model | Rank | Claim-ready | Limitation |
| --- | ---: | --- | --- |
| Awaxis Kr 31B | 1 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Deepreinforce AI Ornith 1 0.397B | 2 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Prefeitura Rio Rio 3 5 Open 397B | 3 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Carnice V2 27B | 4 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| Local Direct Glm52 Oq4e Mtp | 5 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Gemma 4.31B It | 6 | no | not claim-ready (quantization, hardwareProfile) |
| Kimi K2.6 MLX 3 5bit Inf | 7 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| Qwopus3 6.35B A3b V1 (Q8_0) | 8 | no | not claim-ready (quantization, hardwareProfile) |
| Community Kimi K2.6 MLX DQ3 K M (Q8) | 9 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Community Qwen3.5 35B A3b 4bit | 10 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| GLM Collection Mxfp4 GLM 5 2 Mixq Mxfp4 | 11 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Kimi K2 7 Code MLX 3 6bit | 12 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Nex N2 Pro MLX 5 3bit Vision | 13 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| GLM 5 1 (UD Q4_K_S) | 14 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 2/8 declared workloads |
| GLM 5 2 (UD Q4_K_S) | 15 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| Kimi K2 7 Code | 16 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| K Xl MiniMax M3 Ud Q5 K Xl | 17 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Qwen3.5 397B A17b Mtp | 18 | no | not claim-ready (quantization, hardwareProfile) |
| Qwopus3 6.27B V2 (Q8_0) | 19 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Gemma 4.26B A4b It | 20 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Kimi K2.6 RAM-344 GGUF (local) | 21 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| GLM 5 2 Ram Local Knee | 22 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| Qwopus3 6.27B V2 Mtp (BF16) | 23 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Step3 7 Flash (BF16) | 24 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Darwin 27B Opus I1 (Q6_K) | 25 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| Qwen3.6 27B (IQ4_NL) | 26 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Gemma 4.31B It Claude Opus Distill | 27 | no | not claim-ready (quantization, hardwareProfile) |
| Mimo V2 5 Coder (Q2) | 28 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Qwen3.6 27B (IQ4_XS) | 29 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Qwen3 Coder Next (UD IQ4_XS) | 30 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Qwen3.6 27B NEO-CODE IQ4 GGUF | 31 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Nex N2 Pro (IQ4_NL) | 32 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |
| HY MT2 1.8B (Q8_0) | 33 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 3/8 declared workloads |

### public anchor swebench mini v1

| Model | Rank | Claim-ready | Limitation |
| --- | ---: | --- | --- |
| Kimi K2.6 RAM-344 GGUF (local) | 1 | no | not claim-ready (quantization, hardwareProfile) |
| Awaxis Kr 31B | 2 | no | not claim-ready (quantization, hardwareProfile) |
| GLM 5 2 Ram Local Knee | 3 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 5/8 declared workloads |
| Deepreinforce AI Ornith 1 0.397B | 4 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| Prefeitura Rio Rio 3 5 Open 397B | 5 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Gemma 4.31B It | 6 | no | not claim-ready (quantization, hardwareProfile) |
| Qwopus3 6.27B V2 (Q8_0) | 7 | no | not claim-ready (quantization, hardwareProfile) |
| Qwopus3 6.35B A3b V1 (Q8_0) | 8 | no | not claim-ready (quantization, hardwareProfile) |
| Mimo V2 5 Coder (Q2) | 9 | no | not claim-ready (quantization, hardwareProfile) |
| Community Kimi K2.6 MLX DQ3 K M (Q8) | 10 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Kimi K2 7 Code MLX 3 6bit | 11 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| Step3 7 Flash (BF16) | 12 | no | not claim-ready (quantization, hardwareProfile) |
| K Xl MiniMax M3 Ud Q8 K Xl | 13 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 7/8 declared workloads |
| Qwen3.5 397B A17b Mtp | 14 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B (BF16) | 15 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B (IQ4_NL) | 16 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B (IQ4_XS) | 17 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3.6 27B (Q3_K_M) | 18 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Qwen3.6 27B (Q4_0) | 19 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |
| Qwen3 Coder Next (BF16) | 20 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3 Coder Next (Q4_1) | 21 | no | not claim-ready (quantization, hardwareProfile) |
| Qwen3 Coder Next (UD IQ4_XS) | 22 | no | not claim-ready (quantization, hardwareProfile) |
| Darwin 27B Opus I1 (Q6_K) | 23 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| GLM 5 2 (UD Q4_K_S) | 24 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 6/8 declared workloads |
| Gemma 4.26B A4b It | 25 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 4/8 declared workloads |
| Qwopus3 6.27B V2 Mtp (BF16) | 26 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 4/8 declared workloads |
| Qwen3.6 27B NEO-CODE IQ4 GGUF | 27 | no | not claim-ready (quantization, hardwareProfile) |
| Gemma 4.31B It Claude Opus Distill | 28 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 4/8 declared workloads |
| HY MT2 1.8B (Q8_0) | 29 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 1/8 declared workloads |

### swebench verified v1

| Model | Rank | Claim-ready | Limitation |
| --- | ---: | --- | --- |
| Gemma 4.31B It Claude Opus Distill | 1 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Gemma 4.12B It (BF16) | 2 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Gemma 4.12B It Ud Q8 K Xl | 3 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 30/51 declared workloads |
| K Xl MiniMax M3 Ud Q8 K Xl | 4 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 34/51 declared workloads |
| Qwen3 Coder Next (Q4_1) | 5 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Kimi K2 7 Code MLX 3 6bit | 6 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Qwen3.5 397B A17b Mtp | 7 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Community Kimi K2.6 MLX DQ3 K M (Q8) | 8 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 29/51 declared workloads |
| Step3 7 Flash (BF16) | 9 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Awaxis Kr 31B | 10 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Gemma 4.31B It | 11 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Prefeitura Rio Rio 3 5 Open 397B | 12 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 29/51 declared workloads |
| GLM 5 2 (UD Q4_K_S) | 13 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 46/51 declared workloads |
| Qwen3.6 27B (Q4_0) | 14 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 17/51 declared workloads |
| Qwopus3 6.27B V2 Mtp (BF16) | 15 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 15/51 declared workloads |
| Qwopus3 6.35B A3b V1 (Q8_0) | 16 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 35/51 declared workloads |
| Qwopus3 6.27B V2 (Q8_0) | 17 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Kimi K2.6 RAM-344 GGUF (local) | 18 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Mimo V2 5 Coder (Q2) | 19 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Qwen3 Coder Next (UD IQ4_XS) | 20 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Qwen3.6 27B (IQ4_XS) | 21 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Qwen3.6 27B NEO-CODE IQ4 GGUF | 22 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Qwen3.6 27B (IQ4_NL) | 23 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Gemma 4.26B A4b It | 24 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Qwen3.6 27B (Q3_K_M) | 25 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 2/51 declared workloads |
| Mistralai Devstral Small 2.24B Instruct 2512 Q4 0 | 26 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 31/51 declared workloads |
| Darwin 27B Opus I1 (Q6_K) | 27 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 42/51 declared workloads |
| HY MT2 1.8B (Q8_0) | 28 | no | not claim-ready (quantization, hardwareProfile, workloadCoverage); covered 17/51 declared workloads |

## What changed

_First release: no prior dataset to diff against._

## Corrections

_No corrections for this release._

<!-- release:attribution-footer -->
## About and sponsor

This is an independent, evidence-backed evaluation. The links below are
clearly labeled and separate from the benchmark evidence and verdicts above.

- [House of Vibe](https://houseofvibe.ai/?utm_source=houseofvibe.ai&utm_medium=report&utm_campaign=2026-07-dry-run)
- [Will Mitchell](https://willmitchell.com/?utm_source=willmitchell.com&utm_medium=report&utm_campaign=2026-07-dry-run)

Authored reports and verdict prose are licensed CC BY-ND 4.0; code and tooling are MIT.
<!-- /release:attribution-footer -->

