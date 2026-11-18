# 資料欄位

`book.json` 的 pages 依來源順序排列，units 依 page_id 連回來源位置。每個單元含識別碼、原字串、層別、版面角色和覆核狀態。bbox 是對應來源框位，null 表示目前沒有可安全共用的框位。疑讀和缺損可含候選、來源與字串範圍。

main_unit_sequence 記正文單元的連讀順序。note_insertions 用單元 ID、Unicode 碼位及小註各段順序記錄插入位置。figure_unit_groups 保留圖字群。SOURCE-MAP.json 含畫布網址及已知工作影像尺寸。

READER-MAP.json、TXT 及 TEI 的 sidecar 把公開字串定位回同一 JSON 單元。歷史字形與表格的前版詳細編碼仍可從 gaiji.json 及 TABLES.json 查閱。
