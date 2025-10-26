# KMG JavaFX（kmg-javafx）

[![Java](https://img.shields.io/badge/Java-21-orange.svg)](https://www.oracle.com/java/)
[![JavaFX](https://img.shields.io/badge/JavaFX-26--ea12-blue.svg)](https://openjfx.io/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.6-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![Maven](https://img.shields.io/badge/Maven-3.x-blue.svg)](https://maven.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

kmg-javafx（以降は、「KMG JavaFX」と言う。）は、KMG シリーズの JavaFX アプリケーション開発のための基盤となるライブラリです。

特徴は、JavaFX フレームワークをベースに、多くのプロジェクトで使用できるように構成されています。

## 概要

本プロジェクトは、以下の機能を提供します：

- JavaFX アプリケーション基盤
- テスト基盤機能
- JUnit テストサポート
- TestFX テストフレームワーク統合

## ドキュメント

詳細なドキュメントは [docs/](docs/) ディレクトリに格納されています：

## プロジェクト構成

```bash
kmg-javafx/
├── src/
│   ├── main/java/kmg/javafx/
│   │   ├── infrastructure/
│   │   │   └── test/           # テスト基盤
│   │   │       └── AbstractKmgJunitTest.java  # JUnitテスト抽象クラス
│   │   └── package-info.java   # パッケージ情報
│   ├── main/resources/         # リソースファイル
│   └── test/java/kmg/javafx/
│       └── infrastructure/
│           └── test/           # テスト基盤テスト
│               └── AbstractKmgJunitTestTest.java  # テスト基盤のテスト
├── docs/                       # ドキュメント
│   ├── javadoc/               # Javadoc
│   └── 設計書/                 # 設計書
│       └── インフラストラクチャ層テスト層の設計書.md
└── pom.xml                    # Maven設定ファイル
```

## 開発環境

- Java 21
- JavaFX 26-ea+12
- Spring Boot 3.5.6
- Maven 3.x
- JUnit Jupiter 5.13.4
- TestFX 4.0.18
- OpenJFX Monocle 21.0.2

### ビルドツール

- Maven Compiler Plugin 3.12.1
- Maven Surefire Plugin 3.2.5（JUnit テストレポート用）
- JaCoCo Maven Plugin 0.8.14（カバレッジレポート用）
- Spring Boot Maven Plugin 3.5.6
- JavaFX Maven Plugin 0.0.8
- Exec Maven Plugin 3.6.2

### プロジェクト情報

- グループ ID: kmg.javafx
- アーティファクト ID: kmg-javafx
- バージョン: 0.1.0
- エンコーディング: UTF-8

## ビルド方法

```bash
mvn clean install
```

## テスト実行

```bash
mvn test
```

## JavaFX アプリケーション実行

### Maven を使用した実行

```bash
mvn javafx:run
```

### Exec Maven Plugin を使用した実行

```bash
mvn exec:java
```

## 主要機能

### テスト基盤

#### AbstractKmgJunitTest

KMG シリーズの JUnit テストの抽象クラスです。以下の機能を提供します：

- **KMG Fund 例外の検証**: `verifyKmgFundException()` メソッド
- **KMG Core 例外の検証**: `verifyKmgCoreException()` メソッド
- **例外メッセージの検証**: ドメインメッセージとメッセージタイプの検証
- **原因クラスの検証**: 例外の原因クラスの検証

#### テスト機能

- JUnit Jupiter 5 サポート
- TestFX 4.0.18 統合
- OpenJFX Monocle 21.0.2 サポート（ヘッドレステスト用）

## 依存関係

### 主要依存関係

- **kmg-core**: KMG コアライブラリ（0.2.1）
- **kmg-fund**: KMG 基盤ライブラリ（0.1.1）
- **JavaFX Controls**: JavaFX コントロール（26-ea+12）
- **JavaFX FXML**: JavaFX FXML サポート（26-ea+12）
- **JavaFX Graphics**: JavaFX グラフィックス（26-ea+12）
- **JavaFX Base**: JavaFX ベース（26-ea+12）

### テスト依存関係

- **TestFX Core**: TestFX テストフレームワーク（4.0.18）
- **TestFX JUnit5**: TestFX JUnit5 サポート（4.0.18）
- **OpenJFX Monocle**: ヘッドレステスト用（21.0.2）

## 設定ファイル

### Maven 設定

- `pom.xml` - Maven プロジェクト設定
- JavaFX Maven Plugin 設定
- Exec Maven Plugin 設定

### リポジトリ設定

- GitHub Packages リポジトリ
- KMG シリーズ依存関係管理

## ライセンス

本プロジェクトは LICENSE ファイルに記載の条件の下で提供されています。

## 貢献について

バグ報告や機能改善の提案は、GitHub の Issue を通じてお願いします。

### 貢献の方法

1. リポジトリをフォーク
2. 機能ブランチを作成（`git checkout -b feature/amazing-feature`）
3. 変更をコミット（`git commit -m 'Add some amazing feature'`）
4. ブランチにプッシュ（`git push origin feature/amazing-feature`）
5. プルリクエストを作成

### コーディング規約

- Java コーディング規約に従う
- 適切な Javadoc コメントを記述
- 単体テストを必ず作成
- テストカバレッジ 100% を維持

---

**kmg-javafx** - JavaFX アプリケーション開発のための基盤ライブラリ
