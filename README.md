# DI-sheep：深度强化学习 + 羊了个羊

## **2022.9.30之后的开发者请移步新的主库：[opendilab/DI-sheep](https://github.com/opendilab/DI-sheep)**

当人工智能技术的明珠——深度强化学习，遇到号称“通关率只有0.01%”的游戏“羊了个羊”，会碰撞出哪些奇思妙想呢？

# 使用指南

## 快速上手

- 如果想**在线试玩** --> [在线网页（施工中）](https://github.com/PaParaZz1/DI-sheep)
- 如果想**本地部署/测试**
  - 服务端（Python）
    ```shell
    # 预先安装好 Python3
    cd service
    pip install -r requirements.txt
    FLASK_APP=app.py flask run
    ```
  - 客户端（react）
    ```shell
    # 预先安装好 node.js 和 react
    npm run build
    npm run preview
    ```
    然后在网页中打开对应链接即可
- 如果想进行完整的深度强化学习训练
    ```shell
    # 预先安装好 Python3
    cd service
    pip install -r requirements-train.txt
    python3 -u sheep_ppo_main.py
    ```
- 如果想使用定义好的 gym 羊了个羊环境 --> 点个 star 之后直接暴力 CTRL C+V 拿走 `service/sheep_env.py` 尽情魔改
- 如果想了解更多深度强化学习相关知识 --> 欢迎参阅 [DI-engine](https://github.com/opendilab/DI-engine) 和[相关文档](https://di-engine-docs.readthedocs.io/zh_CN/latest/)
- 如果想了解未来的更新计划 --> 请参阅[更新计划](#更新计划)
- 如果有其他问题或想法 --> 欢迎 github ISSUE 区讨论，或是贡献 Pull requests

## 项目结构
```text
.
├── LICENSE
├── ui                       --> react 网页前端
└── service                  --> Python 核心模块（算法和服务端）
    ├── app.py                  --> flask 服务 app
    ├── requirement.txt         --> Python 依赖库列表
    ├── sheep_env.py            --> gym 格式环境
    ├── sheep_model.py          --> 基于 PyTorch 的 Actor-Critic 神经网络模型
    ├── sheep_ppo_main.py       --> 基于 DI-engine 的深度强化学习训练主函数
    ├── test_sheep_env.py       --> gym 格式环境的单元测试
    └── test_sheep_model.py     --> 神经网络模型的单元测试
```

# 更新计划

## 算法

- [ ] 强化学习训练参数调整和算法微调
- [ ] 详细的神经网络和强化学习算法设计文档
- [ ] model-based RL 和 planning 算法
- [ ] 神经网络压缩（用于部署） 

## 环境
- [ ] 添加原类型游戏（比如3tiles）中的各种道具
- [ ] 牌的层数问题如何定义
- [ ] 结合 JAX 优化环境运行速度


## 应用
- [ ] 更多 AI 训练时的行为分析
- [ ] 更多自定义主题和 BGM
- [ ] 在线网页端部署
- [ ] 移动端应用（欢迎Android/IOS开发者支持）


# 致谢
- react 前端部分主要参考 https://github.com/StreakingMan/solvable-sheep-game ，请大家也多多支持这个 repo 


# License
DI-sheep is released under the Apache 2.0 license.
