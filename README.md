# 血液培養採取判定アプリ

成人の感染疑い患者を対象に、NEWS2、qSOFA、例外病態の有無から血液培養採取の目安を表示する静的Webアプリです。

## 使い方

`index.html` をブラウザで開くと、そのまま利用できます。サーバーやビルドは不要です。

NEWS2の各項目は、数値を直接入力するのではなく該当する範囲を選択して計算します。qSOFAはNEWS2の呼吸数、収縮期血圧、意識状態から自動計算します。

## 判定の概要

- 例外病態あり：血液培養2セットの採取を推奨
- NEWS2 5点以上：血液培養2セットの採取を推奨
- NEWS2 3-4点かつqSOFA 1点：血液培養2セットの採取を推奨
- NEWS2 3-4点かつqSOFA 2-3点：血液培養2セットを採取
- NEWS2 3-4点かつqSOFA 0点：個別判断
- NEWS2 0-2点：ルーチン採取は原則不要

## 根拠と位置づけ

NEWS2は、呼吸数、酸素飽和度、収縮期血圧、脈拍、意識状態、体温、酸素投与の有無から急性疾患の重症度を標準化して評価する早期警告スコアです。qSOFAは、感染が疑われる患者で予後不良リスクを示す簡便な臨床指標として提案され、呼吸数22回/分以上、収縮期血圧100 mmHg以下、意識変容の3項目で構成されます。

本フローは、NEWS2で全身状態を広く評価し、NEWS2 3-4点の中間リスクではqSOFAで臓器障害リスクを加えて層別化する院内運用案です。血液培養採取基準として前向き検証された標準基準ではないため、臨床判断を代替しません。

血液培養は、敗血症が疑われ抗菌薬投与が必要な場面で、投与前に可能な範囲で採取することが推奨されています。採取のために抗菌薬投与を大きく遅らせないでください。

NEWS2は通常のSpO2 Scale 1を使用しています。慢性高二酸化炭素血症でSpO2 Scale 2を用いる患者には未対応です。

## 出典

- Royal College of Physicians. National Early Warning Score (NEWS) 2. https://www.rcp.ac.uk/resources/national-early-warning-score-news-2/
- Seymour CW, et al. Assessment of Clinical Criteria for Sepsis. JAMA. 2016. https://pubmed.ncbi.nlm.nih.gov/26903335/
- Singer M, et al. The Third International Consensus Definitions for Sepsis and Septic Shock. JAMA. 2016. https://pubmed.ncbi.nlm.nih.gov/26903338/
- Evans L, et al. Surviving Sepsis Campaign: International Guidelines for Management of Sepsis and Septic Shock 2021. Intensive Care Med. 2021. https://pubmed.ncbi.nlm.nih.gov/34599691/
