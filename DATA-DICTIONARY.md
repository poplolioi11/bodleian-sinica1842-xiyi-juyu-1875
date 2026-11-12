# 資料字典

`book.json`是公開原生結構主本。`pages`前25筆與0.3.0逐欄完全相同；後41筆保留固定來源裁定的568個原生單位、24則分離`notes`、`original_margin`及4個平行`tables`記錄。兩組ID保留原有形式，並非原書頁碼。新41按固定範圍順序列28面完整正文，再列13個選定圖表層，不是全書連讀順序。

`units[].text`與`notes[].text`是保留原字、原刻句讀及空白的文字。`layer`區分主文、圖題、圖字、小字、表格等。`canonical_offset`按單位自身或所屬面串接字串的Unicode codepoints計算，半開區間；未插入現代分隔符。`source_anchor`提供來源面／層定位；沒有字級證據即不造字框。

`original_margin`內的`running_title`、`original_page_label`、`month`、`book_header`、`page_label`只有字串值可投影為原版心文字。`chapter_context_from_initial`是篇章情境，`printed_chapter_running_title_on_this_face`是來源判斷旗標，兩者均不投影正文。不能因頁面屬某章，就把該章名當成本面另有原印題名。

`READING-MAP.json`保存小註附著、跨欄／跨面續接與表格讀序。`anchor.offset`是父字串Unicode codepoint邊界；`after_text`與該邊界前字串對應。`physical_source_page_id`指實際來源面，與註文的語意父單位分開。`TABLES.json`是原表結構的平行表示；原表文字已在原生單位中投影一次，不額外重錄。`column_roles`若明示editorial，僅為欄位解釋，不是原印表頭；○不換為0，不換算尺寸。

`uncertainties.json`保留前25面既有疑讀與52筆新41來源覆核後未解。`matching_ranges`及`locations`是零起算、終點不含的Unicode codepoint位置；多個匹配不自行挑定單一處。候選不是已採用讀法。`gaiji.json`保留前25面既有記錄及新41的一筆外字；外字標記與□依各自記錄解讀，不以標記長度推定原字數。

`EXPORT-MAP.json`逐單位列出TXT／TEI的來源類型、頁與順序；TXT及TEI均從公開主本固定投影。單位間的導航分隔與單位自身的原有換行不同。保存`book.json`、`EXPORT-MAP.json`、TXT／TEI及各自sidecar可無損重驗匯出，不需公開私人製作程式或工作紀錄。

`SOURCE-MAP.json`提供原件canvas、取得影像的SHA-256、可用尺寸與裁區。固定預覽座標不能稱為原生掃描字框。`CHANGES.json`列0.3.0至0.4.0的固定字串、增刪及結構差異，舊版差異另存。`VALIDATION.json`只報實跑的資料工程檢查，不認證文字正確、人類審定或法律權利。
