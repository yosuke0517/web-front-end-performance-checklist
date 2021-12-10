# web-front-end-performance-checklist

---

# 1. 測定する
- ツールでの測定
  - [PageSpeed Insights](https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect&hl=ja)
    - [ ] スコアを測定する（100点に近ければ近いほど良いがリソースと
    - [ ] 実施した際の費用（リソース等）と効果のバランスを検討する
  - [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=ja)
    - [ ] スコアを測定する（100点に近ければ近いほど良いがリソースと
    - [ ] 実施した際の費用（リソース等）と効果のバランスを検討する
  - [newrelic（継続的監視）](https://newrelic.com/lp/browser-monitoring)
    - [ ] パフォーマンスを測定しボトルネックを特定する
- Networkパネルでの測定（時間がかかっている処理を特定する）
  - [ ] DOMContentLoaded （青い線）
    - 遅い場合、スクリプトによる読み込みによる読み込みブロックの可能性あり（JavaScript実行のチューニング参照）
  - [ ] Loadイベント（赤い線）
    - 遅い場合、リソースの容量が大き過ぎる可能性あり
  - ※Networkパネルでの各項目についての詳細は[コチラ](https://fuzzy-hunter-3bf.notion.site/Web-c945271a34b54e4c8a6b5c3b0d7ffd30#1a8908946aca4f03a54f1fdc8da5b0fb)
- Performanceパネルでの測定
  - [] ボトルネックの特定
    - Frame内でどこに一番時間がかかっているのかを特定する
      1. リソース読み込み（Loading）
      2. JavaScript実行（Scripting）
      3. レイアウト計算（Rendering）
      4. レンダリング結果の描画（Painting）
- Memoryパネルでの測定
  - [ ] メモリを使い過ぎている箇所を特定する