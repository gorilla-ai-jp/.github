# .github

このリポジトリは gorilla-ai-jp オーガニゼーションのプロフィール README(`profile/README.md`)と、各リポジトリに共通で適用されるコミュニティ用ファイルを管理します。

This repository holds the organization profile (`profile/README.md`) and default community health files shared across gorilla-ai-jp repositories.

## 新規リポジトリの作成手順 / New repository checklist

1. `oss-template` から「Use this template」で作成する(公開)
2. `main` 保護ルールを適用する

   ```bash
   gh api -X POST repos/gorilla-ai-jp/<repo>/rulesets --input rulesets/protect-main.json
   ```

3. 脆弱性の非公開報告を有効にする

   ```bash
   gh api -X PUT repos/gorilla-ai-jp/<repo>/private-vulnerability-reporting
   ```

Dependabot とシークレットスキャンは組織の既定値で自動的に有効になります。
