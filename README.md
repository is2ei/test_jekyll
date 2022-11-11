test_jekyll
===

Jekyll + GitHub Pages の動作検証用リポジトリ

## Prerequisites

- [Ruby](https://www.ruby-lang.org/en/)
- [Bundler](https://bundler.io/)
- (Optional) VS Codeを使っている場合
  - [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

*Rubyの3系を使うとwebrickが読み込めないエラーが出る。依存関係を更新する回避策もあるが、現状はJekyllデフォルトのGemfileは更新せず2系で動かすことを想定している。[参考](https://github.com/jekyll/jekyll/issues/8523)*

## Getting started

#### 1) 依存ライブラリのインストール

```
bundle install
```

#### 2) 開発サーバーを起動

```
bundle exec jekyll serve
```

起動後は http://127.0.0.1:4000/test_jekyll/ でアクセスできる


## Release

#### 1) PRを作成する 

- [develop -> main](https://github.com/is2ei/test_jekyll/compare/main...develop)

#### 2) レビューを依頼し、approveをもらう

#### 3) マージする

## Create new page

#### 1) markdownファイルを作成する

ファイル名の例：`hello.markdown`

ファイル内容の例：

```
---
layout: page
title: Hello
permalink: /hello/
---

## Where does it come from?

Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.

The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.
```

*`layout`は基本的に`page`を使用すること*

#### 2) ヘッダー内のリンク一覧を更新する

`_config.yml`を開き、`header_pages`を更新する

例：

```
header_pages:
  - index.markdown
  - hello.markdown
```

## Update dependencies

ローカル環境では`github-pages`Gemを利用している。実際にGitHubで使用されるバージョンは[Dependency versions](https://pages.github.com/versions/)に記載されているので、時々確認して古くなったらGemfileを修正すること。


## List dependencies

```
bundle exec github-pages versions
```

## References

- [Dependency versions](https://pages.github.com/versions/)
- [Jekyll](https://jekyllrb.com/)
- [About GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)
- [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
- [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
- [Adding a theme to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll)
