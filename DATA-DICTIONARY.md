# 資料欄位與閱讀方法

`book.json`是本書資料：`pages`前25筆與0.2.0完全相同；後41筆保留凍結初錄單位陣列、來源定位、分離`notes`、`original_margin`及平行`tables`結構。兩組ID維持既有形式：前25面使用`sinica1842-c...`，新增面使用`c...`，不是新增的原書頁碼。新頁按凍結範圍順序列28面正文，再列13個選定圖表層，並非全書連讀次序。

`book.json`是公開結構主本，保留頁來源、層與單位；公開TXT／TEI依同一匯出映射衍生。`EXPORT-MAP.json`逐單位說明來源：原頁單位、分離原註或由固定版心欄位衍生的匯出單位。原表的文字已在新561個單位內，`TABLES.json`不再加入額外文字單位。各單位可含原有換行與製表符。

`book.txt.sidecar.json`用0起算Unicode碼位範圍（結尾不含）定位TXT字串。TXT單位間另加一個換行；這不是原刻標點。`book.tei.sidecar.json`把相同單位與頁ID對映TEI的xml:id。TEI正文只承載同一單位字串，疑讀、表格與錨點的完整結構在JSON；不宣稱完整校勘TEI。保留sidecar、book.json與EXPORT-MAP.json才能無損回讀。

`READING-MAP.json`保留4處原有小字錨點、新21註及4表位置。新註`anchor.offset`是含原刻句讀的父單位Unicode碼位邊界；`after_text`提供原有定位片段。部分錨點、分類與表格對齊是暫定，原狀態不提高。跨頁續註有`continuation_of`，正文父單位不一定在註記所在面。

`uncertainties.json`前32筆為原有疑讀／印章記錄，另有144筆新初錄疑讀。`matching_ranges`僅列字串精確出現位置；多個匹配時不自行決定哪一處。候選不是已採用讀法。`gaiji.json`保留既有12筆及新7筆；`[[G...]]`、`⟦g...⟧`及`□`依來源記錄解讀，不一概推定缺字數。原字數未知時不改成一字。

`SOURCE-MAP.json`提供官方canvas／影像入口、來源檔hash及已知尺寸。bbox僅有來源面或區塊精度，未校準逐字框不造座標。c060右的URL是右半部定位連結，實得檔為固定預覽的無損裁片，並非由該URL直接下載。原刻頁標記、影像序及資料索引分開。

`CHANGES.json`記錄0.3.0新增範圍及舊25面不變；`CHANGES-v0.2.0.json`保存前版的逐項來源修訂。`COVERAGE.json`與`READING-GUIDE.md`說明排除與母刊現有文字，不把未轉錄內容當空白或已完成。
