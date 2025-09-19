# LCM Quality Project

このリポジトリは、**LCM不具合データを Power Query で集計・可視化**するための  
Excel ブックと参照テーブルを管理しています。  
品質データの共有と分析効率化を目的としています。

---

## 📂 フォルダ構成

```plaintext
LCM_Quality_Project/
├── data/         # 参照テーブル（マスタ類）
│   ├── CountermeasureMaster_tbl.xlsx        # 対策マスタ
│   ├── LocationMaster_tbl.xlsx              # 拠点マスタ
│   ├── LCM_InstalledModels_AllSites_tbl.xlsx # モデル・サイト対応表
│   └── ...（その他マスタ）
│
├── workbook/     # メインのダッシュボード
│   └── LCM_Quality_Dashboard_Dev_v0.xlsm
│
└── README.md     # この説明ファイル
```

---

## 🚀 セットアップ手順（新しいPCで使う場合）

**1. GitHub からクローン**

```bash
git clone https://github.com/kjfarm1225/LCM_Quality_Project.git
```

**2. Excel ブックを開く**

```plaintext
workbook/LCM_Quality_Dashboard_Dev_v0.xlsm
```

**3. Power Query のパスを更新**

- [データソース設定] → [パラメータ] でローカルパスを変更  
- `data/` フォルダを参照できるように設定

---

## 🛠 運用ルール

変更後は以下のコマンドで GitHub へ反映します。

```bash
git add .
git commit -m "update: データ更新 or クエリ修正"
git push
```

### コミットメッセージの推奨ルール

- `add:` 新しいマスタ・ブック追加  
- `update:` 既存データやクエリ更新  
- `fix:` 修正（バグや参照パスなど）

---

## 📜 更新履歴

- v0 : 初回コミット（ブックとマスタ登録）

---

## ✅ メモ

- `data/` フォルダのファイル名は変更しないこと（Power Query 参照エラー防止）
- 不要な一時ファイル（`~$*.xlsx` など）は `.gitignore` で除外することを推奨