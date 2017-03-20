# EmojiRegex
EmojiRegex


### 一、emoji 的范围

[查阅维基百科中 emoji 的说明](https://zh.wikipedia.org/wiki/%E7%B9%AA%E6%96%87%E5%AD%97#Unicode_.E5.8C.BA.E5.9D.97)

#### 1. [杂项符号及图形](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Miscellaneous_Symbols_and_Pictographs)

杂项符号及图形一共有768个字符，范围为： U+1F300 ～ U+1F5FF，在 Java 中正则表达式为：

```
"[\\uD83C\\uDF00-\\uD83D\\uDDFF]"
```

#### 2. [增补符号及图形](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Supplemental_Symbols_and_Pictographs)

增补符号及图形中一共有82个字符，范围为： U+1F900 ～ U+1F9FF，在 Java 中正则表达式为：

```
"[\\uD83E\\uDD00-\\uD83E\\uDDFF]"
```

#### 3. [表情符号](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Emoticons)

表情符号一共有80个字符，范围为： U+1F600 ～ U+1F64F，在 Java 中正则表达式为：

```
"[\\uD83D\\uDE00-\\uD83D\\uDE4F]"
```

#### 4. [交通及地图符号](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Transport_and_Map_Symbols)

交通及地图符号一共有103个字符，范围为： U+1F680 ～ U+1F6FF，在 Java 中正则表达式为：

```
"[\\uD83D\\uDE80-\\uD83D\\uDEFF]"
```

#### 5. [杂项符号](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Miscellaneous_Symbols)

杂项符号一共有256个字符，范围为： U+2600 ～ U+26FF 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2600-\\u26FF]\\FE0F?"
```

#### 6. [装饰符号](https://zh.wikipedia.org/wiki/Template:Unicode_chart_Dingbats)

装饰符号一共有192个字符，范围为： U+2700 ～ U+27BF 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2700-\\u27BF]\\FE0F?"
```

#### 7. [封闭式字母数字符号](https://en.wikipedia.org/wiki/Enclosed_Alphanumerics)

封闭式字母数字符号中只有一个 emoji 字符，为： U+24C2 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"\\u24C2\\uFE0F?"
```

#### 8. [封闭式字母数字补充符号](https://en.wikipedia.org/wiki/Enclosed_Alphanumeric_Supplement)

封闭式字母数字补充符号包含41个 emoji 字符，其中26个属于区域指示符号

##### 8.1 [区域指示符号](https://en.wikipedia.org/wiki/Regional_Indicator_Symbol)

区域指示符号一共有26个字符，范围为： U+1F1E6 ～ U+1F1FF，并且其中每两个字母可以代表一个国家或地区的旗帜，在 Java 中正则表达式为：

```
"[\\uD83C\\uDDE6-\\uD83C\\uDDFF]{1,2}"
```

##### 8.2 其他封闭式字母数字补充 emoji 符号

除了区域指示符号外其他的 emoji 字符为： U+1F170、 U+1F171、 U+1F17E、 U+1F17F、 U+1F18E 和 U+1F191 ～ U+1F19A 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\uD83C\\uDD70\\uD83C\\uDD71\\uD83C\\uDD7E\\uD83C\\uDD7F\\uD83C\\uDD8E\\uD83C\\uDD91-\\uD83C\\uDD9A]\\uFE0F?"
```

#### 9. [键帽符号(#⃣, *️⃣ and 0⃣-9⃣)](https://en.wikipedia.org/wiki/Basic_Latin_%28Unicode_block%29)

键帽符号一共有12个字符，其组成方式为： U+0023、 U+002A 和 U+0030 ～ U+0039 12个键帽基础字符加上 U+FE0F 和 U+20E3， 如：

```
"\u0023\u20E3" > "#⃣"

"\u002A\uFE0F\u20E3" > "*️⃣"

"\u0030\u20E3" > "0⃣"

"\u0039\u20E3" > "9⃣"
```

其中 uFE0F 是可选的，所以在 Java 中正则表达式为：

```
"[\\u0023\\u002A[\\u0030-\\u0039]]\\uFE0F?\\u20E3"
```

#### 10. [箭头符号](https://en.wikipedia.org/wiki/Arrows_%28Unicode_block%29)

箭头符号中有8个 emoji 字符，范围为： U+2194 ～ U+2199 和 U+21A9 ～ U+21AA 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2194-\\u2199\\u21A9-\\u21AA]\\uFE0F?"
```

#### 11. [杂项符号及箭头](https://en.wikipedia.org/wiki/Miscellaneous_Symbols_and_Arrows)

杂项符号及箭头中有7个 emoji 字符，分别为： U+2B05 ～ U+2B07、 U+2B1B、 U+2B1C、 U+2B50 和 U+2B55 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2B05-\\u2B07\\u2B1B\\u2B1C\\u2B50\\u2B55]\\uFE0F?"
```

#### 12. [补充箭头符号](https://en.wikipedia.org/wiki/Supplemental_Arrows-B)

补充箭头符号中有2个 emoji 字符，分别为： U+2934 和 U+2935 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2934\\u2935]\\uFE0F?"
```

#### 13. [ CJK 符号和标点](https://en.wikipedia.org/wiki/CJK_Symbols_and_Punctuation)

CJK (Chinese, Japanese and Korean) 符号和标点中有两个 emoji 字符，分别为： U+3030 和 U+303D 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u3030\\u303D]\\uFE0F?"
```

