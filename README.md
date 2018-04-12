<a class="wiz_toc h1" href="#懒得看的点这里, 直接到示例">懒得看的点这里, 直接到示例</a>
<br>
<a class="wiz_toc h1" href="#任务管理">任务管理</a>
<br>
<a class="wiz_toc h2" href="#界面说明">界面说明</a>
<br>
<a class="wiz_toc h1" href="#新增任务">新增任务</a>
<br>
<a class="wiz_toc h2" href="#1.请求参数配置">1.请求参数配置</a>
<br>
<a class="wiz_toc h3" href="#配置名称">配置名称</a>
<br>
<a class="wiz_toc h3" href="#请求方式">请求方式</a>
<br>
<a class="wiz_toc h3" href="#入口url">入口url</a>
<br>
<a class="wiz_toc h3" href="#请求参数">请求参数</a>
<br>
<a class="wiz_toc h3" href="#代理ip">代理ip</a>
<br>
<a class="wiz_toc h3" href="#动态解析">动态解析</a>
<br>
<a class="wiz_toc h2" href="#2.选择器配置">2.选择器配置</a>
<br>
<a class="wiz_toc h3" href="#选择器界面">选择器界面</a>
<br>
<a class="wiz_toc h4" href="#主界面">主界面</a>
<br>
<a class="wiz_toc h4" href="#增、改">增、改</a>
<br>
<a class="wiz_toc h4" href="#查">查</a>
<br>
<a class="wiz_toc h4" href="#预览">预览</a>
<br>
<a class="wiz_toc h3" href="#字段选择器属性">字段选择器属性</a>
<br>
<a class="wiz_toc h4" href="#字段使用条件">字段使用条件</a>
<br>
<a class="wiz_toc h3" href="#元素集选择器的存在意义">元素集选择器的存在意义</a>
<br>
<a class="wiz_toc h3" href="#选择器树形图">选择器树形图</a>
<br>
<a class="wiz_toc h3" href="#下一步/保存选择器">下一步/保存选择器</a>
<br>
<a class="wiz_toc h1" href="#查看/下载数据">查看/下载数据</a>
<br>
<a class="wiz_toc h1" href="#读取配置">读取配置</a>
<br>
<a class="wiz_toc h1" href="#采集示例">采集示例</a>
<br>
<a class="wiz_toc h2" href="#" 多元素 "选择器=" " +=" " 翻页(1)"="">"多元素"选择器 + 翻页(1)</a>
<br>
<a class="wiz_toc h3" href="#请求配置">请求配置</a>
<br>
<a class="wiz_toc h3" href="#参数配置">参数配置</a>
<br>
<a class="wiz_toc h2" href="#元素集选择器+翻页(2)+详情">元素集选择器+翻页(2)+详情</a>
<br>
<a class="wiz_toc h3" href="#参数配置">参数配置</a>
<br>
<a class="wiz_toc h1" href="#可能存在的问题">可能存在的问题</a>
<br>
<a class="wiz_toc h1" href="#动态解析">动态解析</a>
<br>
<a class="wiz_toc h1" href="#网页页模板不同">网页页模板不同</a>
<br>
<a class="wiz_toc h1" href="#选择器无法选中">选择器无法选中</a>

# 懒得看的点这里, 直接到示例
<a href="#采集示例">采集示例</a>

# 任务管理
## 界面说明
**主界面:**
![](/server/static/images/90eb120e-33b8-48fb-a665-4048a77839b9.png)

该模块管理爬虫的运行状态, 可以暂停、停止和恢复爬虫的运行.

**详情界面:**
![](/server/static/images/7028c459-888e-40ae-b412-e268540d4150.png)

如图, 点击任务, 进入详情页, "爬虫统计"为scrapy爬虫框架的日志信息; "请求队列"为将要爬取的url; 上方有"暂停"、"恢复"和"停止"爬虫任务按钮.

