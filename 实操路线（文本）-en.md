# Implementable Skill Tree v2.1: High Ceiling, Low Hype, Strong Evidence

## 0. Overall Positioning

### 0.1 Real Current Starting Point

- Not a low-ability starting point, but **engineering zero-base**.
- Comprehensive strength, articulation, reflection, AI collaboration sensitivity, and commitment are advantages, but they **cannot be directly converted into engineering ability** – they only help build ability faster.
- **Do not package currently as**: AI Infra, SRE, Cloud Native, Platform Engineering, Distributed Systems Engineer.
- **Realistic positioning**: Junior Backend / Ops-oriented / Test-Dev oriented candidate.
- **Long-term direction**: Backend Infrastructure / Observability / Reliability Engineering.
- **Principle**: Low-level entry is allowed, but all low-level tasks must be **completed with high quality**.

### 0.2 Core Goal

Within two years, train from “non-CS, no engineering experience, high-risk of AI‑project‑bubble student” into a candidate who:

> Can write real small tools and backend services in Python/Go, deploy, test, troubleshoot, write English documentation, form an evidence chain, and survive junior‑level engineering follow‑up questions.

The final goal is not to win by labels, but to **win by evidence**.

### 0.3 Do Not Underestimate Overall Strengths, But Do Not Relax Engineering Gates

- Strengths are only learning accelerators, not resume capability items.
- **Only items that can be written on the resume**: runnable projects, explainable code, test results, English README, API documentation, troubleshooting logs, RCA post‑mortems, commit history, benchmark/load test records, real PR/issue/review records.

### 0.4 General Principles

1. Evidence first, not self‑narrative.
2. First close low‑level loops, then move to advanced systems.
3. First single‑host service, then containers, then K8s, then cloud.
4. First ordinary troubleshooting, then observability, then SRE methodology.
5. First backend engineering, then platform engineering.
6. AI can be used, but it cannot replace understanding.
7. All key projects must be explainable in English.
8. No word that cannot withstand follow‑up questions goes on the resume.

---

## 1. Global Hard Prerequisites: English + Evidence + AI Discipline

### 1.1 English Ability

#### Required Competence

- Read English official documentation
- Write English README, issue notes, API documentation, bug reproduction notes, incident RCA
- Explain project background, design, trade‑offs, limitations in English

#### Daily Minimum Training

- 30 minutes of English technical reading
- 10 technical words/phrases accumulation
- 1 paragraph of English re‑explanation of the day’s technical point

#### Weekly Output

- At least one English learning note (e.g., Python file handling, Go error handling, HTTP status codes, Docker image layers, PG transactions, Redis retries, DNS troubleshooting, K8s CrashLoopBackOff, etc.)

### 1.2 Evidence Standards

**All projects must include**: repo link, commit history, README, how to run, test results, run logs, known limitations, troubleshooting notes

**Backend/API projects additionally include**: API usage, request/response examples, error cases, config example, database migration notes

**Troubleshooting projects additionally include**: symptom, impact, timeline, hypothesis, evidence, root cause, mitigation, prevention

### 1.3 AI Usage Discipline

AI is a coach, reviewer, sparring partner – **not a writer**.

**Allowed**: explain concepts, review code, generate testing ideas, hypothesise bugs, generate English draft then revise, simulate interview follow‑up questions

**Forbidden**: one‑click generation of a full project and submitting it, merging without understanding, packaging AI‑generated demos as engineering, calling prompt tuning “AI Infra”, packaging tutorial deployments as production experience, claiming “strong AI collaboration” as a core ability

**Every core project must survive oral follow‑up questions**: Why is the code written this way? What happens on failure? Are there tests? How are abnormal inputs/timeouts handled? Where are the logs? How to reproduce a bug? How do you prove it ran?

---

## 2. Stage 0: Stress Reduction & Execution System Rebuild (Weeks 0–4)

**Goal**: Stop anxiety about roadmaps, turn every day into executable engineering training. Not pursuing advanced technology, only stable start. Allow 3‑4 weeks for true zero‑base.

**Core Tasks**:
- Git/GitHub basic workflow
- Daily study log + English note habit
- Set up Python environment, get comfortable with terminal
- Complete the first minimal CLI
- Establish a “daily small loop” rhythm

