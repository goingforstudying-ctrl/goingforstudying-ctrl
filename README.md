# Hi, I'm goingforstudying-ctrl

Backend engineer focused on **data infrastructure & workflow-orchestration reliability**. I debug the tools you already run in production — Airflow, Celery, Prefect, aiohttp — and upstream the fixes.

**31 merged PRs** across Airflow, Celery, TensorFlow, VS Code, aiohttp, Superset, Prefect, Deno, and more. Mostly race conditions, memory leaks, and failure-path correctness. Every claim below is one click from the diff.

📫 goingforstudying@gmail.com

---

## Selected merged PRs

### Distributed systems & orchestration

| Project | PR | What it fixes |
|---|---|---|
| apache/airflow | [#68741](https://github.com/apache/airflow/pull/68741) | Scheduler race — stale executor `SUCCESS` overwriting a re-queued deferred task |
| celery/celery | [#10342](https://github.com/celery/celery/pull/10342), [#10366](https://github.com/celery/celery/pull/10366) | Redis `ResultConsumer` memory leak — root-caused twice: original fix, then the regression after a revert |
| PrefectHQ/prefect | [#22417](https://github.com/PrefectHQ/prefect/pull/22417) | ECS runs stuck `PENDING` when the capacity provider can't place a task |
| apache/datafusion-ballista | [#2119](https://github.com/apache/datafusion-ballista/pull/2119) | Retryable IO errors misclassified when wrapped in `DataFusionError::Shared` — transient storage errors killed whole jobs |
| astronomer/astronomer-cosmos | [#2737](https://github.com/astronomer/astronomer-cosmos/pull/2737) | Warn when users pass output-only template fields that get silently discarded |
| kubevela/kubevela | [#7162](https://github.com/kubevela/kubevela/pull/7162) | Stable, identifiable `User-Agent` for Helm repo index fetches |

### Async Python & networking

| Project | PR | What it fixes |
|---|---|---|
| aio-libs/aiohttp | [#12787](https://github.com/aio-libs/aiohttp/pull/12787) | Race in `TCPConnector.close()` — in-flight DNS resolutions now fail cleanly instead of hanging |
| langgenius/dify | [#36903](https://github.com/langgenius/dify/pull/36903) | `idle-in-transaction` from long-lived DB sessions in tool icon lookups |
| apache/superset | [#40746](https://github.com/apache/superset/pull/40746) | MCP tools crashing on `Role` ORM objects — Pydantic validation fix |
| Significant-Gravitas/AutoGPT | [#12540](https://github.com/Significant-Gravitas/AutoGPT/pull/12540) | `IndexError` guard for empty `choices` in LLM provider responses |

### Runtimes & tooling

| Project | PR | What it fixes |
|---|---|---|
| tensorflow/tensorflow | [#119869](https://github.com/tensorflow/tensorflow/pull/119869) | Wrong `xlogy` / `xlog1py` gradient w.r.t. `x` at `x = 0` |
| microsoft/vscode | [#318935](https://github.com/microsoft/vscode/pull/318935) | Toolbar layout breakage in CJK locales |
| denoland/deno | [#34410](https://github.com/denoland/deno/pull/34410) | LSP — remove a panic path in `PerformanceScopeMark` drop |
| usememos/memos | [#6000](https://github.com/usememos/memos/pull/6000) | Link previews silently dropped standard `<meta name=description>` |
| Y2Z/monolith | [#492](https://github.com/Y2Z/monolith/pull/492) | Send all matching cookies, not just the last one |

---

*Full list: [all merged PRs](https://github.com/search?q=author%3Agoingforstudying-ctrl+is%3Apr+is%3Amerged&type=pullrequests&s=created&o=desc)*
