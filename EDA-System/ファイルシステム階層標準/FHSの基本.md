# ファイルシステム階層標準（FHS: Filesystem Hierarchy Standard）

## FHS（Filesystem Hierarchy Standard）の主要なディレクトリ構造

```markdown
/
├── /bin     - 基本的なコマンド（ls, cp など）
├── /sbin    - システム管理用コマンド（root向け）
├── /usr     
│   ├── /bin   - 追加的なコマンド
│   ├── /sbin  - 追加的なシステム管理コマンド
│   ├── /lib   - 共有ライブラリ、モジュール
│   ├── /local - システム管理者がインストールするソフトウェア
│   └── /share - アーキテクチャ独立なデータ
├── /etc     - 設定ファイル
├── /home    - ユーザーのホームディレクトリ
├── /lib     - 重要な共有ライブラリ、カーネルモジュール
├── /opt     - 追加アプリケーションパッケージ（EDAツールがよくインストールされる）
├── /tmp     - 一時ファイル
└── /var     - 可変データ（ログなど）
```

## EDAにおける重要なポイント

1. `/opt` や `/usr/local`
   - Synopsysなどのベンダーツールがよくインストールされる場所
   - ライセンスファイルの配置場所としてもよく使用される

2. `/etc`
   - シェル設定（cshの設定など）
   - ライセンスデーモンの設定
   - QUEUEシステムの設定

3. `/usr/lib`
   - EDAツールが使用する共有ライブラリ
   - ツールの依存関係を確認する際に重要

4. `/home`
   - ユーザーの`.cshrc`, `.vimrc`などの設定ファイル
   - 作業ディレクトリ
