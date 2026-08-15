# AWS SAA QUEST ダッシュボード

`index.html` は、Notionの「⚔️ AWS SAA QUEST」(World Map / Quest Log / Battle Log)を見るための
単一HTMLダッシュボード。Claudeのartifact機能でホストしたものと同じソースをここにも保存している。

## 仕組み

- 開いたブラウザから `window.claude.mcp` 経由でNotionのデータソースへ直接クエリを投げ、
  ライブで表示する(閲覧者自身のNotion連携が必要)。
- Notion連携がない環境で開いた場合は、ファイル内に埋め込まれた最終スナップショットを表示する。
- 外部ビルドやサーバーは不要。`index.html` 単体で完結する。

## 更新方法

このファイルはNotionのDB構造やダッシュボードのデザインを変えたときに手動で差し替える。
自動同期パイプラインは意図的に組んでいない(学習の妨げにならないよう、運用コストを増やさない方針)。
