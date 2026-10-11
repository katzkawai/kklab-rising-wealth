# kklab-rising-wealth

米国家計の純資産：上位1%と下位50%（実質値）

FRB「Distributional Financial Accounts（DFA）」の四半期純資産（2000Q1〜2026Q2）を、PCE価格指数（PCEPI）と CPI-U（CPIAUCSL）で2026年第2四半期ドルに実質化し、NBC News "Rising wealth" の図を再構成したページです。

- 公開ページ: https://katzkawai.org/kklab-rising-wealth/
- データ: `data.csv`（兆ドル。名目・PCE実質・CPI実質、全家計に占めるシェア、各四半期末月の物価指数）

## 出典
- Board of Governors of the Federal Reserve System, Distributional Financial Accounts — `dfa-networth-levels.csv`
- 上位1% = Top 0.1% + 99–99.9th（FRED `WFRBLT01026` と一致）／下位50% = FRED `WFRBLB50107`
- U.S. BEA, PCE Price Index (`PCEPI`); U.S. BLS, CPI-U (`CPIAUCSL`) — FRED 経由、季節調整済み月次

## 方法
純資産は四半期末のストックなので、各四半期末月（3・6・9・12月）の物価指数で換算：実質値 = 名目値 × P(2026Q2) / P(t)。データ取得日 2026-10-12。
