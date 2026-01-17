# miyabi-ppal-plugin

Miyabi PPAL Plugin - Course Society for Claude Code

## 概要

オンラインコース・メンバーシップ運営のための6つの専門エージェント（Course Society）を提供する Claude Code プラグイン。

## Course Society エージェント

| エージェント | 読み | 役割 | トリガー |
|------------|------|------|---------|
| **しきるん** | しきるん | 統括・調整 | `/shikirun` |
| **まなぶん** | まなぶん | カリキュラム・Teachable | `/manabun` |
| **つくるん** | つくるん | コンテンツ制作 | `/tsukurun` |
| **ひろめるん** | ひろめるん | マーケティング・L-Step | `/hiromerun` |
| **ささえるん** | ささえるん | サポート | `/sasaerun` |
| **かぞえるん** | かぞえるん | 分析・KPI | `/kazoerun` |

## インストール

### 方法1: クローンして使用（推奨）

```bash
# 1. プラグインディレクトリにクローン
cd ~/.claude
git clone https://github.com/ShunsukeHayashi/miyabi-ppal-plugin.git
```

### 方法2: シンボリックリンク

```bash
# 既存のリポジトリがある場合
ln -s /Users/shunsukehayashi/dev/miyabi-ppal-plugin ~/.claude/miyabi-ppal-plugin
```

### Claude Code で有効化

Claude Code の設定ファイル `~/.claude/config.json` に以下を追加:

```json
{
  "plugins": [
    "~/.claude/miyabi-ppal-plugin"
  ]
}
```

または、プロジェクト単位で有効化する場合は、プロジェクトの `.claude/config.json` に:

```json
{
  "plugins": [
    "../miyabi-ppal-plugin"
  ]
}
```

## 使い方

### コマンド例

```
/shikirun ローンチ実行計画を作成して
/manabun Teachable商品を設定して
/tsukurun セールスレターを書いて
/hiromerun L-Step シナリオを作成して
/sasaerun FAQを作成して
/kazoerun KPIレポートを作成して
```

## プロジェクト構成

```
miyabi-ppal-plugin/
├── .claude-plugin/
│   └── plugin.json      # プラグイン設定
├── skills/
│   ├── shikirun/        # しきるん
│   ├── manabun/         # まなぶん
│   ├── tsukurun/        # つくるん
│   ├── hiromerun/       # ひろめるん
│   ├── sasaerun/        # ささえるん
│   └── kazoerun/        # かぞえるん
└── README.md
```

## ライセンス

MIT

## 作者

Shunsuke Hayashi

## 関連プロジェクト

- [PPAL](https://github.com/ShunsukeHayashi/PPAL) - Pro Prompt Agent Lab
