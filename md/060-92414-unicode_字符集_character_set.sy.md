---
show: step
version: 1.0
enable_checker: true
---

# unicode

## 回忆上次内容

- 上次回顾了东亚地区文字编码的情况
- 中日韩各有各的编码格式
	- 日本有日本汉字
		- 字符数量超过20000+
	- 韩国有朝鲜汉字
		- 字符数量超过20000+
	- 中国的简体和繁体汉字
		- 字符数量都超级大
		- 彼此还认对方为乱码
- 如果有一种编码所有的字符都能编进去就好了
  - 中、日、韩、欧洲拉丁拼音等等等都包括
- 能有么？🤔

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20211004-1633338216226)

### 回顾历史

- 计算机中只有 `0` 和 `1`
  - 并且是存储在字节里的
  - 原来只能表示和处理数字
  - 字符无法处理
- 后来某些二进制数固定下来代表某个字符
  - 形成了字符集 
  - 从博多码(5bits)到 BCDIC(6bits)
  - 再到 EBCDIC码(8bits) 最后统一于 `ascii`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614479268989)

- 但是各国家和地区都有自己的字符
  - 这一领域没有统一的标准
  - 所以每个国家和地区指定自己的标准
  - 想要同时显示法语字符和希伯来字符是不可能的
  - 同样字节状态在不同编码格式里代表不同的字符
  - 都认为对方是乱码
  - 彼此不兼容
  - 编码方式有上百种之多

### 分久必合

- 无法解决的问题背后其实可能是机会
- Xerox(施乐公司) 在 1980 年代开始尝试一种编码能融合多语言
  - Xerox 字符集包括
	- 拉丁
	- 阿拉伯
	- 希伯来
	- 希腊
	- 西里尔
	- 中日韩字符

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221022-1666445734877)

- 这个字符集 1988 年进化为 unicode

### uni

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220515-1652607479811)

- uni 来自于
    - unique
    - unified
    - universal
    - unicorn
    - university
    - uniform

### 得一

- 这个词头计算机领域也有很多很牛的单词
    - unity、unit、unix
- 这名字得一了啊
    - 少则得,多则惑,是以圣人抱一为天下式
    - 天得一以清，地得一以宁，神得一以灵，谷得一以盈，万物得一以生，侯王得一而以为正
- 这个版本叫做 unicode88，是 16 位的 unicode
  - 1989 年 Unicode 这个工作组来了一些从大厂来的人，微软和 sun 都来了
  - 1991/1/3 日，Unicode 委员会在加州成立
  - 1991 年 8 月，unicode 第一卷发布
  - 1992 年 6 月，第 2 卷发布，这里面包含了汉语字符
  - Adobe, Apple, Facebook, Google, IBM, Microsoft, Netflix 和 SAP SE 加入 unicode 委员会

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614481940908)

- 字符的全球标准化开始了

### 基础字符

- ascii还是牢牢占据着0-127这最关键的位置
- 紧挨着 ascii 的字符位置非常重要
  - 这个字符集就是 Latin-1
  - 他是由 iso-8859-1 西欧字符集进化而来

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614486021235)

- 这其实也暗示出unicode的编码排序规则
- 以书写系统为单位来分类和收录

### 书写系统

- 英文字母、西里尔文字母来自希腊文字母
- 不同的书写系统可能会有重复的字母
- 但对应着不同的序号

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665541895851)

- 虽然字形一模一样
	- 但是属于三个书写系统
		- 希腊文字母
		- 英文字母
		- 西里尔字母

### 持续进化

- 每个版本都会有些变化
  - 整个编码区域分成若干个 blocks
  - 新版本对于这些 blocks 里面的字符有所增加

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614482179744)

- 除了字符之外还有很多符号
	- 比如十二个星座

### 十二星座

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220706-1657077784482)

- 集装箱标准化一旦开始
	- 就会反过来约束火车轮船飞机
- 你要想加入这个交流的行列
	- 必须要先从遵守现有的规则开始
- 新编码unicode的时代来了
	- 他会把一切字符吸收进去

### 阴阳太极

- 易有太极
	- ️☯

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614482724842)

- 是生两仪
	- ⚊ 陽 (U+268A) ⚋ 陰 (U+268B)
- 两仪生四象
	- ⚌(太陽,U+268C)、⚍(少陰,U+268D)、⚎(少陽,U+268E)、⚏(太陰,U+268F)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913117031)

### 八卦

- 四象生八卦
	- ☰ ☱ ☲ ☳ ☴ ☵ ☶ ☷

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651912743635)

- 如果把
	- ⚊ 陽 (U+268A)当做1
	- ⚋ 陰 (U+268B)当做0
- 顺序是逆序(递减)
- 从外而内
	- 天
	- 泽
	- 水
	- 雷
	- 风
	- 火
	- 山
	- 地

- 八卦有了
	- 可以重卦么？

### 重卦

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913261981)

- 八八六十四卦

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220211-1644564209397)

- 看起来都可以玩算卦了
- 还能做什么呢？

### 乱来

- 来随便试一个

```python
print("\u9999")
```

- 看看这是什么字？

### 中日韩字符

- 中文编码原来是 gbk

- unicode 现在unicode把中日韩(CJK)当成一组
	- 排序是CJK
	- 位置是unicode.org下方的code chart中找到

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220710-1657448172896)

- 当然关于排序各有各的排法
	- 中国是中日韩
	- 日本是日中韩
	- 韩国是韩中日
- unicode组织的CJK显然综合了东亚文化圈的排名
	- 我仿佛听到卡吉玛

### 所在位置

- 象形文字数量确实是拼音文字没有办法比的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220710-1657448246051)

