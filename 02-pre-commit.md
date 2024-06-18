# pre-commit

[pre-commit document](https://pre-commit.com/)

## Installation

安装 pre-commit
```
pip install pre-commit
```

查看 pre-commit 版本
```
pre-commit --version
```

## Usage

1. 在项目下添加 pre-commit-config.yaml
```yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
-   repo: https://github.com/psf/black
    rev: 22.10.0
    hooks:
    -   id: black
```

2. install git hook scripts
```
pre-commit install
```

3. run against all the files
```
pre-commit run --all-files
```

4. 自动更新 repo 的版本
自动更新 `.pre-commit-config.yaml` 中使用到的 `repo`
```
pre-commit autoupdate
```

## .pre-commit-config.yaml

```yaml
# global include pattern
files: ''
# global exclude pattern
exclude: '^$'
# 如果设置为true，在出现的一个检查错误后停止执行剩下的检查
fail_fast: false
# 一组 repo 的列表
repos:
    # 要 clone 的仓库 url
-   repo: https://github.com/pre-commit/pre-commit-hooks
    # 要 clone 的 reversion 或者 tag
    rev: v2.3.0
    # hook 列表
    hooks:
        # hook id
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
-   repo: https://github.com/psf/black
    rev: 22.10.0
    hooks:
    -   id: black
```