**Gate Requirements**:
- Local Git repo with at least 10 meaningful commits
- Python CLI: read a text file, count lines, words, number of error lines
- English README (what / how to run / example / limitations)
- At least 3 pytest tests
- One 200‑word English learning record
- Able to explain orally: variables, functions, loops, conditionals, file reading, exception handling

**Forbidden**: changing career end‑state, adding new skills to the tree, reading senior JD to scare yourself, touching K8s / AI Infra / eBPF / Rust / C++

---

## 3. Stage 1: Programming Fundamentals, Python Tooling & Lightweight CS Basics (Months 1–3)

**Goal**: Independently write small tools, test, document, explain code.

### Core Skills

**Python basics**: variables/functions/modules, list/dict/set/tuple, file I/O, JSON/CSV, exception handling, argparse/typer, requests, pathlib, logging, pytest, venv

**Git/GitHub**: commit, branch, PR, issue, README, .gitignore, commit conventions

**Basic algorithms & data structures** (enough for junior level): string processing, arrays/hash tables, stack/queue, sorting, simple recursion, basic time complexity judgement (do not get obsessed with LeetCode)

**Lightweight CS basics** (must be interspersed early):
- Process vs thread, blocking vs non‑blocking
- File/directory/permissions/paths, standard I/O
- Environment variables, port, socket, localhost
- HTTP request/response structure, status codes 2xx/3xx/4xx/5xx
- Role of DNS, intuitive explanation of TCP 3‑way handshake
- Suggested reading: Computer Networking: A Top‑Down Approach, first 4 chapters
- 30 basic Linux commands: pwd, ls, cd, mkdir, rm, cp, mv, touch, cat, less, grep, find, chmod, chown, ps, kill, top, df, du, free, curl, ping, dig, ss, lsof, tar, env, export, journalctl, systemctl

### Stage Project A: Log Analysis CLI

- Functions: read Nginx‑style log, count total requests, error count/rate, top N endpoints, filter by status code, output JSON/Markdown report
- Engineering: ~300 lines, pytest for core logic, English README + example log + example output + run log + limitations

### Stage Project B: HTTP Health Check CLI

- Functions: read a list of URLs, concurrent/sequential HTTP checks, record response time, timeout setting, retries
- Engineering: clean error handling, logging, pytest, English README + troubleshooting note

### Go Warm‑up Week (end of Stage 1)

- Complete Go Tour basics
- Write 3 small functions + table‑driven tests
- Write a program that reads JSON and outputs a summary
- Write a minimal HTTP handler that returns JSON
- Short English note: Python error handling vs Go error handling

### Stage Gates

- Independently write a 300‑500 line Python CLI, explain core code
- Write pytest, understand basic failures and fix them
- Manage projects with Git, at least 2 English READMEs, 20 English notes
- Explain core concepts of lightweight CS basics
- Complete Go warm‑up week tasks

---

## 4. Stage 2: Go & HTTP Service Foundations (Months 4–7)

**Goal**: Enter backend services, build basic Go, HTTP, testing, containerisation abilities. This is the first real difficulty spike – reserve 4 months.

### Core Skills

**Go basics**: package/module, struct, interface, error handling, context, basic goroutine/channel, defer, table‑driven tests, go test, gofmt/go vet

**HTTP service**: routing, middleware, JSON encoding/decoding, status codes, config, structured logging, health check, graceful shutdown

**Container basics**: Dockerfile, docker build/run, environment variables, container logs, basic docker compose

### Stage Project C: Go Uptime Monitor API

- Functions: REST API to manage URL targets, periodic checking, record status and response time, provide query endpoint, /healthz and /readyz, expose basic metrics
- Engineering: Go HTTP service, unit tests, Dockerfile + docker compose, English README + API examples + error cases + run log

**Not required yet**: K8s, deep Prometheus, pprof, trace, advanced concurrency, controllers

### Stage Gates

- Write a Go HTTP service from scratch, explain handler/middleware/context/error handling
- Run it with Docker, write basic tests and English API docs
- Explain the request flow from entry to response

---

## 5. Stage 3: Backend Engineering Closed Loop (Months 8–10)

**Goal**: Be able to write a backend project with state, tests, deployment, and failure handling.

### Core Skills

**PostgreSQL**: schema design, primary/foreign keys, basic indexes, transactions, migrations, basic connection pool, preliminary EXPLAIN