主界面为管理爬虫任务状态的模块, 前后端实时同步, 前端实时接收爬虫任务日志, 后端实时响应爬虫任务状态的改变.
# 新增任务
![](/server/static/images/0815f886-5de3-412b-8d21-b20a642af05a.png)

配置request请求参数和入口url, 同为后续爬虫的请求参数.

## 1.请求参数配置
### 配置名称
任务ID的标识, 在数据查询时用来查找数据集合, 保存配置时用来选择请求参数和字段选择器, 唯一值, 不可重复, 不能为`config`字符串.

### 请求方式
本平台选常用的两种请求, post和get.

### 入口url
爬取页面的入口页面, 选择采集参数和后续页面会在该页面进行扩展

### 请求参数
请求参数分为三种:
**1.请求头header参数**
爬虫常用的header参数有

| Header | 解释 | 示例 |
| ---- | ---- | ---- |
| Accept | 指定客户端能够接收的内容类型 | Accept: text/plain, text/html |
| Accept-Charset | 浏览器可以接受的字符编码集。 | Accept-Charset: iso-8859-5 |
| Accept-Encoding | 指定浏览器可以支持的web服务器返回内容压缩编码类型。 | Accept-Encoding: compress, gzip |
| Accept-Language | 浏览器可接受的语言 | Accept-Language: en,zh |
| Accept-Ranges | 可以请求网页实体的一个或者多个子范围字段 | Accept-Ranges: bytes |
| Content-Length | 请求的内容长度 | Content-Length: 348 |
| Content-Type | 请求的与实体对应的MIME信息 | Content-Type: application/x-www-form-urlencoded |
| Date | 请求发送的日期和时间 | Date: Tue, 15 Nov 2010 08:12:31 GMT |
| Proxy-Authorization | 连接到代理的授权证书 | Proxy-Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ== |
| Referer | 先前网页的地址，当前请求网页紧随其后,即来路 | Referer: https://www.baidu.com/ |
| User-Agent | User-Agent的内容包含发出请求的用户信息 | User-Agent: Mozilla/5.0 (Linux; X11) |

**2.cookie参数**
有些网站需要验证cookie参数

**3.form-data参数**
选择post请求时, 提交的参数信息

![](/server/static/images/acfce330-9ea4-4ce6-92fc-569707e8076c.png)
如图为header参数

### 代理ip
针对防爬虫网站设计, 动态代理ip, 有效时间`2018-05-10 14:44:00`前

### 动态解析
越来越多的网站选用js渲染页面, 针对非模板页面加载网站

示例url: `http://shop.99114.com/47907188/ch6`

静态爬虫获取页面内容：
![](/server/static/images/15155175263081.png)

动态爬虫获取页面内容：
![](/server/static/images/2.png)

动态爬虫实际获取页面内容：
![](/server/static/images/3.png)

在动态爬虫获取页面的前端展现上, 已竭力实现实际获取内容, 但仍不可避免造成爬取内容和展现内容不符.

## 2.选择器配置
![](/server/static/images/3da3e10c-80de-4597-9823-88a07ddb78b3.png)

选择器配置界面分为两部分, 上方的**采集页面**和下方的**选择器页面**.
上方的采集页面为请求配置完成后点击"下一步"所呈现出的页面内容.
下方的选择器界面为选择将要采集的数据.

### 选择器界面
#### 主界面
![](/server/static/images/28e81b8d-a8bb-4fc1-85c9-f3839f14da4a.png)
提供字段选择器的层级显示、增、删、改、查、预览功能
#### 增、改
![](/server/static/images/1d258dd7-3462-465e-a6ee-eff449a794ee.png)
添加/修改字段选择器, 共有7中类型的字段选择器<a href="#字段选择器属性">字段选择器属性</a>
#### 查
![](/server/static/images/28546708-1d60-416a-a874-a9cea4f7dce3.jpg)
显示选择器选择在页面中选择的位置
#### 预览
![](/server/static/images/709f40e1-b083-4d60-98e9-877fdf53c7b2.png)
显示选择器匹配的数据


