# llm_comparison

## シンプル版（SPECS & PRICE + CODING）

- 左固定: **Opus4.6 / Sonnet4.6 / Opus4.5 / Sonnet4.5**
- その後は価格感ベースで並び替え（**Qwen3.6 Plus は Kimi K2.5 と MiniMax M2.7 の間**）
- ローカル可能な **Qwen3.6-35B-A3B / Qwen3.6-27B は右側固定**
- Opus4.6 / Opus4.5 / Sonnet4.5 は現行データ未掲載のため `—`

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

### SPECS & PRICE（主要項目）

| Model | Input $/M | Output $/M | Context | 形態 |
|---|---:|---:|---|---|
| Opus4.6 | — | — | — | — |
| Sonnet4.6 | 3.00 | 15.00 | 1M(β)/200K | API |
| Opus4.5 | — | — | — | — |
| Sonnet4.5 | — | — | — | — |
| Kimi K2.6 | 0.60 | 2.80 | 256K | API/OW |
| Kimi K2.5 | 0.60 | 2.50 | 256K | API/OW |
| Qwen3.6 Plus | 0.325 | 1.95 | 1M native | API |
| MiniMax M2.7 | 0.30 | 1.20 | 200K | API |
| MiniMax M2.5 | 0.30 | 1.20 | 200K | API/OW |
| GLM-5.1 | 0.95 | 3.15 | 200K | API/OW |
| GLM-5 | 1.00 | 3.20 | 200K | API/OW |
| Step 3.5 Flash | 0.10 | 0.30 | 256K | API/OW |
| Qwen3.6-35B-A3B | 0.163 | 1.30 | 262K→1M(YaRN) | LOCAL/API |
| Qwen3.6-27B | 未発表 | 未発表 | 262K→1M(YaRN) | LOCAL/API |

### CODING（主要ベンチ）

| Model | SWE-bench Verified | SWE-bench Pro | Terminal-Bench 2.0 |
|---|---:|---:|---:|
| Opus4.6 | — | — | — |
| Sonnet4.6 | 79.6 | ~60* | 59.1 |
| Opus4.5 | — | — | — |
| Sonnet4.5 | — | — | — |
| Kimi K2.6 | 80.2 | 58.6 | 66.7 |
| Kimi K2.5 | 76.8 | — | — |
| Qwen3.6 Plus | 78.8 | — | 61.6 |
| MiniMax M2.7 | 未公開 | 56.2 | 57.0 |
| MiniMax M2.5 | 80.2 | — | — |
| GLM-5.1 | 77.8 | 58.4 | — |
| GLM-5 | 77.8 | — | — |
| Step 3.5 Flash | 74.4 | — | 51.0 |
| Qwen3.6-35B-A3B | 73.4 | — | 51.5 |
| Qwen3.6-27B | 77.2 | 53.5 | 59.3 |
