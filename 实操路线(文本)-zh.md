# 落实版技能树 v2.1：高上限、低泡沫、强证据

## 0. 总定位

### 0.1 当前真实起点

- 不是低能起点，但属于**工程零基础起点**。
- 综合实力、表达、反思、AI 协作敏感度、投入意愿均为优势，但**不能直接兑换成工程能力**，只能帮助更快建立能力。
- **当前不包装为**：AI Infra、SRE、云原生、平台工程、分布式系统工程师。
- **真实定位**：初级后端 / 运维开发 / DevOps / 测试开发方向候选人。
- **长期方向**：Backend Infrastructure / Observability / Reliability Engineering。
- **原则**：允许低级切入，但所有低级任务必须**高质量完成**。

### 0.2 核心目标

两年内从“非科班、无工程经历、AI 项目泡沫风险高的学生”训练为：

> 能用 Python / Go 写真实小工具和后端服务，能部署、测试、排障、写英文文档、形成证据链，并能通过初级工程岗位追问的候选人。

最终不是靠标签赢，而是靠**证据赢**。

### 0.3 不小瞧综合实力，但不放松工程门禁

- 优势只作为学习加速器，不作为简历能力项。
- **可写入简历的只有**：可运行项目、可解释代码、测试结果、英文 README、API 文档、排障日志、RCA 复盘、commit history、benchmark/load test 记录、真实 PR/issue/review 记录。

### 0.4 总原则

1. 证据优先，不靠自我叙事。
2. 先低级闭环，再高级系统。
3. 先单机服务，再容器，再 K8s，再云。
4. 先普通排障，再可观测性，再 SRE 方法论。
5. 先后端工程，再平台工程。
6. AI 可以用，但不能替你理解。
7. 所有关键项目必须英文可讲。
8. 任何经不起追问的词，不写进简历。

---

## 1. 全局硬前置：英文 + 证据 + AI 使用纪律

### 1.1 英文能力

#### 能力要求

- 阅读英文官方文档
- 写英文 README、issue note、API 文档、bug reproduction note、incident RCA
- 用英文讲清项目背景、设计、限制、权衡

#### 每日最低训练

- 30 分钟英文技术阅读
- 10 个技术词汇或表达积累
- 1 段英文复述当天技术点

#### 每周产出

- 至少一篇英文 learning note（如：Python 文件处理、Go error handling、HTTP 状态码、Docker 镜像层、PG 事务、Redis 重试、DNS 排障、K8s CrashLoopBackOff 等）

### 1.2 证据规范

**所有项目必须包含**：repo link、commit history、README、how to run、test result、run log、known limitations、troubleshooting notes

**后端/API 项目额外包含**：API usage、request/response examples、error cases、config example、database migration notes

**排障项目额外包含**：symptom、impact、timeline、hypothesis、evidence、root cause、mitigation、prevention

### 1.3 AI 使用纪律

AI 是教练、审查员、对照组，**不是代写者**。

**允许**：解释概念、review 代码、生成测试思路、找 bug 假设、生成英文初稿后修改、模拟面试追问

**禁止**：一键生成完整项目提交、不理解就合并、AI 套壳 demo 写成工程、prompt 调参包装成 AI Infra、教程部署包装成生产经验、“AI 协作很强”当核心能力

**每个核心项目必须能通过口头追问**：代码为什么这么写？失败会怎样？有无测试？异常输入/超时怎么处理？日志在哪？如何复现 bug？如何证明它运行过？

---

## 2. 阶段 0：降压与执行系统重建（第 0-4 周）

**目标**：停止路线图焦虑，把每天变成可执行的工程训练。不追求高级技术，只追求稳定启动。真零基础放宽至 3-4 周。

**核心任务**：
- Git/GitHub 基础工作流
- 每日学习日志 + 英文笔记习惯
- 搭建 Python 环境，熟悉终端
- 完成第一个极小 CLI
- 建立“每天小闭环”节奏

**门禁要求**：
- 本地 Git 仓库，至少 10 次有意义的 commit
- Python CLI：读取文本文件，统计行数、词数、错误行数量
- 英文 README（what / how to run / example / limitations）
- 至少 3 个 pytest 测试
- 一篇 200 词英文学习记录
- 能口头解释：变量、函数、循环、条件、文件读取、异常处理