**Redis**: cache basics, queue/worker basics, retry, timeout, basic idempotency, dead‑letter queue concept

**Backend engineering**: REST API design, validation, error modelling, configuration management, logging, unit/integration tests, basic GitHub Actions CI

### Stage Project D: Incident Tracker / Task API

- Functions: CRUD for incidents/tasks, store in PG, Redis worker for async tasks (notifications, status checks, reports), basic auth, migrations, integration tests, docker compose up
- Engineering: OpenAPI or clear API docs, README + test results + run log + limitations + schema notes + failure cases

### Stage Gates

- Complete a backend project with DB, Redis, tests, Docker Compose
- Test coverage 60‑70% for core modules
- Explain transactions, indexes, connection pool, retries, idempotency
- Explain the whole flow from request to DB insert to worker trigger to failure handling
- Deliver a 5‑minute English project explanation

---

## 6. Stage 4: Linux, Networking & Ordinary Troubleshooting (Months 11–13)

**Goal**: Build troubleshooting intuition, first solve ordinary problems with ordinary tools, stay away from eBPF.

### Core Skills

**Linux basics**: processes, file descriptors, permissions, signals, environment variables, systemd/journald, disk/inode, memory/CPU observation

**Networking basics**: HTTP, DNS, TCP handshake/teardown, port/socket, timeouts, retries, TLS basics

**Troubleshooting tools**: curl, dig, ss, lsof, ps, top/htop, free, df/du, journalctl, docker logs, basic tcpdump, introductory strace

### Fault Lab A: Single‑host & Docker Faults

Based on the Stage 3 project, create and diagnose: port already in use, config errors, DB connection failures, Redis unavailable, DNS failures, HTTP timeouts, FD exhaustion, disk full, slow queries, worker stuck, high CPU, memory growth

### Output Requirements

At least 6 English RCAs, each containing: symptom, impact, timeline, hypothesis, commands used, evidence, root cause, fix, prevention

### Stage Gates

- Locate issues by evidence chain, not guesswork
- Explain the meaning of curl/dig/ss/lsof outputs
- Locate problems with service start/access/DB/Redis connections
- Write English RCAs

**Explicitly deferred**: eBPF, BCC, in‑depth perf, kernel tracing

---

## 7. Stage 5: Containers & Kubernetes Practical Layer (Months 14–17)

**Goal**: Be able to run and troubleshoot your own services on K8s, without writing controllers.

### Core Skills

**Container deepening**: image layers, multi‑stage builds, container logs, basic container networking, basic resource limits

**Basic K8s resources**: Pod, Deployment, Service, Ingress, ConfigMap, Secret, Namespace, requests/limits, probes, Job/CronJob, rollout/rollback

**K8s troubleshooting**: Pending, CrashLoopBackOff, ImagePullBackOff, readiness failure, Service/Ingress unreachable, DNS issues, OOMKilled, basic CPU throttling

### Stage Project E: Deploy to Local K8s

- Use kind/minikube, deploy Go API + PG/Redis (experimental), ConfigMap/Secret, probes, Service/Ingress, be able to rollout/rollback

### Fault Lab B: Kubernetes Faults

At least 8 K8s fault experiments, each with reproduction steps, command outputs, English RCA, fix record, and explanation of differences from single‑host/Docker scenarios

### Stage Gates

- Explain the Pod creation to Running flow, Service exposure mechanism, differences between probes
- Diagnose CrashLoopBackOff / ImagePullBackOff / Pending
- Deliver an English K8s troubleshooting story

**Explicitly deferred**: custom controllers, operators, automatic cordon/drain, service mesh, deep CNI

---

## 8. Stage 6: Observability & SRE Introduction (Months 18–20)

**Goal**: Correlate metrics, logs, and traces to locate problems. If Stage 4/5 fault labs are solid, can compress to 3 months.

### Core Skills

**Metrics**: Prometheus, Grafana, counter/gauge/histogram, P95/P99, error rate, saturation, basic alerting

**Logs**: structured logging, correlation ID, log levels, basic Loki

**Traces**: OpenTelemetry basics, span, trace id, Jaeger basics

**SRE basics**: SLI, SLO, error budget, alert fatigue, runbook, incident response, rollback, load testing, basic fault injection