选择器用来选定采集数据的位置和内容, 该界面可以用鼠标点击配置将要采集的数据, 查看采集数据的位置, 预览采集数据的内容, 根据采集数据不同, 将字段选择器分为以下7类.
### 字段选择器属性

| 字段选择器 | 名称 | 多元素属性(multiple) | 可选子元素 | 该类型页面唯一 | 可查看选择器 | 可预览数据 | 是否采集 |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| SelectorDetail | 详情页选择器 | 否 | 是 | 是 | 是 | 是 | 否 |
| SelectorElement | 元素集选择器 | 是 | 是 | 否 | 否 | 否 | 否 |
| SelectorElementAttribute | 元素属性选择器 | 是 | 否 | 否 | 是 | 是 | 是 |
| SelectorHTML | html选择器 | 是 | 否 | 否 | 是 | 是 | 是 |
| SelectorImage | 图片选择器 | 是 | 否 | 否 | 是 | 是 | 是 |
| SelectorLink | 翻页选择器 | 否 | 否 | 是 | 是 | 是 | 否 |
| SelectorText | 文本选择器 | 是 | 否 | 否 | 是 | 是 | 是 |

#### 字段使用条件

> 1.避免同级别multiple、非multiple属性的选择器并存

所有采集的字段(SelectorElementAttribute、SelectorHTML、SelectorImage、SelectorText)有字段选中"多元素属性"时, 不可选择其他采集的字段, 会造成两个字段集合维度混乱("多元素属性"的字段多对一非列表属性字段), 后端维度无法对应的字段值统一处理为空字符串.

如果有"多元素属性", 该父类下所有采集的字段选择器尽量全都是"多元素属性"；
如果没有"多元素属性", 该父类下所有采集的字段选择器尽量都没有"多元素属性".
![](/server/static/images/47b3f912-b840-4062-bd6b-f0bfc14b43ab.png)
![](/server/static/images/1ae43476-59d4-40bd-a1ef-9705df3030a3.png)
如图：标题、内容为可采集字段, 他们的多元素属性必须一致.
![](/server/static/images/600acd3f-432d-4784-9f41-654aabe628df.png)
不一致时示例

> 2.翻页选择器只能在入口页面设置且唯一

SelectorLink(翻页选择器)在入口页面下只能存在一个.
SelectorLink是递归采集函数.
存在多个时导致系统效率降低, 稳健性下降.

> 3.元素集选择器下可采集的字段多元素属性以元素集选择器为准

SelectorElement(元素集选择器)的子类采集选择器(SelectorElementAttribute、SelectorHTML、SelectorImage、SelectorText)选择multiple(多元素属性)时, 会将子类数据集升维, 数据解析错误.

[详细解释见<a href="#元素集选择器的存在意义">元素集选择器的存在意义</a>]
![](/server/static/images/85d6f868-f03b-4c9e-b8c9-cd7ffc832029.png)
如图：元素集下所有的可采集字段(红圈中)的multiple(多元素属性)以元素集是否选择multiple(多元素属性)为准.

前端表单按照字段选择器名称生成模板, 暂时未判断父类属性; 后端元素SelectorElement(元素集选择器)的子类采集选择器采集时将不会判断multiple(多元素属性).统一按照父类SelectorElement(元素集选择器)是否选择multiple(多元素属性)判断.

> 4.详情页选择只能有一条链式选择器

前端采集页面在iframe标签内, 详情页选择后无法返回, 同级别选择器只能存在一个, 不同层次的选择器存在详情页选择器则他们必在同一条链式选择器上.
后端采集框架scrapy为异步回调, 选择器解析为链式回调, 同级别存在多个详情页选择器会导致数据混淆、丢失.
![](/server/static/images/c5173f94-9895-4709-81db-0df46599fdf5.png)
如图："详情", "联系"为两个详情选择器, 在同一条链式选择器上

### 元素集选择器的存在意义

采集到所需的数据由两个因素决定：html文本和选择器， 其中html文本为页面中内容所在的html块, 选择器为指定采集的字段内容.

