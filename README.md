# llm_comparison

## シンプル版（SPECS & PRICE + CODING）

- 左固定: **Opus4.6 / Sonnet4.6 / Opus4.5 / Sonnet4.5**
- その後は価格感ベースで並び替え（**Qwen3.6 Plus は Kimi K2.5 と MiniMax M2.7 の間**）
- ローカル可能な **Qwen3.6-35B-A3B / Qwen3.6-27B は右側固定**
- `*` は推計/条件付き値、`—` は未公開または確認不能

### モデル順

1. Opus4.6
2. Sonnet4.6
3. Opus4.5
4. Sonnet4.5
5. Kimi K2.6
6. Kimi K2.5
7. Qwen3.6 Plus
8. MiniMax M2.7
9. MiniMax M2.5
10. GLM-5.1
11. GLM-5
12. Step 3.5 Flash
13. Qwen3.6-35B-A3B (LOCAL可)
14. Qwen3.6-27B (LOCAL可)

### SPECS & PRICE + CODING（HTML同等テキスト / Summary除く）

| 項目 | Opus4.6 | Sonnet4.6 | Opus4.5 | Sonnet4.5 | Kimi K2.6 | Kimi K2.5 | Qwen3.6 Plus | MiniMax M2.7 | MiniMax M2.5 | GLM-5.1 | GLM-5 | Step 3.5 Flash | Qwen3.6-35B-A3B | Qwen3.6-27B |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **──── 基本情報** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 開発元 | Anthropic | Anthropic | Anthropic | Anthropic | Moonshot | Moonshot | Alibaba | MiniMax | MiniMax | Z AI | Z AI | StepFun | Alibaba | Alibaba |
| リリース | 2026-02-05 | 2026-02-17 | 2025-11 (言及) | 2025-09-29 | 2026-04-20 | 2026-01-27 | 2026-04-02 | 2026-03-18 | 2026-02-12 | 2026-04-07 | 2026-02-11 | 2026-01-29 | 2026-04-16 | 2026-04-21 |
| ライセンス | Prop. | Prop. | Prop. | Prop. | Mod.MIT | Mod.MIT | Prop. | 非商用 | OW | MIT | MIT | Open | Apache 2.0 | Apache 2.0 |
| 形態 | API | API | API | API | API/OW | API/OW | API | API | API/OW | API/OW | API/OW | API/OW | LOCAL/API | LOCAL/API |
| **──── アーキテクチャ** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 総パラメータ | 非公開 | 非公開 | 非公開 | 非公開 | 1T | 1T | 非公開 | 230B | 230B | 744B | 744B | 196B | 35B | 27B |
| アクティブParam | — | — | — | — | 32B | 32B | — | 10B | 10B | 40B | 40B | 11B | 3B | 27B(Dense) |
| 構造 | ? | ? | ? | ? | MoE | MoE | Hybrid(DeltaNet+MoE) | MoE | MoE | MoE | MoE | MoE(SWA 3:1) | MoE(DeltaNet+MoE) | Dense(DeltaNet+Attn) |
| コンテキスト長 | 1M(β) | 1M(β)/200K | 200K | 200K | 256K | 256K | 1M native | 200K | 200K | 200K | 200K | 256K | 262K→1M(YaRN) | 262K→1M(YaRN) |
| マルチモーダル | テキスト・画像 | テキスト・画像 | テキスト・画像 | テキスト・画像 | テキスト・画像・動画 | テキスト・画像 | テキスト・画像・動画 | テキストのみ | テキストのみ | テキストのみ | テキストのみ | テキストのみ | テキスト・画像・動画 | テキスト・画像・動画 |
| **──── 料金 ($/M tokens)** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| Input ($/M) | — | 3.00 | — | 3.00 | 0.60 | 0.60 | 0.325 | 0.30 | 0.30 | 0.95 | 1.00 | 0.10 | 0.163 | 未発表 |
| Output ($/M) | — | 15.00 | — | 15.00 | 2.80 | 2.50 | 1.95 | 1.20 | 1.20 | 3.15 | 3.20 | 0.30 | 1.30 | 未発表 |
| Input コスト比 (Sonnet4.6=1.0) | — | x1.0 | — | x1.0 | x5.0 | x5.0 | x9.2 | x10 | x10 | x3.2 | x3.0 | x30 | x18.5 | ∞(LOCAL) |
| Output コスト比 (Sonnet4.6=1.0) | — | x1.0 | — | x1.0 | x5.4 | x6.0 | x7.7 | x12.5 | x12.5 | x4.8 | x4.7 | x50 | x11.5 | ∞(LOCAL) |
| **──── 推論速度** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 出力速度 (t/s) | — | ~55* | — | — | — | 37 | 53 | 50 | 65 | 46 | 62 | 183 | 215 | — |
| TTFT (s) | — | ~1.5* | — | — | — | 2.82 | 2.82 | 2.10 | 1.85 | 1.68 | 1.72 | 1.08 | 2.67 | — |
| AA Intelligence Index | — | 52 | — | — | — | 47 | 50 | 50 | 42 | 51 | 50 | 38 | 43 | — |
| **──── 実世界SW開発** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| SWE-bench Verified (%) | 81.42* | 79.6 | — | 77.2 | 80.2 | 76.8 | 78.8 | 未公開 | 80.2 | 77.8 | 77.8 | 74.4 | 73.4 | 77.2 |
| SWE-bench Pro (%) | — | ~60* | — | — | 58.6 | — | — | 56.2 | — | 58.4 | — | — | — | 53.5 |
| Terminal-Bench 2.0 (%) | 首位(数値未公開) | 59.1 | — | — | 66.7 | — | 61.6 | 57.0 | — | — | — | 51.0 | 51.5 | 59.3 |
| SWE-bench Multilingual (%) | — | — | — | — | 76.7 | 73.0 | — | 76.5 | — | — | — | — | — | — |
| **──── コーディング能力** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| LiveCodeBench (%) | — | — | — | — | — | 85.0 | — | — | — | — | 52.0 | 86.4 | — | — |
| SkillsBench (%) | — | — | — | — | — | — | — | — | — | — | — | — | 40.6 | 48.2 |
| MCPMark (%) | 62.7* | — | — | — | — | — | — | — | — | — | — | — | 37.0 | — |
| OSWorld Verified (%) | — | — | — | 61.4 | — | — | — | — | — | — | — | — | — | — |

### 参考ソース（今回追記分）

- Sonnet 4.5: SWE-bench Verified **77.2%**, OSWorld **61.4%**, 価格 **$3/$15**, リリース **2025-09-29**
  - https://raw.githubusercontent.com/Java-Edge/Java-Interview-Tutorial/bbf8d8e4480583c2986e1afb00137aa2d103044f/docs/md/AI/llm/claude-4-5-sonnet.md
- Sonnet 4.6: リリース **2026-02-17**, 価格 **$3/$15**
  - https://raw.githubusercontent.com/Java-Edge/Java-Interview-Tutorial/bbf8d8e4480583c2986e1afb00137aa2d103044f/docs/md/AI/llm/claude-sonnet-4-6.md
- Opus 4.6: リリース **2026-02-05**, SWE-bench Verified 観測値 **81.42%***, MCP Atlas **62.7%***, Terminal-Bench 2.0 **首位(数値未公開)**
  - https://raw.githubusercontent.com/Java-Edge/Java-Interview-Tutorial/bbf8d8e4480583c2986e1afb00137aa2d103044f/docs/md/AI/llm/claude-opus-4-6.md