**禁止事项**：不改职业终局、不新增技能树、不看高级 JD 吓自己、不碰 K8s / AI Infra / eBPF / Rust / C++

---

## 3. 阶段 1：编程基本功、Python 工具层与轻量 CS 基础（第 1-3 个月）

**目标**：独立写小工具、能测试、能记录、能解释代码。

### 核心技能

**Python 基础**：变量/函数/模块、list/dict/set/tuple、文件读写、JSON/CSV、异常处理、argparse/typer、requests、pathlib、logging、pytest、venv

**Git/GitHub**：commit、branch、PR、issue、README、.gitignore、commit 规范

**基础算法与数据结构**（初级够用）：字符串处理、数组/哈希表、栈/队列、排序、简单递归、时间复杂度基本判断（不沉迷刷题）

**轻量计算机基础层**（必须提前穿插）：
- 进程 vs 线程、阻塞 vs 非阻塞
- 文件/目录/权限/路径、标准 IO
- 环境变量、端口、socket、localhost
- HTTP 请求/响应结构、状态码 2xx/3xx/4xx/5xx
- DNS 作用、TCP 三次握手直觉解释
- 建议阅读：《计算机网络：自顶向下》前 4 章
- Linux 基础命令 30 个：pwd, ls, cd, mkdir, rm, cp, mv, touch, cat, less, grep, find, chmod, chown, ps, kill, top, df, du, free, curl, ping, dig, ss, lsof, tar, env, export, journalctl, systemctl

### 阶段项目 A：日志分析 CLI

- 功能：读 Nginx 风格日志，统计总请求数、错误数/率、Top N endpoint，按状态码过滤，输出 JSON/Markdown 报告
- 工程：300 行左右，pytest 核心逻辑，英文 README + 示例日志 + 示例输出 + run log + limitations

### 阶段项目 B：HTTP 健康检查 CLI

- 功能：读 URL 列表，并发/顺序检查 HTTP 状态，记录响应时间，超时设置，重试
- 工程：清晰错误处理、logging、pytest、英文 README + troubleshooting note

### Go 热身周（阶段 1 末尾）

- 完成 Go Tour 基础部分
- 写 3 个小函数 + table-driven tests
- 写一个读取 JSON 并输出摘要的程序
- 写一个最小 HTTP handler 返回 JSON
- 英文短笔记：Python error handling vs Go error handling

### 阶段门禁

- 独立写 300-500 行 Python CLI，能解释核心代码
- 能写 pytest，看懂基本报错并修复
- 用 Git 管理项目，至少 2 个英文 README，20 篇英文笔记
- 能解释轻量 CS 基础核心概念
- 完成 Go 热身周任务

---

## 4. 阶段 2：Go 与 HTTP 服务基础（第 4-7 个月）

**目标**：进入后端服务，建立 Go、HTTP、测试、容器化基本能力。这是第一道大坎，预留 4 个月。

### 核心技能

**Go 基础**：package/module、struct、interface、error handling、context、goroutine/channel 基础、defer、table-driven tests、go test、gofmt/go vet

**HTTP 服务**：routing、middleware、JSON 编解码、状态码、config、结构化日志、health check、graceful shutdown

**容器基础**：Dockerfile、docker build/run、环境变量、容器日志、docker compose 基础

### 阶段项目 C：Go Uptime Monitor API

- 功能：REST API 管理 URL targets，定时检查，记录状态和响应时间，提供查询接口，/healthz 和 /readyz，暴露基础 metrics
- 工程：Go HTTP 服务，单元测试，Dockerfile + docker compose，英文 README + API examples + error cases + run log

**暂不要求**：K8s、Prometheus 深度、pprof、trace、高级并发、controller

### 阶段门禁

- 从零写 Go HTTP 服务，解释 handler/middleware/context/错误处理
- 用 Docker 跑起来，写基础测试和英文 API 文档
- 讲清一个请求从进入到响应的流程

---

## 5. 阶段 3：后端工程闭环（第 8-10 个月）

**目标**：能写有状态、有测试、有部署、有失败处理的后端项目。

### 核心技能

**PostgreSQL**：schema 设计、主键/外键、索引基础、事务、migration、连接池基础、EXPLAIN 初步

