---
marp: true
header: "Marpを使ったスライドテンプレート"
footer: "@k0j1r0n0 (January 31, 2023)"
headingDivider: 1
paginate: true
---

# AWS re:Invent 2022で気になったサービス

## 1. AWS Lambda SnapStart [![icon](./image/aws_lambda.png)](https://aws.amazon.com/jp/blogs/news/new-accelerate-your-lambda-functions-with-lambda-snapstart/)

- 関数を事前に初期化(init)して実行環境のスナップショットを保存しておき、関数を初回実行する際には、予め保存したスナップショットを復元することで起動時間を短縮する。現在、Java 11のみ対応している。

[![](https://docs.aws.amazon.com/images/lambda/latest/dg/images/Overview-Successful-Invokes.png)](https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html#runtimes-lifecycle)

## 2. Amazon Security Lake [![icon](./image/aws_security_lake.png)](https://aws.amazon.com/jp/security-lake/)
  - クラウド、オンプレミス、カスタムソースからのセキュリティログを集約・管理し、分析や利用のアクセスを提供するデータレイクサービスであり、AWS CloudTrail、AWS Security Hub等のログを収集する。

# 参考

- AWS Lambda SnapStart
  - https://aws.amazon.com/jp/blogs/news/new-accelerate-your-lambda-functions-with-lambda-snapstart/
- Lambda execution environment
  - https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html
- Amazon Security Lake
  - https://aws.amazon.com/jp/security-lake/

<style>
  @import url('https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css');        /* Bootstrap */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400&display=swap');    /* Noto Sans JP */
 
  pre {    /* code block */
    /*
    color: #fcfcfc;
    background-color: rgba(0, 0, 0, 0.8);
    */
    font-size: 20pt;
    text-align: left;
  }
  img {
    display: block;
    margin: 0 auto;
    width: 60%;
  }
  img[alt ~= 'icon'] {
    display: inline;
    margin: 0px -10px 10px 10px;
    height: 60px;
    width: auto;
  }
  header {
    width: 100%;
    text-align: left;
    left: 15px;
    top: 10px;
    font-size: 12pt;
    color: gray;
  }
  footer {
    box-sizing: border-box;
    border: 6px solid #6c2735;    /* burgundy */
    background-color: #6c2735;
    width: 100%;
    left: 0px;
    bottom: 0px;
    background-image: url(https://github.com/k0j1r0n0.png);    /* profile image */
    background-repeat: no-repeat;
    background-size: 2%;
    padding-left: 30px;
    font-size: 12pt;
    color: white;
  }
  section {
    justify-content: start;    /* make the text top-justified */
    font-family: 'Helvetica', 'Noto Sans JP';
    font-size: 22pt;
  }
  section::after {
    font-size: 15pt;
    color: white;
    bottom: 2px;
    /* insert page numbers as 'n/N' */
    content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
  }
  h1 {
    color: #6c2735;
    font-size: 28pt;
    position: absolute;
    top: 34px;
    left: 30px;
    width: 95%;
    padding: 0 0 0 45px;
    border-bottom: 3px solid gray;
  }
  h1::before, h1::after {
    font-size: 140%;
    content: '□';
    position: absolute;
  }
  h1::before {
    left: 0;
    top: -20px;
  }
  h1::after {
    left: 10px;
    top: -12px;
    color: gray;
  }
  h2 {
    color: darkorange;
    font-size: 24pt;
    position: relative;
    left: -24px;
    top: -10px;
    margin-bottom: -18px;
  }
  ul {
    list-style-type: none;
    position: relative;
    padding-left: 30px;
    padding-top: 2px;
  }
  li:before {
    display: block;
    position: absolute;
    left: 0px;
    color: gray;
    font-family: 'Helvetica';
    content: '●';
  }
</style>