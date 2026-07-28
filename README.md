# ラジアン（柏木主税） / RadianN_kswg 👋

一次創作サークル **「百花繚乱研究所」** のサークル主。
**自分の創作活動を回すために必要な道具を、自分で要件定義して作る**ことを続けています。

- 🤖 **AI協働開発** — VS Code ＋ AIエージェント（Claude / GitHub Copilot / Codex）で、実用ツールとBotを設計から本番運用まで
- 🎨 **創作活動** — 一次創作「ナンバーテールズ」を中心に、公式サイト・キャラクターDB・VRMモデル・同人タロットなど

## 🧭 開発者としての現在地

**1. AIエージェントを「使う」だけでなく「働かせる」構成を設計している**
`AGENTS.md` を Single Source of Truth とし、`CLAUDE.md` / `copilot-instructions.md` を薄い入口として派生させる構成を複数リポジトリで運用中。MCP（Model Context Protocol）でAIから外部ツール・ローカルファイルを操作する連携も実装しています。

**2. AI生成コードを検証する仕組みを持っている**
`APHRNTs_100` は実装 約5,200行に対しテスト 約4,200行（vitest 46ファイル）。AIに書かせたコードをそのまま通さず、テストで検証してからマージする運用です。

**3. 要件定義から本番運用・障害対策まで一人で通している**
Misskey AI Bot 3本を運用中（うち2本はGCP上で常時稼働）。`master`マージ後の自動デプロイと、3層ウォッチドッグ（プロセス / VM内 / VM外部）による自動復旧まで構築しています。1本目で作った運用基盤を2本目へ横展開しました。

## 🤖 主力プロジェクト