**Redis**：cache 基础、queue/worker 基础、retry、timeout、idempotency 初步、死信队列概念

**后端工程**：REST API 设计、validation、错误模型、配置管理、日志、单测/集成测试、GitHub Actions 基础 CI

### 阶段项目 D：Incident Tracker / Task API

- 功能：incident/task CRUD，PG 存储，Redis worker 处理异步任务（通知、状态检查、报告），基础鉴权，migration，集成测试，docker compose 一键启动
- 工程：OpenAPI 或清晰 API 文档，README + test result + run log + limitations + schema notes + failure cases

### 阶段门禁

- 完成包含 DB、Redis、测试、Docker Compose 的后端项目
- 核心模块测试覆盖率 60%-70%
- 能解释事务、索引、连接池、重试、幂等
- 能讲清请求落库 → 触发 worker → 失败处理全流程
- 能用英文讲 5 分钟项目

---

## 6. 阶段 4：Linux、网络与普通排障能力（第 11-13 个月）

**目标**：建立排障直觉，先用普通工具解决普通问题，不碰 eBPF。

### 核心技能

**Linux 基础**：进程、文件描述符、权限、信号、环境变量、systemd/journald、磁盘/inode、内存/CPU 观察

**网络基础**：HTTP、DNS、TCP 握手/挥手、端口/socket、超时、重试、TLS 基础

**排障工具**：curl、dig、ss、lsof、ps、top/htop、free、df/du、journalctl、docker logs、tcpdump 基础、strace 入门

### 故障实验室 A：单机与 Docker 故障

基于阶段 3 项目制造并排查：端口占用、配置错误、DB 连接失败、Redis 不可用、DNS 失败、HTTP 超时、FD 耗尽、磁盘满、慢查询、worker 卡住、CPU 飙高、内存增长

### 输出要求

至少 6 篇英文 RCA，包含：symptom、impact、timeline、hypothesis、commands used、evidence、root cause、fix、prevention

### 阶段门禁

- 按证据链定位问题，不依赖猜测
- 解释 curl/dig/ss/lsof 输出含义
- 定位服务启动/访问/DB/Redis 连接类问题
- 能写英文 RCA

**明确后移**：eBPF、BCC、perf 深入、kernel tracing

---

## 7. 阶段 5：容器与 Kubernetes 实用层（第 14-17 个月）

**目标**：会用 K8s 承载和排查自己的服务，不写 controller。

### 核心技能

**容器深化**：镜像层、多阶段构建、容器日志、容器网络基础、资源限制基础

**K8s 基础资源**：Pod、Deployment、Service、Ingress、ConfigMap、Secret、Namespace、requests/limits、探针、Job/CronJob、rollout/rollback

**K8s 排障**：Pending、CrashLoopBackOff、ImagePullBackOff、readiness 失败、Service/Ingress 不可达、DNS 问题、OOMKilled、CPU throttling 基础

### 阶段项目 E：部署到本地 K8s

- 用 kind/minikube，部署 Go API + PG/Redis（实验方式），ConfigMap/Secret，探针，Service/Ingress，能 rollout/rollback

### 故障实验室 B：Kubernetes 故障

至少 8 个 K8s 故障实验，每个附复现步骤、命令输出、英文 RCA、修复记录，并说明与单机/Docker 场景的异同

### 阶段门禁

- 解释 Pod 创建到 Running 流程、Service 暴露机制、探针区别
- 排查 CrashLoopBackOff / ImagePullBackOff / Pending
- 能用英文讲一个 K8s 排障故事

**明确后移**：自定义 controller、operator、自动 cordon/drain、service mesh、CNI 深入

---

## 8. 阶段 6：可观测性与 SRE 入门层（第 18-20 个月）

**目标**：能从指标、日志、trace 关联定位问题。若阶段 4/5 故障实验室扎实，可压缩至 3 个月。

### 核心技能

**Metrics**：Prometheus、Grafana、counter/gauge/histogram、P95/P99、错误率、饱和度、基础告警

**Logs**：结构化日志、correlation ID、日志级别、Loki 基础

**Traces**：OpenTelemetry 基础、span、trace id、Jaeger 基础

**SRE 基础**：SLI、SLO、error budget、告警疲劳、runbook、故障响应、回滚、负载测试、故障注入入门

