本資料來源: 
http://www.ucamc.com/e-learning/javascript/194-javascript-browser-language-code.html
http://www.wibibi.com/info.php?tid=400

Javascript 取得遊覽器語系代碼

navigator 對像中的這幾個與 language 相關的屬性。
navigator 對象包含有關瀏覽器的信息。沒有應用於 navigator 對象的公開標準，不過所有瀏覽器都支持該對象。但是其內部一些屬性及其返回值在各瀏覽器並不統一。

language：返回當前的瀏覽器語言（來自 Mozilla Developer Center）
userLanguage：返回操作系統設定的自然語言（來自 MSDN）
browserLanguage：返回當前的瀏覽器語言（來自 MSDN）
systemLanguage：返回當前操作系統的缺省語言（來自 MSDN）

使用以下代碼在各不同遊覽器打印出並分析：
<script>
document.write('navigator.language:'+navigator.language);
document.write('<br>navigator.userLanguage:'+navigator.userLanguage);
document.write('<br>navigator.browserLanguage:'+navigator.browserLanguage);
document.write('<br>navigator.systemLanguage:'+navigator.systemLanguage);
</script>

4 個屬性返回值的情況如下：
對象 : IE6 IE7 IE8 | Firefox Chrome Safari | Opera
navigator.language: undefined | zh-TW | zh-TW
navigator.userLanguage: zh-tw| undefined | zh-tw
navigator.browserLanguage: zh-tw| undefined | zh-tw
navigator.systemLanguage: zh-tw| undefined | undefined

同時獲取navigator.language與navigator.browserLanguage，並且在做toLowerCase()轉成小寫字母：
(navigator.language || navigator.browserLanguage).toLowerCase()
以上取得遊覽器語言代碼後，就可配合需求使用判斷式，以下提供各國語言代碼提供參考對照。

各國語言代碼表語言代碼對照表Language Codes Table
af 南非荷蘭語	sq 阿爾巴尼亞語
ar-sa 阿拉伯語(沙特阿拉伯)	ar-iq 阿拉伯語(伊拉克)
ar-eg 阿拉伯語(埃及)	ar-ly 阿拉伯語(利比亞)
ar-dz 阿拉伯語(阿爾及利亞)	ar-ma 阿拉伯語(摩洛哥)
ar-tn 阿拉伯語(突尼斯)	ar-om 阿拉伯語(阿曼)
ar-ye 阿拉伯語(也門)	ar-sy 阿拉伯語(敘利亞)
ar-jo 阿拉伯語(約旦)	ar-lb 阿拉伯語(黎巴嫩)
ar-kw 阿拉伯語(科威特)	ar-ae 阿拉伯語(阿拉伯聯合酋長國)
ar-bh 阿拉伯語(巴林)	ar-qa 阿拉伯語(卡塔爾)
eu 巴斯克語	bg 保加利亞語
be 貝勞語	ca 加泰羅尼亞語
zh-tw 中文(中國台灣)	zh-cn 中文(中華人民共和國)
zh-hk 中文(中國香港特別行政區)	zh-sg 中文(新加坡)
hr 克羅地亞語	cs 捷克語
da 丹麥語	nl 荷蘭語(標準)
nl-be 荷蘭語(比利時)	en 英語
en-us 英語(美國)	en-gb 英語(英國)
en-au 英語(澳大利亞)	en-ca 英語(加拿大)
en-nz 英語(新西蘭)	en-ie 英語(愛爾蘭)
en-za 英語(南非)	en-jm 英語(牙買加)
en 英語(加勒比)	en-bz 英語(伯利茲)
en-tt 英語(特立尼達)	et 愛沙尼亞語
fo 法羅語	fa 波斯語
fi 芬蘭語	fr 法語(標準)
fr-be 法語(比利時)	fr-ca 法語(加拿大)
fr-ch 法語(瑞士)	fr-lu 法語(盧森堡)
gd 蓋爾語(蘇格蘭)	gd-ie 蓋爾語(愛爾蘭)
de 德語(標準)	de-ch 德語(瑞士)
de-at 德語(奧地利)	de-lu 德語(盧森堡)
de-li 德語(列支敦士登)	el 希臘語
he 希伯來語	hi 北印度語
hu 匈牙利語	is 冰島語
in 印度尼西亞語	it 意大利語(標準)
it-ch 意大利語(瑞士)	ja 日語
ko 朝鮮語	ko 朝鮮語(韓國)
lv 拉脫維亞語	lt 立陶宛語
mk FYRO 馬其頓語	ms 馬來西亞語
mt 馬耳他語	no 挪威語(博克馬爾)
no 挪威語(尼諾斯克)	pl 波蘭語
pt-br 葡萄牙語(巴西)	pt 葡萄牙語(葡萄牙)
rm 拉丁語系	ro 羅馬尼亞語
ro-mo 羅馬尼亞語(摩爾達維亞)	ru 俄語
ru-mo 俄語(摩爾達維亞)	sz 薩摩斯語(拉普蘭)
sr 塞爾維亞語(西里爾)	sr 塞爾維亞語(拉丁)
sk 斯洛伐克語	sl 斯洛文尼亞語
sb 索布語	es 西班牙語(西班牙傳統)
es-mx 西班牙語(墨西哥)	es 西班牙語(西班牙現代)
es-gt 西班牙語(危地馬拉)	es-cr 西班牙語(哥斯達黎加)
es-pa 西班牙語(巴拿馬)	es-do 西班牙語(多米尼加共和國)
es-ve 西班牙語(委內瑞拉)	es-co 西班牙語(哥倫比亞)
es-pe 西班牙語(秘魯)	es-ar 西班牙語(阿根廷)
es-ec 西班牙語(厄瓜多爾)	es-cl 西班牙語(智利)
es-uy 西班牙語(烏拉圭)	es-py 西班牙語(巴拉圭)
es-bo 西班牙語(玻利維亞)	es-sv 西班牙語(薩爾瓦多)
es-hn 西班牙語(洪都拉斯)	es-ni 西班牙語(尼加拉瓜)
es-pr 西班牙語(波多黎各)	sx 蘇圖語
sv 瑞典語	sv-fi 瑞典語(芬蘭)
th 泰語	ts 湯加語
tn 瓦納語	tr 土耳其語
uk 烏克蘭語	ur 烏爾都語
ve 文達語	vi 越南語
xh 科薩語	ji 依地語
zu 祖魯語	 