### Stage Project F: Observability Lab

- Add Prometheus metrics, Grafana dashboard, structured logs + correlation ID, OTel trace to the Go project, at least 1 alert rule + runbook
- Fault experiments: error rate spike, P99 latency increase, slow DB query, worker backlog, Redis unavailable, API timeout

### Output Requirements

At least 3 in‑depth English stories: incident RCA, performance optimisation report, observability design explanation

Each story includes: problem, design/hypothesis, evidence, commands/dashboard/logs/traces, mitigation, final fix, trade‑offs, limitations

### Stage Gates

- From metric alert locate to logs and trace
- Explain importance of P99, meaning of histogram buckets
- Write a runbook, perform basic load test
- Deliver a complete incident story from discovery to fix

---

## 9. Stage 7: Cloud, IaC, CI/CD & Job‑Ready Evidence (Months 21–24/27)

**Goal**: Compress abilities into demonstrable, interview‑ready, submittable evidence assets. 24 months is the high‑intensity target line, 25‑27 months is the more realistic stable line.

### Cloud Platform Choice

Choose AWS or GCP and go deep. Master: IAM, VPC, VM, LB, container registry, managed database concepts, managed K8s concepts, cost awareness. On‑prem is fine if budget is limited, do minimal cloud validation.

### IaC

Terraform basics: provider, resource, variable, output, state, plan, apply, destroy, module introduction (not enterprise‑level)

### CI/CD

GitHub Actions: test, build image, push, deploy, rollback, git revert, release notes

### Release Experiments

Complete at least one of: blue‑green, canary, rolling update with rollback

Attach: pre‑release checklist, process log, failed rollback experiment, English change record, risk list

### Job‑Evidence Organisation

**Core Project 1**: Python tool project (proves scripting, testing, English docs, CLI)

**Core Project 2**: Go backend project (proves API, DB, Redis, testing, Docker, CI)

**Core Project 3**: Observability + troubleshooting lab (proves Linux, K8s, metrics, logs, traces, RCA)

### Resume Positioning

**Suggested title**: Junior Backend / DevOps‑oriented Engineering Student – Backend & Reliability Engineering Intern Candidate

**Chinese positioning (translated for reference)**: Junior Backend / Ops‑oriented / DevOps direction candidate, long‑term focus on observability and reliability engineering

**Do not write yet**: AI Infra, SRE, Platform, K8s Engineer (unless proven by projects)

### Stage Gates

- 3 runnable projects with complete English READMEs
- At least 1 with full API docs, 1 with Docker/Compose, 1 deployed to K8s
- At least 6 English RCAs, 3 English in‑depth technical stories
- Continuous, credible GitHub commit history
- Deliver a 30‑45 minute English project walkthrough, survive follow‑up questions on code, troubleshooting, and basic system design

---

## 10. Advanced Expansion Layer: Only Enter After Mainline Gates Are Passed

### 10.1 Kubernetes Controller / Operator

**Entry condition**: proficient deployment and troubleshooting, can explain core resources, completed 8 K8s fault RCAs.

**Topics**: reconcile loop, informer, workqueue, idempotency, rate limiting, finalizer, CRD. Write a simple controller, do not touch automatic node draining.

### 10.2 eBPF / Deep Linux Observability

**Entry condition**: already able to locate common issues with ordinary tools, completed CPU/memory/FD/network fault RCAs, understand system calls, processes, sockets.

**Topics**: bpftrace, BCC, uprobes/kprobes, perf events. Suggest using bpftrace to observe syscall latency.

### 10.3 Distributed Systems & Database Depth

**Entry condition**: completed backend projects, have experienced pitfalls with retries/timeouts/idempotency/transactions.

**Topics**: consistency models, timeout/retry/backoff, idempotency, outbox pattern, saga concept, distributed lock traps, Raft concept, PG locks/replication/backup/PITR.

### 10.4 Security Engineering

**Entry condition**: basic backend and K8s foundation.

**Topics**: OAuth2/OIDC, JWT risks, TLS/mTLS, K8s RBAC, NetworkPolicy, secret management, image scanning, least privilege.

### 10.5 AI Infra

**Entry condition**: completed Go backend, K8s deployment & troubleshooting, observability lab; able to explain basic GPU/model serving/latency/throughput concepts.