### 阶段项目 F：可观测性实验室

- 给 Go 项目添加 Prometheus metrics、Grafana dashboard、结构化日志 + correlation ID、OTel trace，至少 1 个告警规则 + runbook
- 故障实验：错误率升高、P99 延迟、DB 慢查询、worker 积压、Redis 不可用、API 超时

### 输出要求

至少 3 篇英文深度故事：事故复盘 RCA、性能优化报告、可观测性设计说明

每篇包含：problem、design/hypothesis、evidence、commands/dashboard/logs/traces、mitigation、final fix、trade-offs、limitations

### 阶段门禁

- 从指标告警定位到日志和 trace
- 解释 P99 重要性、histogram bucket 意义
- 写 runbook，做基础 load test
- 讲清一次从发现到修复的完整事故故事

---

## 9. 阶段 7：云、IaC、CI/CD 与求职证据层（第 21-24/27 个月）

**目标**：将能力压缩为可展示、可面试、可投递的证据资产。24 个月为高强度目标线，25-27 个月为更稳妥现实线。

### 云平台选择

AWS 或 GCP 择一深入。掌握：IAM、VPC、VM、LB、容器镜像仓库、托管数据库概念、托管 K8s 概念、成本意识。预算有限可本地为主，云上最小验证。

### IaC

Terraform 基础：provider、resource、variable、output、state、plan、apply、destroy、module 入门（不追求企业级）

### CI/CD

GitHub Actions：测试、构建镜像、推送、部署、回滚、Git revert、release notes

### 发布实验

完成至少一种：blue-green、canary、rolling update with rollback

附：发布前检查、过程记录、失败回滚实验、英文 change record、风险清单

### 求职证据整理

**核心项目 1**：Python 工具项目（证明脚本、测试、英文文档、CLI）

**核心项目 2**：Go 后端项目（证明 API、DB、Redis、测试、Docker、CI）

**核心项目 3**：可观测性 + 排障实验室（证明 Linux、K8s、metrics、logs、traces、RCA）

### 简历定位

**建议标题**：Junior Backend / DevOps-oriented Engineering Student，Backend & Reliability Engineering Intern Candidate

**中文定位**：初级后端 / 运维开发 / DevOps 方向候选人，长期关注可观测性与可靠性工程

**暂不写**：AI Infra、SRE、Platform、K8s Engineer（除非已被项目证明）

### 阶段门禁

- 3 个可运行项目，英文 README 齐全
- 至少 1 个有完整 API 文档，1 个有 Docker/Compose，1 个部署到 K8s
- 至少 6 篇英文 RCA，3 篇英文深度技术故事
- GitHub 提交记录连续可信
- 能完成 30-45 分钟项目英文讲解，接受代码、排障、系统设计追问

---

## 10. 高阶扩展层：只在主线门禁通过后进入

### 10.1 Kubernetes Controller / Operator

**进入条件**：熟练部署排障，能解释核心资源，已完成 8 个 K8s 故障 RCA。

**学习内容**：reconcile loop、informer、workqueue、幂等、限流、finalizer、CRD。建议写一个简单 controller，不碰自动 drain Node。

### 10.2 eBPF / 深层 Linux 可观测性

**进入条件**：已能用普通工具定位常见问题，完成 CPU/内存/FD/网络故障 RCA，理解系统调用、进程、socket。

**学习内容**：bpftrace、BCC、uprobes/kprobes、perf events。建议用 bpftrace 观察系统调用延迟。

### 10.3 分布式系统与数据库深度

**进入条件**：已完成后端项目，踩过重试/超时/幂等/事务的坑。

**学习内容**：一致性模型、超时/重试/退避、幂等、发件箱模式、saga 概念、分布式锁陷阱、Raft 概念、PG 锁/复制/备份/PITR。

### 10.4 安全工程

**进入条件**：已有后端和 K8s 基础。

**学习内容**：OAuth2/OIDC、JWT 风险、TLS/mTLS、K8s RBAC、NetworkPolicy、secret 管理、镜像扫描、最小权限。

### 10.5 AI Infra

**进入条件**：已完成 Go 后端、K8s 部署排障、可观测性实验室，能解释 GPU/模型服务/延迟/吞吐概念。

