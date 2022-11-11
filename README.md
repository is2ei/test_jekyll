test_jekyll
===

Jekyll + GitHub Pages の動作検証用リポジトリ

## Prerequisites

- [Ruby](https://www.ruby-lang.org/en/)
- [Bundler](https://bundler.io/)

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

起動後は http://127.0.0.1:4000/ でアクセスできる


## Release

#### 1) PRを作成する 

- [develop -> main](https://github.com/is2ei/test_jekyll/compare/main...develop)

#### 2) レビューを依頼し、approveをもらう

#### 3) マージする


## `github-pages`Gemの更新

ローカル環境では`github-pages`Gemを利用している。実際にGitHubで使用されるバージョンは[Dependency versions](https://pages.github.com/versions/)に記載されているので、時々確認して古くなったらGemfileを修正すること。


## 依存Gemのバージョン一覧の確認

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
