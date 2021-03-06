# Python Package Template

📦 一个快速上传到 PyPI 的 Python Package 模版。

## 使用方法

1. 点击本项目右上角的绿色按钮 `Use this template`（使用此模板），输入名称和说明，完成创建；

2. 将项目克隆到本地，这里以本项目为例，实际操作时这里需要替换你自己的项目；

    ```bash
    git clone https://github.com/Ailln/python-package-template.git --depth 1
    ```

3. 修改配置，文件中有提示；

    ```bash
    cd python-package-template

    # 1. 将下文中的 your_package_name 改成你的实际项目名称
    mv package_name your_package_name

    # 2. 接下来修改 `setup.py /package_name/shell/usage.py`中的参数，里面有提示。

    # 3. 最后 `README.md` 修改为你的项目介绍，也就是你当前在读的这个文本。
    ```

4. 编写你的 Package 代码；

5. 上传到 PyPi（需要注册），参考[如何发布自己的包到 pypi](https://www.v2ai.cn/2018/07/30/python/1-pypi/)；

    ```bash
    bash scripts/upload_pypi.sh
    ```

6. 更新到 Github。

    ```bash
    git push
    ```

## 项目结构

```bash
.
├── package_name # 需要手动修改为你的项目名称
│   ├── __init__.py
│   ├── shell # 在命令行中执行的代码
│   │   ├── __init__.py
│   │   └── usage.py
│   ├── src # 静态资源
│   │   └── temp.txt
│   └── version.py # 版本号
├── scripts
│   ├── local_install.sh # 本地测试安装
│   └── upload_pypi.sh # 上传到 PyPi 的工具
├── setup.py # 安装配置
├── requirements.txt # 包依赖
├── requirements_dev.txt # 开发依赖
├── README.md # 项目文档
├── LICENSE # 本项目的 License，需要手动替换它
└── .gitignore
```

## 许可

[![](https://award.dovolopor.com?lt=License&rt=MIT&rbc=green)](./LICENSE)

## TODO

- [ ] 增加自动修改 `package name` 的脚本。
- [ ] 增加 test 相关代码。

## 参考

- [如何从模板创建仓库？](https://help.github.com/cn/articles/creating-a-repository-from-a-template)
- [如何发布自己的包到 pypi ？](https://www.v2ai.cn/2018/07/30/python/1-pypi/)
