# credit-assistant 实训环境

大语言模型部署及应用实训（课程代码 20261173）第 1 周的环境仓库，用于沉淀可复现的开发环境与部署记录。

## 环境要求

| 组件 | 版本 / 位置 |
|---|---|
| 操作系统 | Windows 11 |
| Docker Desktop | 29.6.1（数据目录 `D:\docker\DockerDesktop`） |
| Git | 2.56.1（`D:\Git`） |
| Miniconda | `D:\miniconda3` |
| Python | 3.10.22（conda 环境 `credit-assistant`） |

## 快速开始

```bat
conda env create -f environment.yml
conda activate credit-assistant
python --version
```

验证环境可复现：先 `conda env create -f environment.yml`，能成功创建同名环境即视为通过。

## 目录说明

| 路径 | 说明 |
|---|---|
| `environment.yml` | conda 环境导出文件（`--no-builds`），用于重建环境 |
| `README.md` | 环境说明与使用约定 |

## 第 1 周完成事项

- Docker Desktop 安装、数据目录迁移、镜像加速与 `hello-world` 验证
- MySQL 8.0.45 容器（`mysql-db`，主机端口 9999 → 容器 3306）
- Conda 环境 `credit-assistant` 创建与 `environment.yml` 导出
- Git 仓库初始化、`week1-lab` 分支与提交记录

## 数据安全约束

- 不提交密钥、口令、真实征信数据与大体积模型权重
- 示例口令仅用于隔离的实训环境，真实项目不得使用弱口令
- 对外提供服务统一走网关鉴权，不直接暴露模型端口
