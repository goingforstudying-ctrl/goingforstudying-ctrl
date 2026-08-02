# My code ships in VS Code, TensorFlow, and Apache Airflow

Software engineer across the stack — **AI engineering, full-stack product, and the infrastructure underneath**. When a tool I use breaks, I root-cause it and upstream the fix: **31 merged PRs** in some of the most-used open-source projects in the world. Race conditions, memory leaks, gradient math, UI edge cases — every claim below is one click from the diff.

📫 goingforstudying@gmail.com

---

### 🤖 AI engineering

| Project | PR | What it fixes |
|---|---|---|
| tensorflow/tensorflow | [#119869](https://github.com/tensorflow/tensorflow/pull/119869) | Wrong `xlogy` / `xlog1py` gradient w.r.t. `x` at `x = 0` |
| apache/superset | [#40746](https://github.com/apache/superset/pull/40746) | **MCP** tools crashing on `Role` ORM objects — Pydantic validation fix |
| Significant-Gravitas/AutoGPT | [#12540](https://github.com/Significant-Gravitas/AutoGPT/pull/12540) | `IndexError` guard for empty `choices` in LLM provider responses |
| langgenius/dify | [#36903](https://github.com/langgenius/dify/pull/36903) | `idle-in-transaction` from long-lived DB sessions in tool icon lookups |
| ogx-ai/ogx | [#6072](https://github.com/ogx-ai/ogx/pull/6072) | `RuntimeError: Event loop is closed` on first VertexAI inference after startup |

### 🧰 Full-stack & product

| Project | PR | What it fixes |
|---|---|---|
| microsoft/vscode | [#318935](https://github.com/microsoft/vscode/pull/318935) | Toolbar layout breakage in CJK locales |
| denoland/deno | [#34410](https://github.com/denoland/deno/pull/34410) | LSP — remove a panic path in `PerformanceScopeMark` drop |
| usememos/memos | [#6000](https://github.com/usememos/memos/pull/6000) | Link previews silently dropped standard `<meta name=description>` |
| Y2Z/monolith | [#492](https://github.com/Y2Z/monolith/pull/492) | Send all matching cookies, not just the last one |

### ⚙️ Distributed systems & infra

| Project | PR | What it fixes |
|---|---|---|
| apache/airflow | [#68741](https://github.com/apache/airflow/pull/68741) | Scheduler race — stale executor `SUCCESS` overwriting a re-queued deferred task |
| celery/celery | [#10342](https://github.com/celery/celery/pull/10342), [#10366](https://github.com/celery/celery/pull/10366) | Redis `ResultConsumer` memory leak — root-caused twice: original fix, then the regression after a revert |
| PrefectHQ/prefect | [#22417](https://github.com/PrefectHQ/prefect/pull/22417) | ECS runs stuck `PENDING` when the capacity provider can't place a task |
| aio-libs/aiohttp | [#12787](https://github.com/aio-libs/aiohttp/pull/12787) | Race in `TCPConnector.close()` — in-flight DNS resolutions now fail cleanly instead of hanging |
| apache/datafusion-ballista | [#2119](https://github.com/apache/datafusion-ballista/pull/2119) | Retryable IO errors misclassified — transient storage errors killed whole jobs |
| astronomer/astronomer-cosmos | [#2737](https://github.com/astronomer/astronomer-cosmos/pull/2737) | Warn when users pass output-only template fields that get silently discarded |
| kubevela/kubevela | [#7162](https://github.com/kubevela/kubevela/pull/7162) | Stable, identifiable `User-Agent` for Helm repo index fetches |

---


*Full list: [all merged PRs →](https://github.com/search?q=author%3Agoingforstudying-ctrl+is%3Apr+is%3Amerged&type=pullrequests&s=created&o=desc)*