在使用到元素集选择器的大多数情况下html块多为列表形式存在, 选择器有多个.

**不使用元素集选择器时**
多个选择器按照"多元素"属性选择采集的数据, 页面本身可能存在内容块数据缺失, 造成多个选择器选择的数据列无法一一对应, 造成数据混淆、错位

示例：
![](/server/static/images/6cfe84f9-a938-49e7-ae1a-e16e67d25bbf.png)![](/server/static/images/545c2037-3d39-4e72-bddf-a84b180cc693.png)
![](/server/static/images/7fbf683b-98d8-4c09-9315-acc601a07387.png)![](/server/static/images/d0ca6d60-b3db-4514-bfb2-0c88fc862ea6.png)

"多元素属性"选择器优先遍历css选择器

新建两个"多元素属性"选择器, 第一个采集"name"字段, 第二个采集"href"字段, 当页面本身存在数据缺失时, 会使"name"和"href"数据无法一一对应."name_2" => "href_3" 导致数据错位.

**使用元素集选择器时**
![](/server/static/images/a7aff1d4-ad56-430f-a6de-aace92b2f56d.png)![](/server/static/images/73d3b897-1656-4f2c-8e63-f75ec30e1d08.png)

元素集选择器优先遍历内容块, 然后遍历css选择器, 使得数据维度得到统一, 缺失值也不会影响结果值

元素集选择器优先遍历内容块, "多元素属性"的选择器会优先遍历选择器, 两个开始采集维度的不同, 会导致不同的结果.当采集字段中存在多个"多元素属性"的选择器且他们具有同一个父元素, 优先考虑将这些选择器置于元素集选择器中.

### 选择器树形图
![](/server/static/images/85d6f868-f03b-4c9e-b8c9-cd7ffc832029.png)
显示各个层级的选择器关系

### 下一步/保存选择器
![](/server/static/images/48ab3a69-30c6-4707-b302-de21c4584294.png)
开始或者保存任务

# 查看/下载数据
![](/server/static/images/85ff994f-659a-42e3-a253-40bb730c2a64.png)

查看数据和下载已采集数据的页面

# 读取配置
![](/server/static/images/4b396b3a-c14e-4412-b0ac-566c08ac6946.png)

开始或删除任务

# 采集示例
## "多元素"选择器 + 翻页(1)
`http://www.51sole.com/s.aspx?q=PVC通风管`
### 请求配置
![](/server/static/images/c5c446a4-e1a5-403b-a5fc-3395af38237d.png)
### 参数配置
1.填写字段名称`商品名称`(唯一), 如果重复, 选择器保存失败
2.选择 选择器类型
3."点击选择"按钮开启选择器
4-5.分别点击同一列表中同一采集内容(自动匹配通用选择器, 无法匹配时会提示; 如采集单个选择, 只用点击选择器一次即可)
6.点击确定按钮获取"css选择器"内容, 确定左侧"键盘事件"共绑定了一个按键, S键: 当前选择器, P键: 当前选择元素的父元素, C键: 当前选择元素的子元素
7.选择"多元素属性"
8.保存选择器
![](/server/static/images/00a1e6e7-b30c-4754-8c57-6c89b2963296.png)

同上, 采集`公司url`字段
![](/server/static/images/2da8e8e6-d454-4713-9631-975644a15c81.png)

点击下一页, 选择`翻页选择器`
![](/server/static/images/3d7d1bfc-b673-40c2-9943-b4e537fc22a1.png)

整体如下：
主页面选择器：
![](/server/static/images/5f5724f9-48dc-478b-93d2-b1fed42889d6.png)
选择器层级：
![](/server/static/images/c1284037-d84f-42c5-861f-d63c017fc7de.png)
点击`下一步` `开始任务` 启动任务, 然后再主界面进行任务管理或者`查看数据`里下载数据
![](/server/static/images/2137d59b-71b9-4f71-a5f8-8fb114eadfa6.png)