| リポジトリ | 概要 | 技術 |
|---|---|---|
| [APHRNTs_100](https://github.com/radiann-kswg/APHRNTs_100) | 生活管理・セルフケア支援のMisskey AI Bot。**本番稼働中**。マルチLLM抽象化 / Tool use / SQLite永続化 / Markdown⇄DB双方向同期 / 危機検知 | TypeScript |
| [NumberTales-MisskeyAIBot](https://github.com/radiann-kswg/NumberTales-MisskeyAIBot) | 創作キャラクターのMisskey AI Bot。**本番稼働中**。創作DBからのプロンプト動的生成 / 週次担当のPoll選出 / 3層ウォッチドッグ | TypeScript |
| [Tarot-byFateLineDealer](https://github.com/radiann-kswg/Tarot-byFateLineDealer) | タロット占いBot「錦野舞」。**Claude / Copilot / Codex / Misskey Bot の4つの入口が、同じ正本を実行時に読む**構成。設定を複製せず1箇所の変更で全環境が変わる | Python |
| [100BeautiesLab_CreationsDB](https://github.com/radiann-kswg/100BeautiesLab_CreationsDB) | 創作キャラクターの公開データベース。**GitHub Pages上でService Workerによる擬似REST APIを3スコープ実装**。スキーマ定義・参照解決エンジン付き | JavaScript |
| [PenchantManufacture_ImageAssets](https://github.com/radiann-kswg/PenchantManufacture_ImageAssets) | 自作英数字フォント「PenchantManufacture」のSNS向け図柄絵文字アセット集。生成をバッチ化 | Python |
| [RadianNs_WebSite](https://github.com/radiann-kswg/RadianNs_WebSite) | サークル主のオフィシャルサイト。Vue.js 3 ＋ SASS / GitHub Pages | TypeScript |
| [TENTOBI](https://github.com/radiann-kswg/TENTOBI) | 「天動説を唱えた罰がぶっ飛んでいる件について」チーム制作ゲーム | C++ |

## 🛠️ 制作したツール

「日々の作業で面倒なこと」をその都度ツール化してきました。**発注者は自分**です。

| リポジトリ | 概要 |
|---|---|
| [QuickPNG-Tinize4Web](https://github.com/radiann-kswg/QuickPNG-Tinize4Web) | Web向けPNG縮小・圧縮の一括バッチ（Python） |
| [QuickPNG-SmartObjectExport](https://github.com/radiann-kswg/QuickPNG-SmartObjectExport) | PSDのスマートオブジェクトを一括PNG出力（Python） |
| [Secvier_ImageAssets](https://github.com/radiann-kswg/Secvier_ImageAssets) | 独自英数字フォント「Secvier」のSNS向け絵文字アセット集 |
| [AstroScope](https://github.com/radiann-kswg/AstroScope) | 占星術の道具を扱えるUnityアプリ（GitHub Copilotと共同開発 / C#） |
| [QuaternionViewer](https://github.com/radiann-kswg/QuaternionViewer) | クォータニオン学習用ビューア（C#） |
| [CheatSheet-of_HttpResponceDataCode](https://github.com/radiann-kswg/CheatSheet-of_HttpResponceDataCode) | HTTPステータスコードのチートシート（GitHub Copilotと共同整備） |
| [ChearSheet-of_Numbers](https://github.com/radiann-kswg/ChearSheet-of_Numbers) | 数字の科学的性質・文化的いわれのチートシート（AIエージェントと共同整備） |

## 🎨 創作活動

一次創作 **「ナンバーテールズ」** を中心に活動しています。上記のツール群は、いずれもこの活動の中で実際に困ったことから生まれました。

- 🏠 オフィシャルサイト: https://www.numbertales-radiann.net
- 🗃️ 創作キャラクターDB: https://database.numbertales-radiann.net

| リポジトリ | 概要 |
|---|---|
| [NumberTales-HTML_CSS](https://github.com/radiann-kswg/NumberTales-HTML_CSS) | 一次創作「ナンバーテールズ」公式サイト |
| [SeventyEight-HTML_CSS](https://github.com/radiann-kswg/SeventyEight-HTML_CSS) | 同人タロット制作中の「運命線探偵」公式サイト |
| [ShouArRider-HTML_CSS](https://github.com/radiann-kswg/ShouArRider-HTML_CSS) | 年賀イラスト・ショートストーリー中心の「獣爾騎兵」公式サイト |
| [100BeautiesLab-CharacterVRMs](https://github.com/radiann-kswg/100BeautiesLab-CharacterVRMs) | 創作キャラクターのVRMモデル |
| [Plus-Minus-NumberTales](https://github.com/radiann-kswg/Plus-Minus-NumberTales) | ナンバーテールズ公式パズルアクションゲーム（Unity / C#）。[unityroomで公開中](https://unityroom.com/games/plus-minus-numbertales) |

## 🤝 協働リポジトリ（ゲームジャム等）

2021年から継続的に、短期チーム開発（ゲームジャム等）へ **5回** 参加しています（※印は他オーナー管理のリポジトリ）。
活動記録は[オフィシャルサイト](https://www.numbertales-radiann.net/)にも掲載しています。

| リポジトリ | 概要 |
|---|---|
| [Plus-Minus-5](https://github.com/radiann-kswg/Plus-Minus-5) | 「Global Game Jam 2022」瀬戸内会場 出場作品（Unity / C#）。のちに『[Plus-Minus-NumberTales](https://github.com/radiann-kswg/Plus-Minus-NumberTales)』としてリニューアル（[SXG2022](https://www.numbertales-radiann.com/news/news202206_sxg2022.html) / [SXG2023](https://www.numbertales-radiann.com/news/news202311_sxg2023.html)） |
| KokounoKensei ※ | 『[孤高の剣聖](https://unityroom.com/games/kokounokensei)』—「[ゲームジャム高梁2021](https://gjtakahashi.okayamaunity.com/gjtakahashi2021/)」方谷賞受賞作。PGとして参加（uyaman2014） |
| SaikyoGameJam2023 ※ | 「[最強ゲームジャム2023](https://www.e-topia-kagawa.jp/lecture/saikyo_game_jam_2023/)」参加作品。[unityroomで公開中](https://unityroom.com/games/saikyogamejam2023c)（k-mitani） |
| MonkeytoHuman ※ | 『[モンキー・トゥ・ヒューマン](https://v3.globalgamejam.org/2023/games/monky-human-%E3%83%A2%E3%83%B3%E3%82%AD%E3%83%BC%E3%83%BB%E3%83%88%E3%82%A5%E3%83%BB%E3%83%92%E3%83%A5%E3%83%BC%E3%83%9E%E3%83%B3-2)』—「Global Game Jam 2023」参加作品。[2D版をunityroomで公開中](https://unityroom.com/games/monkey-to-human-2d)（kazu0826 / Moriarium） |
| GlobalgameJam2025 ※ | 『[Bubble Crab](https://globalgamejam.org/games/2025/bubble-crab-9)』—「Global Game Jam 2025」参加作品。[unityroomで公開中](https://unityroom.com/games/bubblecrab)（naninunenoy） |

## 💻 使用技術

| 区分 | 内容 |
|---|---|
| 言語 | TypeScript / Python / C# / C++ / JavaScript / HTML・CSS(SASS) |
| フレームワーク等 | Node.js / Vue.js 3 / Unity / vitest |
| インフラ | GCE / Cloud Run functions / Cloud Scheduler / Cloudflare Workers / GitHub Pages / systemd |
| データ | SQLite / Service Worker擬似API / JSONスキーマ設計 |
| AI協働 | Claude（Desktop / Code / Cowork） / GitHub Copilot / GPT Codex / MCP |
| その他 | Git / GitHub Actions / VRM・Unity(VRChat) |

## 🌐 運営

- **Misskeyサーバ「[shapesky](https://shapesky.xsns.jp/)」の管理者** — 規約策定・連合設定・カスタム絵文字の権利主/ライセンス別の仕分け運用・問い合わせ窓口の維持（ホスティング利用の小規模サーバ・試験運用中）
- **Misskey AI Bot 3本を運営中** — ナンバーテールズBot `@APHR_NTs` / メンタルケアBot「100(モモ)」`@APHR_NTs_100` / タロット占いBot「錦野舞」
- 利用条件を明文化したガイドラインを**日英2言語**で公開・維持

## 📜 資格

- C言語プログラミング能力認定試験 2級（サーティファイ）
- 情報処理技術者能力認定試験 2級（サーティファイ）

## 🔗 リンク

- 🧑‍💻 技術ポートフォリオ: https://www.numbertales-radiann.net/tech/
- 🎨 pixiv: https://www.pixiv.net/users/44375569
- ✉️ Skeb: https://skeb.jp/@RadianN_kswg
