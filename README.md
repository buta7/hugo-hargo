# README

## セットアップ

サイト作成

```shell
hugo new site hugo-hargo
```

レポジトリ初期化

```shell
cd hugo-hargo
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
```

テーマ設定

```shell
git submodule add git@github.com:themefisher/hargo.git themes/hargo
```

サイト設定

```shell
cd hugo-hargo
cp -pr ./themes/hargo/exampleSite/{config.toml,content,static} .
```

config.toml

```toml
baseURL = "https://higebobo.github.io/hugo-hargo/"
languageCode = "ja"
title = "Hugo Hargo"
theme = "hargo"
publishDir = "docs"
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
cp somplace/{Makefile,deploy.sh} .
git remote add origin git@github.com:higebobo/hugo-hargo.git
make deploy
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:higebobo/hugo-hargo.git higebobo-hargo
cd higebobo-hargo
git submodule update --init --recursive
```

## 使い方

### 投稿

新規投稿

```shell
hugo new blog/post-3.md
content/blog/post-3.md created
```

編集

```shell
vi content/blog/hello.md
```

## Link

* [Hargo Hugo Ecommerce Theme \| Hugo Themes](https://themes.gohugo.io/hargo-hugo-ecommerce-theme/)