## 元素集选择器+翻页(2)+详情
`https://zhongshan.china.cn/search/fisnfv.shtml`
### 参数配置
1.选择`元素集选择器`
![](/server/static/images/e9ba8329-9af2-46d3-82fe-904585d95132.png)

2.配置`翻页选择器`(翻页选择器分两种, 点击选择和手动配置, 优先使用手动配置, 选择器有全局表单验证, 改起来太麻烦, 使用手动配置时, 随便填个值), 手动配置时, 翻页url中变动的参数 使用`%s`代替.
![](/server/static/images/795c3e35-7b8c-4e2d-9bd9-4fbf87f619e7.png)

3.进入`元素集选择器`内, 新建`产品名称`, `所在地`和`公司名称`选择器(在元素集选择器中, 默认以第一个元素集为模板, 其他范围内`点击选择`按钮无法生效)
**注意**：在元素集选择器中不要选择"多元素"属性, 元素集选择器中的子选择器, 维度以`元素集选择器`为准.
![](/server/static/images/e0d90b15-0d89-41a3-92bd-3b6b3d703f2a.jpg)

4.配置`详情选择器`, 选择将要进入的标签, 保存
![](/server/static/images/993f90b4-ee2c-4e02-9b1f-76549a343599.png)

5.进入`详情选择器`, 在页面中点击详情链接

6.进入详情页之后, 再配置一个`详情选择器`进入联系页
![](/server/static/images/45afe047-fb6d-47b7-83b8-43216c5f396e.png)

7.在联系页中, 选择`联系人` `电话` `地址`字段采集器
![](/server/static/images/2e7f279e-0f2f-4b7c-bc2d-172f7ba8f75c.png)

8.打开`选择器树形图`查看选择器层级
![](/server/static/images/2f1eb188-2045-4864-9d2d-94303f8f8092.png)

8.`下一步`开始任务, 注意请求间隔, 太快容易被封
![](/server/static/images/e0b5824e-fa27-4b11-ba8c-2c9195e213fa.png)

被封
![](/server/static/images/4.png)

9.查看/下载数据
![](/server/static/images/294b2416-6e38-41d4-8989-5cb80904ed49.png)


# 可能存在的问题
# 动态解析
动态解析网页太慢, 资源占用过高, 显示内容和爬取内容不同, 造成显示内容和爬取内容不同主要因为网站自带js的运行导致的, 如果取消爬取网站自带js, 可能会造成依赖css无法加载, 前端展示效果极差和网页布局和渲染效果缺失, 留待以后解决.

# 网页页模板不同
`http://kungeina0315.51sole.com/companycontact.htm`
`http://jing18028106510.51sole.com/companycontact.htm`

![](/server/static/images/72c2b627-6338-41a7-8670-661cc7bf5dda.png)![](/server/static/images/699f21fd-0cae-4078-8c43-1f0823038d87.png)

场景：两个详情页模板, 由于字段个数不同, 使用css选择器时, 对不同的模板选择字段, 会造成字段缺失或者错位的情况。 这两个页面中, 由于第二个页面多了"传真"和"微信"这两个字段, 导致相同的css选择器在匹配第一个页面的同时, 匹配第二个页面时"传真"字段之后的css选择器选择的字段值错位.

处理：使用css选择器选择整个内容块, 然后使用正则表达式提取采集的内容

![](/server/static/images/396e4817-df36-4f9d-81f0-90d63b2a41a3.png)

如图所示: 采集"手机"字段, 选择整个内容块, 然后使用正则表达式提取.

# 选择器无法选中
![](/server/static/images/1c0aeff2-0045-48f9-80d5-3b070b42e490.png)![](/server/static/images/bb25525b-648f-4a10-a271-e8ca7751e24c.png)
`点击选择`按钮很难选中元素时, 可以先选择他的父元素或子元素, 然后使用键盘按钮C或P调整.
`点击选择`没有反应, 本平台将采集网页放在本域名内, 跨域导致有些资源加载异常, 使得采集脚本无法加载, 此时只能手动填写css选择器.