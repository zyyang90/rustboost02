# cargo generate

可以根据 git 仓库生成新 Rust 项目

## 1. 安装

```
cargo install cargo-generate
```

## 2. 使用

使用 github 上的仓库作为模版，生成新项目:
```
cargo generate username-on-git/template_name
```
或者，使用本地的project 也可以创建新的项目
```
cargo generate --path $HOME/my_project
```
可以指定新项目的名称
```
cargo generate --git https://github.com/zyyang90/hello --name abc
```
