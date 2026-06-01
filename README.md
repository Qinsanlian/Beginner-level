[_Infra_SRE_AI Platform 技能成长进度清单（修复版）.md](https://github.com/user-attachments/files/28465034/_Infra_SRE_AI.Platform.md)
# Infra/SRE/AI Platform 技能成长进度清单（修复版）

> 说明：这是**可折叠的全量进度清单**，完美解决信息密集问题：
> 
> 1. 所有原始规则、门禁、知识点 100% 完整保留，没有任何信息损失
> 
> 2. 默认只显示顶层标题，点击即可展开查看对应模块的所有细节
> 
> 3. 你可以勾选 `[x]` 来跟踪自己的学习进度，逐个突破
> 
> 

---

📌 核心理念（前置总纲）

这是整个体系的底层逻辑，所有能力的基础。

### 1\.1 目标能力

* [ ] 理解：我们的目标是用软件工程、系统思维、可观测性、英文沟通解决真实问题

* [ ] 理解：拒绝工具收藏、AI 演示、路线图 cosplay，所有能力要落地解决问题

### 1\.2 中心主干

* [ ] 掌握核心主干能力：英文证据能力、编程能力、Go / 后端理解、Linux / 网络直觉、调试纪律

* [ ] 理解：英文和证据是所有上层能力的硬前置，没有这个，学再多工具都是空中楼阁

### 1\.3 英文 \+ 证据（全局硬前置🔒）

#### 能力要求

* [ ] 掌握技术英文阅读，能写源码笔记

* [ ] 能编写英文 README、API 文档、事故复盘

* [ ] 能用英文讲清项目、故障、权衡与限制

* [ ] 能写 GitHub issue notes、复现笔记、PR 笔记

* [ ] 理解：文档、测试、bugfix PR 是你的信任资产

#### 硬门禁要求（缺一不通过）

* [ ] 所有关键产出都有英文版

* [ ] 所有项目都有可运行的仓库链接

* [ ] 所有项目都附带测试 / 运行日志

#### 通用产出规范

* [ ] 项目 README 包含：what、how to run、API usage、limitations

* [ ] API 文档包含：endpoint、request/response、error cases、examples

* [ ] 项目讲解包含：problem、design、implementation、trade\-off、result

* [ ] 事故讲解包含：symptom、impact、mitigation、hypothesis、evidence、root cause、fix、prevention

* [ ] 所有产出都附带可验证证据：repo link、commit history、test result、run log、screenshot、trace

* [ ] 能通过模拟面试：coding、项目深度沟通、故障排查、基础系统设计

### 1\.4 避坑指南

* [ ] 记住：只会 kubectl apply 一次 ≠ 掌握 K8s

* [ ] 记住：只会建仪表盘 ≠ 掌握 SRE

* [ ] 记住：只调 LLM API 或跟教程部署 vLLM ≠ 掌握 AI 基础设施

* [ ] 记住：说不出用户 / API / 故障模式 / 权衡 ≠ 掌握平台工程

* [ ] 记住：无法解释 benchmark design 和 controlled variables ≠ 会性能优化

* [ ] 记住：没有英文 README / 复盘 / 运行日志 ≠ 英文就绪

* [ ] 记住：如果能力经不起追问，就不该写在简历上



🏗️ 第一阶段：基础技能层（打牢地基，约1\-3个月）

这个阶段打牢最底层的基本功，所有上层能力都依赖这个基础。

### 2\.1 编程基础🔒

#### 核心技能

* [ ] 掌握 Python 脚本 / CLI 工具开发：文件处理、JSON 解析、HTTP 请求

* [ ] 掌握数据结构与基本算法，能解决日常算法问题

* [ ] 掌握 Git/GitHub 工作流：commit 规范、PR 流程、pytest 单元测试、README 编写

* [ ] 掌握工程化基础：测试覆盖、日志记录、错误处理、配置管理

* [ ] 能解释自己写的每一行核心代码，不是只会复制粘贴

#### 门禁要求（全部完成才算通过）

* [ ] 完成一个 200 行以上的 CLI 工具项目

* [ ] 项目包含完整的单元测试，覆盖核心逻辑

* [ ] 配套英文 README，符合通用产出规范

* [ ] 附运行日志，证明项目可正常运行

* [ ] 项目有清晰的可维护目录结构

### 2\.2 Go 云原生基础🔒

#### 核心技能

* [ ] 掌握 Go 基础语法：结构体、接口、错误处理

* [ ] 掌握并发基础：goroutine、channel、context、超时、取消机制

* [ ] 掌握 Go HTTP 服务：路由、中间件、配置、日志

* [ ] 掌握健康检查与可观测基础：/healthz、/readyz、metrics、pprof、trace

* [ ] 掌握测试与容器化：Go test、benchmark、race 检测器、Dockerfile 编写

#### 门禁要求

* [ ] 实现一个 Go HTTP 服务，能暴露 Prometheus 指标

* [ ] 所有测试通过，能通过 Docker 正常部署

* [ ] 附压测记录，证明服务的性能表现

* [ ] 配套英文 README，符合通用产出规范

### 2\.3 后端工程🔒

#### 核心技能

* [ ] 掌握 REST API 设计：错误码、认证、权限控制

* [ ] 掌握技术栈优先级：优先用 Go 写服务，再补充 FastAPI/Python 后端能力

* [ ] 掌握数据存储：PostgreSQL（schema、索引、事务）

* [ ] 掌握数据存储：Redis（队列、worker、重试、幂等性）

* [ ] 掌握工程化：测试、日志、配置、CI 流程

* [ ] 掌握容器化部署：把服务打包成 Docker 镜像，能正常部署

#### 门禁要求

* [ ] 完成一个真实的 API 项目，包含 DB、测试、部署流程

* [ ] 配套英文 OpenAPI 文档，清晰描述接口

* [ ] 用 Postman/Newman 完成接口测试，证明接口可用

* [ ] 核心模块的单元测试覆盖率≥70%

### 2\.4 Linux \+ 网络🔒

#### 核心技能

* [ ] 掌握系统基础：进程、线程、文件描述符、内存、磁盘、IO

* [ ] 掌握系统管理：systemd、journald、权限管理

* [ ] 掌握网络基础：TCP/IP、DNS、HTTP、TLS

* [ ] 掌握网络优化：连接池、超时、重试、NAT

* [ ] 掌握排查工具：curl、ss、lsof、dig、tcpdump、strace、dmesg

* [ ] 掌握常见故障：延迟、丢包、重传、吞吐、inode 耗尽、FD limit、CPU 飙高、内存泄漏

* [ ] 掌握 eBPF 基础：bpftrace、BCC、perf events、uprobes/kprobes

#### 门禁要求

* [ ] 能独立定位网络失败问题，找到根因

* [ ] 能独立排查 CPU / 内存 / FD/inode 相关的故障

* [ ] 至少完成 2 个 eBPF 场景的实操

* [ ] 附对应的脚本、命令输出、英文 RCA 证据链，证明你真的排查过这些问题



☸️ 第二阶段：云原生与SRE层（核心能力，约3\-6个月）

基础打牢之后，进入云原生和 SRE 的核心能力阶段，这是你做 Infra 工程师的核心竞争力。

### 3\.1 容器 \+ Kubernetes🔒

#### 核心技能

* [ ] 掌握容器基础：Dockerfile、镜像层、容器日志

* [ ] 掌握 K8s 核心资源：Pod、Deployment、Service、Ingress

* [ ] 掌握配置与存储：ConfigMap、Secret、PVC、Namespace

* [ ] 掌握资源管理：RBAC、requests/limits、QoS class、驱逐策略

* [ ] 掌握可用性：liveness/readiness 探针、滚动更新、Job、CronJob、HPA

* [ ] 掌握 Pod 故障排查：Pending、CrashLoopBackOff、ImagePullBackOff、DNS 问题、Service/Ingress 不可达

* [ ] 掌握 Node 故障排查：NotReady、DiskPressure、MemoryPressure、PIDPressure、Pod 驱逐

* [ ] 掌握扩展开发：用 Go 写简单的 controller，自定义 K8s 的能力

#### 门禁要求

* [ ] 能完整解释 Pod 处于 Pending 状态的所有可能原因

* [ ] 用 Go 实现一个简单的 controller，能自动处理 Node NotReady 的情况（cordon\+drain）

* [ ] 提交完整的项目代码，附演示运行日志

* [ ] 配套 400 词以上的英文排查文档，记录故障排查的过程

### 3\.2 可观测性 \+ SRE🔒

#### 核心技能

* [ ] 掌握 Metrics：Prometheus、Grafana、histogram、P99 指标

* [ ] 掌握 Logs：结构化日志、correlation ID、Loki

* [ ] 掌握 Traces：OpenTelemetry、span、采样、Jaeger

* [ ] 掌握 SRE 核心实践：SLO/SLI、burn\-rate 告警

* [ ] 掌握稳定性保障：负载测试、故障注入、回滚机制

* [ ] 掌握发布保障：canary 发布、blue\-green 发布、自动回滚、发布后验证

* [ ] 掌握应急能力：5 分钟止血 —— 回滚、扩容、降级、限流

* [ ] 掌握效率优化：告警降噪、减少琐事、安全自动化

* [ ] 掌握端到端排查：metric 告警 → 日志查询 → trace 链路，能把三者关联起来

* [ ] 掌握调试方法论：理清影响范围与时间线、用假设与证据链排查、快速止血和根因分离、受控 benchmark、尾延迟与饱和点

#### 门禁要求

* [ ] 独立部署 Prometheus\+Grafana\+Loki\+Jaeger 全栈可观测性平台

* [ ] 实现至少 1 条指标 \- 日志 \- trace 关联的告警，能从告警直接定位到具体的问题

* [ ] 输出 3 个英文深度故事：事故复盘、设计文档、性能优化报告

* [ ] 每个故事都包含：止血 \- 排查 \- 复盘的完整操作日志

* [ ] 提交英文 runbook、复盘日志，还有可复现的实验证据

### 3\.3 云 \+ IaC\+CI/CD🔒

#### 核心技能

* [ ] 选择一朵云深入：AWS 或者 GCP

* [ ] 掌握云基础组件：VPC、IAM、VM、LB、存储、容器镜像仓库

* [ ] 掌握托管 K8s：云厂商托管 K8s 服务的使用

* [ ] 掌握 IaC：Terraform，resource、module、state、backend、plan、state show

* [ ] 掌握 CI/CD：测试、构建镜像、部署、Git revert、回滚机制

* [ ] 掌握发布管理：变更审批、canary/blue\-green 发布、自动回滚触发器

* [ ] 掌握回滚风险管控：DB schema 风险、DNS/routing 风险、依赖服务风险、跨集群状态碎片

* [ ] 掌握细粒度恢复：Terraform state 追溯、资源依赖图、module 版本回退

* [ ] 掌握安全与成本：secrets 管理、最小权限、审计、成本意识

#### 门禁要求

* [ ] 完成一次完整的 blue\-green 或 canary 发布

* [ ] 验证自动回滚机制能正常工作，出问题能自动回滚

* [ ] 提交英文的变更记录，记录整个发布过程

* [ ] 完成 Git revert \+ Terraform state 级的回滚演练

* [ ] 输出一份不一致风险清单，梳理你这个系统里所有可能的回滚风险



📄 第三阶段：简历与证据层（能力沉淀，约1\-2个月）

前面的能力都练完了，现在要把这些能力沉淀成能证明你自己的项目，放到简历上。

### 4\.1 简历证据体系🔒

#### 核心要求

* [ ] 选 2\-3 个深度项目，不做一堆浅层 demo

* [ ] 每个项目都有：英文 README、运行指南、测试、限制说明

* [ ] 每个项目都有：incident notes、benchmark notes、design notes

* [ ] 可选：做开源贡献：源码阅读、issue 复现、docs/tests/bugfix PR

#### 门禁要求

* [ ] 简历上的每一条主张，都能打开对应的 GitHub 仓库

* [ ] 别人能按照你的 README，运行你的项目

* [ ] 别人能看到你的运行日志、复盘证据，证明你真的做过这些事



🤖 第四阶段：AI Infra专项层（纵深突破，长期成长）

主干稳固后，选一个方向深入，成为这个领域的专家。

### 5\.1 专项选择

#### 可选方向

* [ ] 通用 SRE 方向：专项 SRE（故障复盘、容量规划、混沌工程）

* [ ] 通用 SRE 方向：专项可观测（OpenTelemetry、eBPF、应用性能剖析）

* [ ] AI Infra 方向：AI Serving

* [ ] AI Infra 方向：AI Training/Cluster

#### 通用门禁要求

* [ ] 产出 1 个深度项目

* [ ] 1 篇英文设计 / 复盘文档

* [ ] 可重复的实验记录

### 5\.2 专项：AI Serving🔒

#### 核心技能

* [ ] 掌握基础：ML 基础、token、batch、checkpoint

* [ ] 掌握框架：vLLM、SGLang、Triton、KServe、Ray Serve

* [ ] 掌握性能调优：batching、KV cache 优化

* [ ] 掌握核心指标：TTFT、TPOT、P99、tokens/sec、错误率

* [ ] 掌握延迟分解：queue、prefill、decode、network、downstream

* [ ] 掌握发布策略：canary rollout、blue\-green、quality gate、自动回滚

* [ ] 掌握 GPU 观测：DCGM Exporter、OOM 排查、eBPF 主机瓶颈排查

* [ ] 掌握全局视角：集群 / 任务 / 服务级的 gpu\_utilization\_ratio 聚合

#### 门禁要求

* [ ] 完成一个推理服务的深度项目

* [ ] 做受控的基准测试，完成延迟分解，找到性能瓶颈

* [ ] 监控 DCGM 单卡指标，能看到每个 GPU 的状态

* [ ] 搭建 gpu\_utilization\_ratio 的聚合看板，看整个集群的 GPU 使用情况

* [ ] 有完整的回滚证据，证明发布出问题能正常回滚

* [ ] 配套英文的复盘文档，记录整个过程

### 5\.3 专项：AI Training/Cluster🔒

#### 核心技能

* [ ] 掌握基础：ML 基础、training、checkpoint

* [ ] 掌握通信：NCCL、RDMA、InfiniBand、RoCE、多节点训练

* [ ] 掌握调度框架：KubeRay、Kueue、Volcano、Slurm、配额、多租户

* [ ] 掌握容错：checkpoint、故障恢复、straggler 问题、集体通信瓶颈

* [ ] 掌握 GPU 管理：GPU Operator、拓扑感知调度、容量与成本约束

* [ ] 掌握集群视角：job/tenant 级的 gpu\_utilization\_ratio、排队效率优化

#### 门禁要求

* [ ] 完成一个训练 / 集群的深度项目

* [ ] 有故障恢复、调度的证据，证明你解决了这些问题

* [ ] 搭建 GPU 全局利用率的看板，能看到整个集群的 GPU 使用情况

* [ ] 配套英文的复盘文档，记录整个过程

### 5\.4 核心 AI 系统（长期深入）🔒

#### 核心技能

* [ ] 掌握底层开发：C\+\+/CUDA、Triton kernel 开发

* [ ] 掌握高速通信：NCCL、RDMA、InfiniBand、RoCE、EFA

* [ ] 掌握硬件指标：HBM、Tensor Core、SM occupancy、MFU、NVLink、PCIe 拓扑、NUMA

* [ ] 掌握并行策略：数据并行、张量并行、流水线并行、专家并行

* [ ] 掌握框架：PyTorch、Megatron、DeepSpeed、JAX runtime、Slurm、HPC

* [ ] 掌握源码深入：vLLM、SGLang runtime 内部实现、GPU Operator 内部实现

* [ ] 掌握性能剖析：Nsight profiling、eBPF、perf，排查主机的瓶颈

* [ ] 掌握开源贡献：系统级的源码阅读，或者严肃的开源贡献

#### 门禁要求

* [ ] 用 profiling 工具，证明你找到了一个真实的系统瓶颈

* [ ] 提交英文的报告，记录整个排查和优化的过程

* [ ] 报告里要包含 MFU、HBM、kernel 或者集体通信的证据，证明你真的找到了瓶颈



> （注：文档部分内容可能由 AI 生成）
> 
> 

> （注：文档部分内容可能由 AI 生成）