**Topics**: model serving basics, batching, queueing, GPU utilisation, vLLM/Triton experiments, inference latency/throughput benchmarks, cost/capacity trade‑offs.

**Note**: Just calling an LLM API or deploying vLLM once does **not** equal AI Infra – you must be able to explain serving, performance, scheduling, capacity, and failure modes.

### 10.6 Rust / C++

**Entry condition**: Python + Go mainline stable, at least 2 core projects completed, Linux/networking fundamentals solid.

**Choice advice**: Cloud‑native/backend/SRE paths can add Rust over the long term; systems/GPU/HPC paths C++ is more relevant. Do not rely on them for job seeking within two years.

---

## 11. Daily / Weekly Execution Template

### Daily Minimum Closed Loop

**Normal**: 2‑4 hours coding/project + 1 hour English technical reading/writing + 1 hour basic knowledge + 30 minutes review

**Time reality**: 15‑20 effective hours per week → roughly 25‑27 months; 8 effective hours per day can increase evidence density – not about stacking new technologies

**Low‑energy minimum**: 30 lines of code you understand, 1 commit, 1 English note, 1 issue log (do not rewrite life plan because of one low‑output day)

### Weekly Minimum Output

- 5+ commits
- 1 verifiable small feature
- 1 English learning note
- 1 bug post‑mortem
- 1 project README update

### Monthly Minimum Output

- 1 demonstrable small version
- 1 project self‑test record
- 1 recorded English project walkthrough (audio or script)
- 1 mock interview review

---

## 12. Resume Inclusion Rules

Only write a technical term on your resume when the minimum evidence is met:

| Term | Minimum Evidence Gate |
|------|-----------------------|
| Python | At least one Python project with tests and README |
| Go | At least one Go HTTP service with tests and Docker |
| PostgreSQL | Actually used in a project, can explain schema, indexes, transactions |
| Redis | Actually used in a project, can explain retries, timeouts, or idempotency |
| Docker | Write your own Dockerfile and explain build/runtime parameters |
| Kubernetes | Deployed your own project, diagnosed 5+ K8s faults |
| Prometheus/Grafana | Not just built a dashboard – can explain metric meaning and one alert‑to‑fix process |
| SRE | At least English RCA, runbook, SLO/SLI practical exercise |
| AI Infra | Must have evidence of model serving, performance, capacity, failure modes |

**Forbidden to package as advanced ability**: AI‑generated frontend demos, just calling an LLM API, tutorial‑style deployments, read docs but no project, can run but cannot explain, no tests/no English README projects

---

## 13. Final Acceptance Criteria

After two years, you must be able to answer these 15 questions:

1. What is your most complete backend project?
2. How do you run it?
3. How is the database schema designed?
4. Why do you need Redis?
5. How do you handle retries on failure?
6. How do you test it?
7. How do you deploy it?
8. How do you observe the service’s health?
9. How do you diagnose 5xx errors?
10. How do you locate a P99 latency increase?
11. How do you examine slow database queries?
12. How do you diagnose a K8s Pod CrashLoopBackOff?
13. What English RCAs have you written?
14. What is the biggest limitation of your project?
15. If you did it again, what would you change?

If you can clearly explain all of these, you are not a bubble.

---

## 14. Key Corrections in This Skill Tree

**Main changes from previous versions**:

1. Acknowledge comprehensive potential, but do not replace engineering evidence
2. Defer eBPF, controllers, AI Infra, Rust/C++
3. Early goals focus on Python / Go / Linux / backend closed loop
4. Kubernetes shifted from development‑extended to deployment & troubleshooting first
5. SRE shifted from “whole package” to evidence‑based fault localisation
6. Translate “foreign company target” into English documentation, RCAs, project presentations
7. All stages bound to verifiable outputs
8. Use gates to prevent AI‑generated shortcuts, roadmap cosplay, deployment bubbles

**New corrections in v2.1**:

- Stage 0 relaxed to 0‑4 weeks
- Stage 1 adds lightweight CS basics + Go warm‑up week
- Stage 2 extended to 4 months
- Fault labs split into A/B, staged separately
- Stage 6 compression precondition: solid prior troubleshooting evidence
- Total timeline annotated as 24‑27 months range

> First build advanced discipline through low‑level tasks, then use that discipline to enter advanced directions.
