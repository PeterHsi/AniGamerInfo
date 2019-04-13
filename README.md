# AniGamerInfo

此專案將自動抓取[巴哈動畫瘋](https://ani.gamer.com.tw)官網新番觀看數並統計，統計檔案將以 `.csv`下載入 [/DailyData](/DailyData) 資料夾，命名規則為：

```
AGI_Daily_YYYYmmdd-HHMM.csv
```

其中 `YYYY` 為西元年，`mm` 為月，`dd` 為日，`HH` 為時(24小時制)，`MM` 為分，時區為 UTC/GMT+8 (台北時區)。

## 資料檔說明

||title|vol|update|number|date|
|---|---|---|---|---|---|
| 30     | 輝夜姬想讓人告白～天才們的戀愛頭腦戰～ | 12   | 03/31  | 3450913 | 2019/04/13 01:00:01 |
|(說明)|動畫標題|更新集數|最後更新日期(月/日)|累計觀看數(次)|資訊記錄時間點 (西元年/月/日 時:分:秒)|

## 排程指令

本專案目前放置在個人電腦內以排程方式執行，指令如下：

```shell
cd /your path here/
git config credential.helper store #第一次需要執行此行
git pull
python3 AGI_Daily_DWer.py
git add .
git commit -a -m "Scheduled Commit: `date`"
git push
```

其中 [`AGI_Daily_DWer.py`](AGI_Daily_DWer.py) 為抓取之 Python 程式碼。

## 已知問題(尚未解決工作)

- [ ] `AGI_Daily_DWer.py` 所有資料會重複抓取兩次(汗)
- [ ] 需要每週統整檔案
- [ ] 前人自行統計之往期需要匯入(希望能與批踢踢西洽版大大洽談資料引用)
- [ ] 自動排程仍須研究(目前個人只會用設定的方式執行)
