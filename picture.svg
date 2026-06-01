mindmap
  root((Infra / SRE / AI Platform<br>技能树门禁系统))
    核心理念
      目标能力
        用软件工程、系统思维、可观测性、英文沟通解决真实问题
        不是工具收藏 / AI演示 / 路线图cosplay
      中心主干
        英文证据 + 编程能力 + Go/后端理解 + Linux/网络直觉 + 调试纪律
        所有上层能力依赖此主干；英文和证据是硬前置
      英文+证据（硬前置）🔒
        技术英文阅读与源码笔记
        英文README、API文档、事故复盘
        用英文讲清项目、故障、权衡与限制
        GitHub issue notes / repro notes / PR notes
        文档/测试/bugfix PR作为信任资产
        硬门禁要求
          关键产出必须有英文版
          可运行仓库链接
          测试/运行日志
          缺一不过
        通用英文门禁
          README：what/how to run/API usage/limitations
          API文档：endpoint/request/response/error cases/examples
          项目讲解：problem/design/implementation/trade-off/result
          事故讲解：symptom/impact/mitigation/hypothesis/evidence/root cause/fix/prevention
          证据：repo link/commit history/test result/run log/screenshot/trace
          模拟面试：coding/project deep dive/troubleshooting/basic system design
          所有关键产出未附英文版或可验证证据，则节点门禁不通过
      底线警示（门禁前勿声称）
        只会kubectl apply一次 ≠ K8s
        只会建仪表盘 ≠ SRE
        只调LLM API或跟教程部署vLLM ≠ AI基础设施
        说不出用户/API/故障模式/权衡 ≠ 平台工程
        无法解释benchmark design和controlled variables ≠ 性能优化
        没有英文README/复盘/运行日志 ≠ 英文就绪
        如果经不起追问，就不该写在简历上
    基础技能层（第一阶段）
      编程基础🔒
        Python脚本/CLI/文件/JSON/HTTP
        数据结构与基本算法
        Git/GitHub/commit/PR/pytest/README
        测试/日志/错误处理/配置
        解释每行核心代码
        门禁
          200+行CLI工具
          含单元测试
          英文README
          运行日志
          可维护目录结构
      Go云原生基础🔒
        Go语法/结构体/接口/错误处理
        goroutine/channel/context/timeout/cancellation
        Go HTTP服务（路由/中间件/配置/日志）
        /healthz /readyz /metrics pprof trace
        Go test/benchmark/race detector/Dockerfile
        门禁
          Go HTTP服务暴露Prometheus指标
          通过测试、Docker部署
          压测记录
          英文README
      后端工程🔒
        REST API设计/错误码/认证/权限
        Go service first，再补FastAPI/Python backend
        PostgreSQL（schema/index/transaction）
        Redis/queue/worker/retry/idempotency
        Testing/logging/config/CI
        Dockerize and deploy
        门禁
          真实API项目含DB/测试/部署
          英文OpenAPI文档
          Postman/Newman测试
          核心模块单元测试覆盖率≥70%
      Linux+网络🔒
        进程/线程/FD/内存/磁盘/IO
        systemd/journald/permissions
        TCP/IP/DNS/HTTP/TLS
        连接池/超时/重试/NAT
        排查工具：curl/ss/lsof/dig/tcpdump/strace/dmesg
        延迟/丢包/重传/吞吐
        inode耗尽/FD limit/CPU飙高/内存泄漏
        eBPF基础
          bpftrace
          BCC
          perf events
          uprobes/kprobes
        门禁
          网络失败定位
          CPU/内存/FD/inode故障排查
          至少2个eBPF场景实操
          附脚本/命令输出/英文RCA证据链
    云原生与SRE层（第二阶段）
      容器+Kubernetes🔒
        Dockerfile/镜像层/容器日志
        Pod/Deployment/Service/Ingress
        ConfigMap/Secret/PVC/Namespace
        RBAC/requests/limits/QoS class/eviction
        liveness/readiness/rolling update/Job/CronJob/HPA
        常见故障
          Pending
          CrashLoopBackOff
          ImagePullBackOff
          DNS
          Service/Ingress不可达
        Node压力
          NotReady
          DiskPressure
          MemoryPressure
          PIDPressure
          pod eviction
        Go controller开发
          watch Node condition
          cordon + drain
          status/event
        门禁
          解释Pod Pending所有原因
          实现Go controller自动处理Node NotReady
          提交代码、演示日志
          400+英文排查文档
      可观测性+SRE🔒
        Metrics：Prometheus/Grafana/histogram/P99
        Logs：结构化日志/correlation ID/Loki
        Traces：OpenTelemetry/span/sampling/Jaeger
        SLO/SLI/burn-rate alert
        负载测试/故障注入/回滚
        变更门禁
          canary或blue-green
          自动回滚
          发布后验证
        5分钟止血：回滚/扩容/降级/限流
        告警降噪/降低琐事/安全自动化
        端到端关联：metric alert → log query → trace span
        调试深度方法论
          影响范围与时间线
          假设与证据链
          快速止血与事后根因分析分离
          benchmark design，controlled workload
          tail latency，queueing，saturation，regression guard
        门禁
          部署Prometheus+Grafana+Loki+Jaeger全栈
          至少1条指标-日志-trace关联告警
          3个英文深度故事（事故/设计/性能）
          每个包含止血-排查-复盘完整操作日志
          提交英文runbook、复盘日志
          可复现实验证据
      云+IaC+CI/CD🔒
        选一朵云：AWS或GCP
        基础组件：VPC/IAM/VM/LB/storage/container registry
        托管K8s基础
        Terraform：resource/module/state/backend/plan/state show
        CI/CD：test/build image/deploy/Git revert/rollback
        变更审批/canary/blue-green/自动回滚触发器
        回滚风险
          DB schema
          DNS/routing
          依赖服务
          跨集群/跨地域状态碎片
        细粒度恢复
          Terraform state追溯
          资源依赖图
          module版本回退
        secrets/least privilege/audit/cost awareness
        门禁
          完成一次blue-green或canary发布
          验证自动回滚
          提交英文变更记录
          Git revert + Terraform state级回滚演练
          不一致风险清单
    简历与证据层（第三阶段）
      简历证据体系🔒
        2-3个深度项目，不要浅层demo
        英文README/运行指南/测试/限制说明
        incident notes/benchmark notes/design notes
        源码阅读与issue复现
        可选：docs/tests/bugfix PR
        门禁
          每条简历主张都能打开仓库
          运行命令
          看到日志或复盘证据
    AI Infra专项层（第四阶段）
      专项纵深选择
        主干稳固后选择一个或多个方向
        通用方向
          专项SRE：故障复盘/容量规划/混沌工程
          专项可观测：OpenTelemetry/eBPF/应用性能剖析
        AI Infra方向
          AI Serving
          AI Training/Cluster
        门禁
          任意细分方向产出1个深度项目
          1篇英文设计/复盘
          可重复实验记录
      专项AI Serving🔒
        基础：ML基础/token/batch/checkpoint
        框架：vLLM/SGLang/Triton/KServe/Ray Serve
        性能调优：batching/KV cache
        核心指标：TTFT/TPOT/P99/tokens/sec/error rate
        延迟分解：queue/prefill/decode/network/downstream
        发布策略：canary rollout/blue-green/quality gate/automatic rollback
        GPU观测
          DCGM Exporter
          OOM/memory
          eBPF host bottleneck
        全局GPU视角：gpu_utilization_ratio（按集群/任务/服务聚合）
        门禁
          推理服务深度项目
          受控基准/延迟分解
          DCGM单卡指标
          gpu_utilization_ratio聚合看板
          回滚证据
          英文复盘
      专项AI Training/Cluster🔒
        基础：ML基础/training/checkpoint
        通信：NCCL/RDMA/InfiniBand/RoCE/multi-node training
        调度框架：KubeRay/Kueue/Volcano/Slurm/quota/multi-tenancy
        容错：checkpoint/fault recovery/straggler/collective bottleneck
        GPU Operator/拓扑感知调度/容量与成本约束
        集群GPU视角：job/tenant级gpu_utilization_ratio与排队效率
        门禁
          训练/集群深度项目
          故障恢复/调度证据
          GPU全局利用率看板
          英文复盘
      核心AI系统（长期）🔒
        C++/CUDA/Triton kernel
        NCCL/RDMA/InfiniBand/RoCE/EFA
        硬件指标：HBM/Tensor Core/SM occupancy/MFU/NVLink/PCIe拓扑/NUMA
        并行策略：Data/Tensor/Pipeline/Expert Parallelism
        框架：PyTorch/Megatron/DeepSpeed/JAX runtime/Slurm/HPC
        内部实现：vLLM/SGLang runtime internals/GPU Operator
        Profiling：Nsight profiling/eBPF/perf for host bottlenecks
        系统级源码阅读或严肃开源贡献
        门禁
          用profiling证明一个真实瓶颈
          提交英文报告
          包含MFU/HBM/kernel或collective证据
