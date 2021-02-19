# Poc_Management_T1
## 未经作者同意不得非法售卖，该程序仅作为交流学术使用，不得非法攻击，自行使用产生问题与作者本人无关

#### #项目支持TXT多目标，多线程  
#### #支持添加管理Poc，自定义Poc 
#### #支持http请求GET、POST验证
#### #支持返回内容验证，支持正则，支持完整文本匹配
#### #临时指纹识别功能



<a name="Gj6kC"></a>
### 前言
自动化漏洞利用，所需要的就是一个极为高效的框架，不管什么语言所编写的框架基础逻辑都不会相差太多。借鉴很多前辈的项目比如 [pocsuite3](https://github.com/knownsec/pocsuite3)、[fire_vulnerability_scanner](https://github.com/coodyer/fire_vulnerability_scanner)、[POC-T](https://github.com/Xyntax/POC-T)等等，对比以上于是有了自己的框架管理[Poc_Management_T1](https://github.com/AnotherVol/Poc_Management_T1)。<br />目的为简化工作流程，方便快速验证某一种漏洞（如果批量验证各种漏洞不就成了漏扫）。在渗透测试过程中，减少扫描是最为有必要的。
<a name="85FfB"></a>
### 实现原理
根据日常渗透测试发现大量的重复工作，发现漏洞产生根本原因就是区访问了指定位置的指定参数，触发漏洞。<br />以 thinkphp5x任意代码执行漏洞(cnvd-2018-24942)为例下图为手动bp测试<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613699751457-f92a8174-0e90-4197-9660-6227cb1ccab9.png#align=left&display=inline&height=693&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1385&originWidth=2560&size=391087&status=done&style=none&width=1280)<br />以此原理只需要构造数据请求包，发送，验证返回内容即可。
<a name="PpfE6"></a>
#### 具体实现示意：
![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613701706617-a5ce03f1-8d98-45a9-ae37-ee4a988f6c98.png#align=left&display=inline&height=729&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1457&originWidth=2536&size=682056&status=done&style=none&width=1268)
<a name="9r9oy"></a>
#### 
<a name="kzYSz"></a>
### Demo展示
![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698180509-c6521023-cbc5-41e2-b849-4e8976961f42.png#align=left&display=inline&height=448&margin=%5Bobject%20Object%5D&name=image.png&originHeight=897&originWidth=1648&size=99732&status=done&style=none&width=824)<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698101790-e4d46401-a567-4961-8d4d-4182fce510a7.png#align=left&display=inline&height=448&margin=%5Bobject%20Object%5D&name=image.png&originHeight=897&originWidth=1648&size=79596&status=done&style=none&width=824)<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698267715-206ad942-5eba-4b63-9992-8b9a4cc41a8f.png#align=left&display=inline&height=543&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1085&originWidth=2002&size=208429&status=done&style=none&width=1001)<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698141469-aa1a8529-12b1-4817-8bab-e1f9f82cdce5.png#align=left&display=inline&height=470&margin=%5Bobject%20Object%5D&name=image.png&originHeight=939&originWidth=1829&size=126607&status=done&style=none&width=914.5)<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698365227-e2010269-7119-4c98-bfc4-6ded9a3bdf52.png#align=left&display=inline&height=448&margin=%5Bobject%20Object%5D&name=image.png&originHeight=897&originWidth=1648&size=164113&status=done&style=none&width=824)<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/1969118/1613698387881-b490b510-1799-4aef-bb73-ef5313e9b7ec.png#align=left&display=inline&height=448&margin=%5Bobject%20Object%5D&name=image.png&originHeight=897&originWidth=1648&size=77900&status=done&style=none&width=824)