**学习内容**：模型服务基础、批处理、排队、GPU 利用率、vLLM/Triton 实验、推理延迟/吞吐 benchmark、成本/容量权衡。

**注意**：只调 LLM API 或部署一次 vLLM 不等于 AI Infra，必须能解释服务、性能、调度、容量和故障模式。

### 10.6 Rust / C++

**进入条件**：Python + Go 主线稳定，至少 2 个核心项目完成，Linux/网络基础不混乱。

**选择建议**：云原生/后端/SRE 方向可长期加 Rust；系统/GPU/高性能计算方向 C++ 更相关。两年内求职不依赖它们。

---

## 11. 每日 / 每周执行模板

### 每日最低闭环

**常规**：2-4 小时代码/项目 + 1 小时英文技术读写 + 1 小时基础知识 + 30 分钟复盘

**时间现实**：每周 15-20 小时有效投入约需 25-27 个月；每天 8 小时有效可提高证据密度，非堆砌新技术

**状态差时保底**：30 行自己理解的代码、1 次 commit、1 段英文笔记、1 个问题记录（不因一天低效重写人生计划）

### 每周最低产出

- 5 次以上 commit
- 1 个可验证小功能
- 1 篇英文 learning note
- 1 次 bug 复盘
- 1 次项目 README 更新

### 每月最低产出

- 一个可展示小版本
- 一次项目自测记录
- 一次英文项目讲解录音或文字稿
- 一次模拟面试复盘

---

## 12. 简历写入规则

只有满足以下条件才能写进简历：

| 技术词 | 最低证据门槛 |
|--------|----------------|
| Python | 至少一个带测试和 README 的 Python 项目 |
| Go | 至少一个带测试和 Docker 的 Go HTTP 服务 |
| PostgreSQL | 项目真实使用，能解释 schema、索引、事务 |
| Redis | 项目真实使用，能解释重试、超时、幂等至少一个 |
| Docker | 能自己写 Dockerfile 并解释构建和运行参数 |
| Kubernetes | 至少部署过自己的项目，排查过 5+ K8s 故障 |
| Prometheus/Grafana | 不只建 dashboard，能解释指标含义和一次告警定位过程 |
| SRE | 至少有英文 RCA、runbook、SLO/SLI 基础实践 |
| AI Infra | 必须有模型服务、性能、容量、故障模式相关证据 |

**禁止包装为高级能力**：AI 生成前端 demo、调用 LLM API、教程式部署、看过文档但无项目、能跑通但讲不清、无测试/无英文 README 的项目

---

## 13. 最终验收标准

两年后必须能回答以下 15 个问题：

1. 你最完整的后端项目是什么？
2. 如何运行？
3. 数据库 schema 怎么设计？
4. 为什么需要 Redis？
5. 失败重试怎么做？
6. 如何测试？
7. 如何部署？
8. 如何观察服务健康？
9. 出现 5xx 怎么排查？
10. P99 延迟升高怎么定位？
11. DB 慢查询怎么看？
12. K8s Pod CrashLoopBackOff 怎么排查？
13. 你写过哪些英文 RCA？
14. 项目最大的限制是什么？
15. 如果重做，你会改什么？

如果这些都能讲清，你就不是泡沫。

---

## 14. 这版技能树的核心修正

**v2.1 相对旧版的主要修正：**

1. 承认综合潜力，但不替代工程证据
2. 后移 eBPF、controller、AI Infra、Rust/C++
3. 早期目标改为 Python / Go / Linux / 后端闭环
4. K8s 从开发扩展转为部署和排障优先
5. SRE 从全家桶转为证据定位故障
6. 外企目标转化为英文文档、RCA、项目讲解
7. 所有阶段绑定可验证产出
8. 用门禁防止 AI 代写、路线图 cosplay、部署泡沫

**v2.1 新增修正：**

- Stage 0 放宽至 0-4 周
- Stage 1 加入轻量 CS 基础层 + Go 热身周
- Stage 2 拉长至 4 个月
- 故障实验室拆为 A/B，分阶段进行
- Stage 6 压缩前提为前序排障证据扎实
- 总周期标注为 24-27 个月区间

> 先用低级任务练出高级纪律，再用高级纪律进入高阶方向。