#### 14. [封闭式 CJK 字母和月份符号](https://en.wikipedia.org/wiki/Enclosed_CJK_Letters_and_Months)

封闭式 CJK 字母和月份符号中有两个 emoji 字符，分别为：U+3297 和 U+3299 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u3297\\u3299]\\uFE0F?"
```

#### 15. [封闭式表意文字补充符号](https://en.wikipedia.org/wiki/Enclosed_Ideographic_Supplement)

封闭式表意文字补充符号中有15个 emoji 字符， 分别为： U+1F201、 U+1F202、 U+1F21A、 U+1F22F、 U+1F232 ～ U+1F23A、 U+1F250、 U+1F251 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\uD83C\\uDE01\\uD83C\\uDE02\\uD83C\\uDE1A\\uD83C\\uDE2F\\uD83C\\uDE32-\\uD83C\\uDE3A\\uD83C\\uDE50\\uD83C\\uDE51]\\uFE0F?"
```

#### 16. [一般标点](https://en.wikipedia.org/wiki/General_Punctuation)

一般标点符号中有2个 emoji 字符，分别为： U+203C 和 U+2049 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u203C\\u2049]\\uFE0F?"
```

#### 17. [几何图形](https://en.wikipedia.org/wiki/Geometric_Shapes)

几何图形中有8个 emoji 字符，分别为： U+25AA、 U+25AB、 U+25B6、 U+25C0 和 U+25FB ～ U+25FE 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u25AA\\u25AB\\u25B6\\u25C0\\u25FB-\\u25FE]\\uFE0F?"
```

#### 18. [拉丁文补充符号](https://en.wikipedia.org/wiki/Latin-1_Supplement_%28Unicode_block%29)

拉丁文补充符号中有2个 emoji 字符，分别为： U+00A9 和 U+00AE 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u00A9\\u00AE]\\uFE0F?"
```

#### 19. [字母符号](https://en.wikipedia.org/wiki/Letterlike_Symbols)

字母符号中有2个 emoji 字符，分别为： U+2122 和 U+2139 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u2122\\u2139]\\uFE0F?"
```

#### 20. [麻将牌](https://en.wikipedia.org/wiki/Mahjong_Tiles_%28Unicode_block%29)

麻将牌中只有一个 emoji 字符，为： U+1F004 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"\\uD83C\\uDC04\\uFE0F?"
```

#### 21. [扑克牌](https://en.wikipedia.org/wiki/Playing_cards_in_Unicode)

扑克牌中只有一个 emoji 字符，为： U+1F0CF 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"\\uD83C\\uDCCF\\uFE0F?"
```

#### 22. [杂项技术符号](https://en.wikipedia.org/wiki/Miscellaneous_Technical)

杂项技术符号中有18个 emoji 字符，分别为： U+231A、 U+231B、 U+2328、 U+23CF、 U+23E9 ～ U+23F3 和 U+23F8 ～ U+23FA 或拼上 U+FE0F，在 Java 中正则表达式为：

```
"[\\u231A\\u231B\\u2328\\u23CF\\u23E9-\\u23F3\\u23F8-\\u23FA]\\uFE0F?"
```

### 二、包含所有 emoji 的正则表达式

```
"(?:[\uD83C\uDF00-\uD83D\uDDFF]|[\uD83E\uDD00-\uD83E\uDDFF]|[\uD83D\uDE00-\uD83D\uDE4F]|[\uD83D\uDE80-\uD83D\uDEFF]|[\u2600-\u26FF]\uFE0F?|[\u2700-\u27BF]\uFE0F?|\u24C2\uFE0F?|[\uD83C\uDDE6-\uD83C\uDDFF]{1,2}|[\uD83C\uDD70\uD83C\uDD71\uD83C\uDD7E\uD83C\uDD7F\uD83C\uDD8E\uD83C\uDD91-\uD83C\uDD9A]\uFE0F?|[\u0023\u002A\u0030-\u0039]\uFE0F?\u20E3|[\u2194-\u2199\u21A9-\u21AA]\uFE0F?|[\u2B05-\u2B07\u2B1B\u2B1C\u2B50\u2B55]\uFE0F?|[\u2934\u2935]\uFE0F?|[\u3030\u303D]\uFE0F?|[\u3297\u3299]\uFE0F?|[\uD83C\uDE01\uD83C\uDE02\uD83C\uDE1A\uD83C\uDE2F\uD83C\uDE32-\uD83C\uDE3A\uD83C\uDE50\uD83C\uDE51]\uFE0F?|[\u203C\u2049]\uFE0F?|[\u25AA\u25AB\u25B6\u25C0\u25FB-\u25FE]\uFE0F?|[\u00A9\u00AE]\uFE0F?|[\u2122\u2139]\uFE0F?|\uD83C\uDC04\uFE0F?|\uD83C\uDCCF\uFE0F?|[\u231A\u231B\u2328\u23CF\u23E9-\u23F3\u23F8-\u23FA]\uFE0F?)"
```

### 参考文章
[1. 《Emojis in Javascript》 https://medium.com/@thekevinscott/emojis-in-javascript-f693d0eb79fb#.o29wt8xei](https://medium.com/@thekevinscott/emojis-in-javascript-f693d0eb79fb#.o29wt8xei)