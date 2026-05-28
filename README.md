flowchart TD
    classDef core fill:#ff4444,stroke:#cc0000,color:white,stroke-width:2px
    classDef advanced fill:#ff9933,stroke:#cc6600,color:white,stroke-width:2px
    classDef senior fill:#f5f5f5,stroke:#999999,color:#333,stroke-width:2px
    classDef year1 fill:#e3f2fd,stroke:#2196f3,stroke-width:2px
    classDef year2 fill:#e8f5e9,stroke:#4caf50,stroke-width:2px
    classDef year3 fill:#fff3e0,stroke:#ff9800,stroke-width:2px
    classDef year4 fill:#fce4ec,stroke:#e91e63,stroke-width:2px
    classDef year5 fill:#f3e5f5,stroke:#9c27b0,stroke-width:2px
    classDef principle fill:#fff9c4,stroke:#fbc02d,stroke-width:2px
    classDef rule fill:#ffebee,stroke:#c62828,stroke-width:2px
    classDef english fill:#e0f7fa,stroke:#00acc1,stroke-width:2px
    classDef route3 fill:#e8eaf6,stroke:#3f51b5,stroke-width:2px

    %% 根节点
    A[五年技能树总览] --> B[设计原则]
    A --> C[时间权重分配]
    A --> D[路线1：云原生/AI Infra]
    A --> E[路线3：技术产品/方案架构]
    A --> F[第一年每日行动基准]
    A --> G[使用铁律]
    A --> H[第0年今日唯一行动]

    %% 设计原则
    B --> B1[英语贯穿所有阶段，权重≥20%]
    B --> B2[路线3分两阶段：第2年启蒙(只练习不求职)，第4年实战(用于面试)]
    B --> B3[依赖关系严格遵守：Docker→K8s→CI/CD→可观测性]
    B --> B4[第1年禁止看路线3，第2年只做写笔记、画图、模拟演讲]
    class B,B1,B2,B3,B4 principle

    %% 时间权重分配
    C --> C1[第1年：技术50% / 英语30% / 其他20%]
    C --> C2[第2年：技术60% / 英语20% / 路线3启蒙10% / 其他10%]
    C --> C3[第3年：技术50% / 英语15% / 路线3启蒙5%+实战15% / 其他15%]
    C --> C4[第4年：技术40% / 英语10% / 路线3实战40% / 其他10%]
    C --> C5[第5年：技术30% / 英语10% / 路线3实战50% / 其他10%]
    class C1 year1
    class C2 year2
    class C3 year3
    class C4 year4
    class C5 year5

    %% 路线1子节点
    D --> D1[操作系统与Linux]
    D --> D2[编程语言]
    D --> D3[容器化]
    D --> D4[Kubernetes]
    D --> D5[云平台]
    D --> D6[CI/CD]
    D --> D7[可观测性]
    D --> D8[性能与优化]
    D --> D9[安全与合规]
    D --> D10[证书]
    D --> D11[英语(贯穿所有阶段)]

    %% D1 分支
    D1 --> D101[常用命令：ls,cd,cp,mv,grep,awk,sed,tar]
    D1 --> D102[进程管理：ps,systemctl,journalctl]
    D1 --> D103[网络工具：netstat,ss,curl,iptables基础]
    D1 --> D104[Shell脚本：变量、循环、条件、函数]
    D1 --> D105[文件系统、/proc、内核参数调优]
    D104 --> D105
    class D101,D102,D103 core,year1
    class D104 advanced,year2
    class D105 senior,year4

    %% D2 分支
    D2 --> D201[Python手写：变量、循环、函数、类、文件读写、requests]
    D2 --> D202[Git：add,commit,push,log,branch]
    D2 --> D203[Go基础：goroutine,channel,包管理]
    D201 --> D203
    class D201,D202 core,year1
    class D203 advanced,year2

    %% D3 分支
    D3 --> D301[Docker：镜像、容器、run/ps/exec/logs/build]
    D3 --> D302[Docker Compose：多容器编排]
    D3 --> D303[容器网络、卷、环境变量]
    D3 --> D304[containerd/CRI-O]
    D301 --> D302
    D301 --> D303
    class D301,D302 core,year1
    class D303 advanced,year2
    class D304 senior,year4

    %% D4 分支
    D4 --> D401[kubectl：get,describe,logs,exec,apply,delete]
    D4 --> D402[核心资源：Pod,Deployment,Service,Ingress,ConfigMap,Secret]
    D4 --> D403[调度：nodeSelector,affinity,taints]
    D4 --> D404[存储：PV/PVC,StorageClass]
    D4 --> D405[Helm：模板化部署]
    D4 --> D406[网络策略：NetworkPolicy]
    D301 --> D401
    D401 --> D402
    D402 --> D403
    D402 --> D404
    D402 --> D405
    class D401,D402 core,year1
    class D403,D404 advanced,year2
    class D405 advanced,year3
    class D406 senior,year4

    %% D5 分支
    D5 --> D501[AWS：EC2,VPC,IAM,S3,EKS基础]
    D5 --> D502[阿里云：ECS,VPC,RAM,OSS,ACK基础]
    D5 --> D503[Terraform：基础设施即代码]
    D402 --> D501
    D402 --> D502
    D501 --> D503
    D502 --> D503
    class D501,D502,D503 advanced,year3

    %% D6 分支
    D6 --> D601[GitLab CI/GitHub Actions：编写流水线文件]
    D6 --> D602[ArgoCD：GitOps]
    D202 --> D601
    D301 --> D601
    D402 --> D601
    D601 --> D602
    class D601 advanced,year2
    class D602 senior,year4

    %% D7 分支
    D7 --> D701[Prometheus+Grafana：指标采集、仪表盘、告警]
    D7 --> D702[Loki：日志]
    D7 --> D703[Jaeger：追踪]
    D402 --> D701
    D701 --> D702
    class D701 advanced,year3
    class D702,D703 senior,year4

    %% D8 分支
    D8 --> D801[压测工具：wrk,ab,vegeta]
    D8 --> D802[HPA：水平自动伸缩]
    D8 --> D803[成本优化：资源请求/限制、FinOps概念]
    D402 --> D802
    class D801,D802 advanced,year3
    class D803 senior,year4

    %% D9 分支
    D9 --> D901[镜像扫描：Trivy基础]
    D9 --> D902[基础合规概念：GDPR数据流图]
    D301 --> D901
    class D901,D902 senior,year4

    %% D10 分支
    D10 --> D1001[CKA]
    D10 --> D1002[CKAD]
    D10 --> D1003[CKS]
    D10 --> D1004[AWS SAA]
    D402 --> D1001
    D1001 --> D1002
    D1001 --> D1003
    class D1001 advanced,year2
    class D1002,D1004 advanced,year3
    class D1003 senior,year4

    %% D11 英语分支
    D11 --> D1101[词汇：四级→六级→雅思 | 每天20分钟]
    D11 --> D1102[阅读官方文档：Docker,K8s,AWS | 每天20分钟]
    D11 --> D1103[写英文技术笔记：中英文对照 | 每周1篇]
    D11 --> D1104[听力/口语：跟读技术演讲、模拟面试 | 每天15分钟]
    class D1101,D1102 year1
    class D1103 year2
    class D1104 year3

    %% 路线3前置条件
    E --> E0[前置条件：完成路线1所有核心+30%进阶；能独立部署完整应用到K8s]
    class E0 rule

    %% 路线3子节点
    E --> E1[硬技术基础]
    E --> E2[业务与成本]
    E --> E3[产品与需求]
    E --> E4[合规与风险管理]
    E --> E5[软沟通]
    E --> E6[证书]

    %% E1
    E1 --> E101[画架构图：draw.io,Lucidchart]
    E1 --> E102[API设计：REST,gRPC]
    class E101 route3,year2
    class E102 route3,year4

    %% E2
    E2 --> E201[技术选型对比报告：3个方案+优劣势 | 练习]
    E2 --> E202[TCO模型：服务器、存储、网络、人力成本]
    E2 --> E203[ROI分析：投入vs业务收益]
    class E201 route3,year2
    class E202,E203 route3,year4
    E202 --> E203

    %% E3
    E3 --> E301[需求访谈与痛点挖掘 | 模拟]
    E3 --> E302[产品路线图规划：季度/年]
    class E301 route3,year3
    class E302 route3,year4
    E201 --> E302

    %% E4
    E4 --> E401[数据流图与合规影响评估：GDPR/PIPL]
    class E401 route3,year4
    D9 --> E401

    %% E5
    E5 --> E501[英文技术演讲：10页PPT,15分钟 | 模拟]
    E5 --> E502[售前POC设计]
    E5 --> E503[跨部门沟通：非技术语言解释决策]
    class E501 route3,year2
    class E502,E503 route3,year4
    D1104 --> E501

    %% E6
    E6 --> E601[AWS SAA | 加分]
    E6 --> E602[雅思6.5/托福95 | 外企硬门槛]
    E6 --> E603[PMP/Scrum Master | 管理加分]
    class E601,E602,E603 route3

    %% 第一年每日行动基准
    F --> F1[Linux：每天3条命令 + 每周1个脚本(如备份日志)]
    F --> F2[Python：手写1个函数(不依赖AI)，累计20+]
    F --> F3[Docker：第6个月能用docker-compose跑WordPress+MySQL]
    F --> F4[K8s：第9个月能用minikube跑nginx，熟练kubectl]
    F --> F5[英语：每天20个单词 + 读1段官方文档(Docker/K8s)]
    F --> F6[GitHub：实时更新所有代码和笔记]
    class F1,F2,F3,F4,F5,F6 year1

    %% 使用铁律
    G --> G1[第1年只看路线1核心，不看进阶，不看路线3]
    G --> G2[第2年可以开始路线3启蒙(画图、写笔记、模拟演讲)，但不得用于求职]
    G --> G3[第4年达到CKA+1年工作经验后，才将路线3技能写入简历]
    G --> G4[英语每天不可中断，否则所有技术学习效率减半]
    G --> G5[每年底对照技能树自查：未完成核心，不得进入下一年]
    class G1,G2,G3,G4,G5 rule

    %% 第0年行动
    H --> H1[安装Ubuntu，敲ls命令]
    H --> H2[在GitHub创建仓库：learning-2026]
    class H1,H2 year1
