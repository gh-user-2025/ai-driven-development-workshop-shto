# 工場設備管理アプリ プロトタイプ

## 概要説明

このデモ プロジェクトは、工場設備管理アプリのプロトタイプ開発をテーマとしています。工場内の設備の稼働状況やメンテナンス情報を一元管理し、効率的な運用をサポートすることを目的としています。

### プロジェクトの目的

- **設備の稼働状況のリアルタイム監視**: センサーを活用して、設備の稼働状況をリアルタイムで監視します。
- **メンテナンス管理**: 設備のメンテナンススケジュールを管理し、予防保全を実現します。
- **データ分析**: 設備の稼働データを分析し、効率的な運用方法を提案します。

### 使用技術

- **Azure Functions**: データの処理や分析を行います。
- **Azure SQL Database**: 収集したデータを保存します。
- **Azure Cosmos DB**: IoT デバイスからのデータをリアルタイムで処理します。
- **Power BI**: データの可視化と分析結果の共有を行います。

### 期待される成果

- 設備の稼働状況をリアルタイムで把握することで、ダウンタイムを削減します。
- メンテナンスの効率化により、設備の寿命を延ばします。
- データに基づいた運用改善提案により、生産性を向上させます。

### 開発条件

- **データセット**: 本デモでは、架空の工場の設備データを使用します。
- **開発環境**: Visual Studio Code などのコードエディタを使用します。
- **言語**: Python などのプログラミング言語を使用します。
- **デプロイ先**: Azure クラウド上にデプロイします。
- **開発手法**: AI-Driven Development を採用します。

### 開発環境のセットアップ

1. リポジトリをクローンします。
   ```bash
   git clone https://github.com/gh-user-2025/ai-driven-development-workshop-shto.git
   cd ai-driven-development-workshop-shto
   ```

2. 必要なツールをインストールします。
   - Node.js
   - Azure CLI
   - Vue CLI

3. 開発コンテナを起動します。
   ```bash
   code .
   # VSCodeで開いた後、コマンドパレットで "Remote-Containers: Reopen in Container" を選択します。
   ```

### Azure へのデプロイ手順

1. Azure にログインします。
   ```bash
   az login
   ```

2. リソースグループを作成します。
   ```bash
   az group create --name <リソースグループ名> --location <リージョン>
   ```

3. Azure Functions をデプロイします。
   ```bash
   az functionapp create --resource-group <リソースグループ名> --consumption-plan-location <リージョン> --runtime python --functions-version 3 --name <関数アプリ名> --storage-account <ストレージアカウント名>
   ```

4. Azure SQL Database を作成します。
   ```bash
   az sql server create --name <サーバー名> --resource-group <リソースグループ名> --location <リージョン> --admin-user <ユーザー名> --admin-password <パスワード>
   az sql db create --resource-group <リソースグループ名> --server <サーバー名> --name <データベース名> --service-objective S0
   ```

5. Azure Cosmos DB を作成します。
   ```bash
   az cosmosdb create --name <アカウント名> --resource-group <リソースグループ名> --locations regionName=<リージョン>
   ```

6. Power BI でデータを可視化します。
   - Power BI Desktop を使用して、Azure SQL Database や Azure Cosmos DB からデータを取得し、レポートを作成します。
   - 作成したレポートを Power BI サービスに公開します。