- 他们听到我们有两万个字母的时候都傻了

### 融合而来

- unicode中的文字将
	- 中国汉字
	- 朝鲜汉字
	- 日本汉字
	- 综合起来

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665543002765)

- 得到一个汉字

### 分布

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614483685175)

- 分在几个 blocks 里面
	- 最常用的在0x4E00-0x9FBF 
		- F、B都是16进制的数字就像1、2、3一样
		- 这个范围就是中日韩字符的范围
	- 也属于 2个字节 以内
	- 字符数量也很多

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614483182116)

- 不过由于汉字数量太多
	- 原来给的空间不够用了

### 新分空间

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665543215735)

- 我们对比一下原来\x表示法和\u表示法

### 两种转义

- 原来`ascii`字符`a`可以用`\x61`表示
	- `\x61` 对应十六进制的(61)<sub>十六进制</sub>
	- 占用`一`个字节
	- 使用`\x`进行转义
- 现在`unicode`字符`一`可以用`\u4e00`表示
	- `\u4e00` 对应十六进制的(4e00)<sub>十六进制</sub>
	- 占用`两`个字节
	- 使用`\u`进行转义 

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220309-1646786138747)

- ascii 字符也能用 `\u` 的方式进行转义

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913393095)

- `\u`必须得4位16进制数
- 不过这样有点浪费空间和带宽
- 序号、字节状态和字符是什么关系呢？

### 关系

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913572123)

- 序号、字节状态和字符
- 这三个东西也构成一个闭环
- 就像ascii一样

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913674488)

- 我们现在再看一下ord和chr的帮助

### ord 和 chr

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665543495761)

- ord将字符的unicode编码转化为单字字符串

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665543504732)

- chr 将[0,0x10ffff] 转化为unicode 单字字符串
- 序号是unicode的序号
- 在[0,127]范围内
	- ascii和unicode重合
	- unicode可以兼容ascii
- 这些汉字可以按照什么方法归类吗？

### 韵母归类

- 合辙押韵

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666867214296)

- 可以用来找到押韵词汇

### 十三道大辙

- 这样就可以更方便找相同韵母的汉字了

|  大辙   | 对应十八韵  |
|  ----  | ----  |
| 一发花 | 十八韵的一麻 | 
| 二梭波 | 十八韵的二波三歌 | 
| 三乜斜 | 十八韵的四皆 | 
| 四衣欺 | 十八韵的五支、六儿、七齐 | 
| 五灰堆 | 十八韵的八微 | 
| 六怀来 | 十八韵的九开 | 
| 七姑苏 | 十八韵的十姑 | 
| 八衣欺 | 十八韵的十一鱼 | 
| 九由求 | 十八韵的十二侯 | 
| 十遥条 | 十八韵的十三豪 | 
| 十一言前 | 十八韵的十四寒 | 
| 十二人臣 | 十八韵的十五痕 | 
| 十三汪洋 | 十八韵的十六唐 | 
| 十四中东 | 十八韵的十七庚和十八东 | 

- 四、八其实可以合成一道大辙
- 如果要双押
	- 就得找词组韵母一致的
	- 其实都可以把所有的词归类
	- 然后制作一个押韵神器
- 词是有字组成的
- 词是如何编码进入计算机的呢？

### 编码解码

- 两个汉字的unicode编码
- 占用四个字节

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210815-1629011301094)

- 已知汉字，得到 unicode 值，叫做编码
  - 过程为 encode
- 已知 unicode 值，得到汉字，叫做解码
  - 过程为 decode



### encode decode

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630839461587)

- 把 str 字符串 encode 编码 为 bytes 字节序列
- 把 bytes 字节序列 decode 解码 为 str 字符串
- 编码和解码是互为逆运算的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630839936445)

- 绕了一圈又回来了
- 😁

### ascii eval

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210905-1630839978314)

- ascii 得到字符串的编码状态
- eval 得到编码的字符串状态
- 这两个也是逆运算
- eval应该如何理解呢？

### eval

- help(eval)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220212-1644676104797)

- eval
	- 意思是evaluate衡量
	- 是一个内置的函数
	- 在`__builtins__`这个module里面
	- 根据全局变量和局部变量的值进行衡量
	- 这里衡量的是
		- 按unicode形式的编码好的字符串

### 洳淉嬡，埥堔嬡。

- 在火星文转化器中
	- 团长，我从此就是杀马特的人了，爱你呦
		- 團萇，莪苁泚僦湜摋骉特哋亾孒，嬡沵呦。
	- 爱我不是你的错
		- 嬡莪芣湜沵哋措
		- ༺༒妳ィ是俄棏翄艕ོ
	- today is my birthday
		- 特嘚[表情]孓麥波斯嘚  

- 其实火星文就是把常用汉字序号
	- 和不常用的汉字的序号
	- 对应了起来
	- 文字转化就是找到序号的映射

### 中文字符集进化

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614483101545)

- 但是如果 2 个字节总共 16 位
	- 16 位最多 65536 各字符
	- 想要把全世界的字符都编码是不现实的
- 如果使用 3 字节编码就大大增加了存储和带宽的压力
	- 那到底应该怎么办呢？
- 到底应该按照 1 字节、2 字节还是 3 字节进行读取呢？

## 总结

- 字符集从博多码到 `ascii`、`8859`各自割据
- 如何把世界上各种字符统进行编码
  - `unicode`顺势而生不断进化
  - 不过字符总量超过了`65536`
  - `2`个字节放不下

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913535341)

- 改如何理解这个"\x62\xdc"呢?🤔
	- 究竟是"拜"
	- 还是"bÜ"呢？


![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221022-1666446876981)

- 我们下次再说！👋

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651928336667)

