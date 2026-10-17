# loty — 鉴定机构抽签系统发布库

> 本仓库为编译产物发布库，**仅存 .so + 启动文件 + 前端资源**，不接受直接修改。
>
> 源码仓库：[SaintVamp/lottery](https://github.com/SaintVamp/lottery)
> 编译流水线：`SaintVamp/lottery` → `SaintVamp/CITools` → 本仓库
> 镜像仓库：`saintvamp/lottery`

## 目录结构

```
loty/
├── app/              # 编译后的业务代码（.so）
│   ├── routes/
│   └── services/
├── web/              # 前端页面
│   ├── admin/        # 管理后台
│   └── draw/         # 客户端抽签页
├── data/             # 数据库目录（运行时挂载）
├── run.py            # 启动入口
└── requirements.txt  # Python 依赖
```

## 发布说明

- 所有代码修改请在 `SaintVamp/lottery` 开发库提交
- push master 后自动触发 CITools 编译，编译产物会 force push 到本仓库
- 本仓库历史始终只有 1 个 commit
