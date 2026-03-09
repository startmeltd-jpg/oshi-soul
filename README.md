# oshi-soul

**OSHI Soul — subtask向け公開版の配信リポジトリ**

---

## このリポジトリの目的

`oshi-soul` は、OSHIエージェントの魂（soul.md）のうち、**subtaskが参照してよい公開部分のみ**を配信するためのパブリックリポジトリです。

内部運用ルール・Supabase接続情報・スクリプトパス・完了済みタスク記録などの機密情報は含まれていません。

---

## ファイル構成

| ファイル | 内容 |
|---------|------|
| `soul_public.md` | subtask向け公開版（思想・価値観・IP定義・原則） |
| `CHANGELOG.md` | 更新履歴 |

---

## soul_public.md の Raw URL

subtaskからは以下のURLで直接取得できます：

```
https://raw.githubusercontent.com/startmeltd-jpg/oshi-soul/main/soul_public.md
```

---

## 更新方法

`soul_public.md` は `oshi-core` リポジトリの `CORE/scripts/sync_soul_public.py` を使って自動更新されます。

```bash
# oshi-core リポジトリで実行
GITHUB_TOKEN=<your_token> python3 CORE/scripts/sync_soul_public.py
```

手動更新が必要な場合は、`oshi-core/soul.md` の公開可能な部分を抽出してこのリポジトリの `soul_public.md` を更新してください。

---

## 管理

- **coordinator**: `oshi-core` の `soul.md` が正本
- **subtask**: このリポジトリの `soul_public.md` を参照
- **更新スクリプト**: `oshi-core/CORE/scripts/sync_soul_public.py`
