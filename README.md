# fake_site_early_action
このリポジトリは、Google CloudのCloud Functionsで実行される複数のPythonプログラムで構成される、偽サイト早期対策システムの実装を含んでいます。

## 概要

偽サイトは、ユーザーを騙して個人情報やクレジットカード情報を盗むことを目的としたウェブサイトです。このような偽サイトを早期に検出し、対策を講じることは、ユーザーの安全を守る上で非常に重要です。

このシステムでは、以下の複数のPythonプログラムが連携して動作します。

1. **URL収集プログラム:** 偽サイトの可能性があるURLを収集します。
2. **サイト解析プログラム:** 収集したURLのウェブサイトを解析し、偽サイトの可能性を判定します。
3. **アラート通知プログラム:** 偽サイトの可能性が高いと判定された場合、関係者にアラートを通知します。

## 構成

リポジトリの構成は以下の通りです。
```
.
├── README.md
├── fuctions
│   ├── get_seed_urlscan
│   │   ├── main.py
│   │   └── requirements.txt
│   ├── gsb
│   │   ├── main.py
│   │   └── requirements.txt
│   ├── notifications
│   │   ├── main.py
│   │   └── requirements.txt
│   └── request_urls
│       ├── main.py
│       └── requirements.txt
├── rules
│   ├── common_rules.yaml
│   └── matching_rules.yaml
└── workflows
    ├── wf_check_notifications.yaml
    └── wf_urlscan_check_notifications.yaml
```


- `functions`ディレクトリには、Cloud Functionsで実行されるPythonプログラムが格納されています。
- `requirements.txt`には、必要なPythonライブラリが記述されています。
- `README.md`はこのファイルです。

## 使い方

1. このリポジトリをクローンします。
2. Google Cloudプロジェクトを作成し、Cloud Functionsを有効にします。
3. `requirements.txt`に記述されたライブラリをインストールします。
4. 各PythonプログラムをCloud Functionsにデプロイします。
5. 必要に応じて、各プログラムの設定を変更します。

## 環境

このシステムは、以下の環境で動作します。

- Python 3.12.3
- Google Cloud Functions

## ライセンス

このシステムは、MITライセンスで提供されています。

## 作者

このシステムの作者は、ytsuboi0322 です。

## 連絡先

このシステムに関するお問い合わせは、yuichi.tsuboi@ntt.com までご連絡ください。
