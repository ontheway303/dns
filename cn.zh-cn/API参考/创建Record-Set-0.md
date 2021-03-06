# 创建Record Set<a name="ZH-CN_TOPIC_0082840627"></a>

## 功能介绍<a name="section2763065016101"></a>

创建单个Record Set。

>![](public_sys-resources/icon-note.gif) **说明：**   
>仅公网域名支持创建多线路Record Set，该接口仅适用于公网DNS。  

## URI<a name="section53701671161015"></a>

POST /v2.1/zones/\{zone\_id\}/recordsets

参数说明请参见[表1](#table30807893173129)。

**表 1**  URI格式的参数说明

<a name="table30807893173129"></a>
<table><thead align="left"><tr id="row38661368173129"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p14212988173129"><a name="p14212988173129"></a><a name="p14212988173129"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="21.3%" id="mcps1.2.4.1.2"><p id="p23287688173129"><a name="p23287688173129"></a><a name="p23287688173129"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.46%" id="mcps1.2.4.1.3"><p id="p1114682173129"><a name="p1114682173129"></a><a name="p1114682173129"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row6301875173129"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="p5124116173129"><a name="p5124116173129"></a><a name="p5124116173129"></a>zone_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.3%" headers="mcps1.2.4.1.2 "><p id="p65804667173129"><a name="p65804667173129"></a><a name="p65804667173129"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="56.46%" headers="mcps1.2.4.1.3 "><p id="p13017963195717"><a name="p13017963195717"></a><a name="p13017963195717"></a>所属zone的ID。仅支持公网zone。</p>
</td>
</tr>
</tbody>
</table>

## 请求<a name="section44958995161021"></a>

-   参数说明

    **表 2**  请求样例的参数说明

    <a name="table9470531173211"></a>
    <table><thead align="left"><tr id="row60397351173211"><th class="cellrowborder" valign="top" width="22.45%" id="mcps1.2.5.1.1"><p id="p65819295173211"><a name="p65819295173211"></a><a name="p65819295173211"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.29%" id="mcps1.2.5.1.2"><p id="p42278174173211"><a name="p42278174173211"></a><a name="p42278174173211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.89%" id="mcps1.2.5.1.3"><p id="p26309572173211"><a name="p26309572173211"></a><a name="p26309572173211"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="38.37%" id="mcps1.2.5.1.4"><p id="p67071922173211"><a name="p67071922173211"></a><a name="p67071922173211"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row65160710173211"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p21415905173211"><a name="p21415905173211"></a><a name="p21415905173211"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p58188388173211"><a name="p58188388173211"></a><a name="p58188388173211"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p45293229173211"><a name="p45293229173211"></a><a name="p45293229173211"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p5054941173211"><a name="p5054941173211"></a><a name="p5054941173211"></a>后缀需以zone name结束且为FQDN（即以“.”号结束的完整主机名）。</p>
    <p id="p4141499817341"><a name="p4141499817341"></a><a name="p4141499817341"></a>当为公网域名时，子域名级别最多为5级。</p>
    <p id="p27471407151355"><a name="p27471407151355"></a><a name="p27471407151355"></a>域名格式不区分大小写，系统会将输入的大写字母统一转换为小写。</p>
    </td>
    </tr>
    <tr id="row34337486173211"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p33154613173211"><a name="p33154613173211"></a><a name="p33154613173211"></a>description</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p28540882173211"><a name="p28540882173211"></a><a name="p28540882173211"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p37402311173211"><a name="p37402311173211"></a><a name="p37402311173211"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p43441715173211"><a name="p43441715173211"></a><a name="p43441715173211"></a>可选配置，对域名的描述。</p>
    <p id="p9966775173211"><a name="p9966775173211"></a><a name="p9966775173211"></a>长度不超过255个字符。</p>
    </td>
    </tr>
    <tr id="row52503862173211"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p4265712173211"><a name="p4265712173211"></a><a name="p4265712173211"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p43588224173211"><a name="p43588224173211"></a><a name="p43588224173211"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p44233480173211"><a name="p44233480173211"></a><a name="p44233480173211"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p29114279173211"><a name="p29114279173211"></a><a name="p29114279173211"></a>Record Set的类型。</p>
    <p id="p1579233173211"><a name="p1579233173211"></a><a name="p1579233173211"></a>取值范围：A,AAAA,MX,CNAME,TXT, NS（仅限公网Zone）,SRV,CAA（仅限公网Zone）。</p>
    </td>
    </tr>
    <tr id="row44235645173211"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p56753577173211"><a name="p56753577173211"></a><a name="p56753577173211"></a>ttl</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p44923213173211"><a name="p44923213173211"></a><a name="p44923213173211"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p3678318721261"><a name="p3678318721261"></a><a name="p3678318721261"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p41610046141952"><a name="p41610046141952"></a><a name="p41610046141952"></a>Record Set的有效缓存时间，以秒为单位。默认值为300s。</p>
    <p id="p20437753173211"><a name="p20437753173211"></a><a name="p20437753173211"></a>取值范围：300~2147483647</p>
    </td>
    </tr>
    <tr id="row59750658173211"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p62596825173211"><a name="p62596825173211"></a><a name="p62596825173211"></a>records</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p32296167173211"><a name="p32296167173211"></a><a name="p32296167173211"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p5792332173211"><a name="p5792332173211"></a><a name="p5792332173211"></a>List&lt;string&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p8321575173211"><a name="p8321575173211"></a><a name="p8321575173211"></a>不同Type对应的Value值规则不同。</p>
    <p id="p813988173211"><a name="p813988173211"></a><a name="p813988173211"></a>如Type为AAAA类型，Value是域名对应的IPv6地址列表。</p>
    <p id="p59053902173211"><a name="p59053902173211"></a><a name="p59053902173211"></a>具体参见《云解析服务用户指南》中“管理记录集”章节的说明及请求样例。</p>
    </td>
    </tr>
    <tr id="row19347487142432"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p19620443142437"><a name="p19620443142437"></a><a name="p19620443142437"></a>line</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p43599524142447"><a name="p43599524142447"></a><a name="p43599524142447"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p30969417142432"><a name="p30969417142432"></a><a name="p30969417142432"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p25494838142432"><a name="p25494838142432"></a><a name="p25494838142432"></a>解析线路，默认为默认线路。请参见<a href="解析线路类型.md">解析线路类型</a>。</p>
    </td>
    </tr>
    <tr id="row3778990815215"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.5.1.1 "><p id="p3329183915215"><a name="p3329183915215"></a><a name="p3329183915215"></a>weight</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.29%" headers="mcps1.2.5.1.2 "><p id="p1228445215215"><a name="p1228445215215"></a><a name="p1228445215215"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.89%" headers="mcps1.2.5.1.3 "><p id="p5551654115215"><a name="p5551654115215"></a><a name="p5551654115215"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.37%" headers="mcps1.2.5.1.4 "><p id="p54597115215"><a name="p54597115215"></a><a name="p54597115215"></a>解析记录的权重，默认为1。</p>
    <a name="ul2108239317221"></a><a name="ul2108239317221"></a><ul id="ul2108239317221"><li>当不填时，默认为1。</li></ul>
    <a name="ul1341791710223"></a><a name="ul1341791710223"></a><ul id="ul1341791710223"><li>当weight=0，表示备用域名解析记录。</li><li>当weight&gt;0，表示主用域名解析记录。</li></ul>
    <p id="p11866386153334"><a name="p11866386153334"></a><a name="p11866386153334"></a>取值范围：0~100</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  tag对象参数说明

    <a name="table9752964195025"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0057310891_row15361836112436"><th class="cellrowborder" valign="top" width="15.21%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057310891_p58707511112436"><a name="zh-cn_topic_0057310891_p58707511112436"></a><a name="zh-cn_topic_0057310891_p58707511112436"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.58%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057310891_p57687928112436"><a name="zh-cn_topic_0057310891_p57687928112436"></a><a name="zh-cn_topic_0057310891_p57687928112436"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.27%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057310891_p42210623112436"><a name="zh-cn_topic_0057310891_p42210623112436"></a><a name="zh-cn_topic_0057310891_p42210623112436"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057310891_p63617265112436"><a name="zh-cn_topic_0057310891_p63617265112436"></a><a name="zh-cn_topic_0057310891_p63617265112436"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0057310891_row35684479112436"><td class="cellrowborder" valign="top" width="15.21%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057310891_p13313439112530"><a name="zh-cn_topic_0057310891_p13313439112530"></a><a name="zh-cn_topic_0057310891_p13313439112530"></a>key</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.58%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057310891_p50150432112436"><a name="zh-cn_topic_0057310891_p50150432112436"></a><a name="zh-cn_topic_0057310891_p50150432112436"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.27%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057310891_p35653193112436"><a name="zh-cn_topic_0057310891_p35653193112436"></a><a name="zh-cn_topic_0057310891_p35653193112436"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057310891_p48921437201850"><a name="zh-cn_topic_0057310891_p48921437201850"></a><a name="zh-cn_topic_0057310891_p48921437201850"></a>键。最大长度36个unicode字符。 key不能为空。不能包含“=”,“*”,“&lt;”,“&gt;”,“\”,“,”,“|”,“/”，且首尾字符不能为空格。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0057310891_row20048002112436"><td class="cellrowborder" valign="top" width="15.21%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057310891_p66095544112533"><a name="zh-cn_topic_0057310891_p66095544112533"></a><a name="zh-cn_topic_0057310891_p66095544112533"></a>value</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.58%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057310891_p1570770112436"><a name="zh-cn_topic_0057310891_p1570770112436"></a><a name="zh-cn_topic_0057310891_p1570770112436"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.27%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057310891_p60123528112436"><a name="zh-cn_topic_0057310891_p60123528112436"></a><a name="zh-cn_topic_0057310891_p60123528112436"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057310891_p61714725112922"><a name="zh-cn_topic_0057310891_p61714725112922"></a><a name="zh-cn_topic_0057310891_p61714725112922"></a>值。每个值最大长度43个unicode字符，可以为空字符串。 不能包含“=”,“*”,“&lt;”,“&gt;”,“\”,“,”,“|”,“/”，且首尾字符不能为空格。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例
    -   A类型

        ```
        {
            "name": "www.example.com.",
            "description": "This is an example record set.",
            "type": "A",
            "ttl": 3600,
            "records": [
                "192.168.10.1",
                "192.168.10.2"
            ],
            "line":"default_view",
            "weight":1
        }
        ```

    -   AAAA类型

        ```
        {
            "name": "www.example.com.",
            "description": "This is an example record set.",
            "type": "AAAA",
            "ttl": 3600,
            "records": [
                "fe80:0:0:0:202:b3ff:fe1e:8329",
                "ff03:0db8:85a3:0:0:8a2e:0370:7334"
            ],
            "line":"default_view",
            "weight":1
        }
        ```

    -   MX类型

        ```
        {
            "name": "www.example.com.",
            "description": "This is an example record set.",
            "type": "MX",
            "ttl": 3600,
            "records": [
                "1 mail.example.com"
            ],
            "line":"default_view",
            "weight":1
        }
        ```

    -   CNAME类型

        ```
        {
            "name": "sale.example.com.",
            "description": "This is an example record set.",
            "type": "CNAME",
            "ttl": 3600,
            "records": [
                "server1.example.com"
            ],
            "line":"default_view",
            "weight":1
        }
        ```

    -   TXT类型

        ```
        {
            "name": "server1.example.com.",
            "description": "This is an example record set.",
            "type": "TXT",
            "ttl": 300,
            "records": [
                "\"This host is used for sale.\""
            ],
            "line":"default_view",
            "weight":1
        }
        ```

    -   NS类型

        ```
        {
            "name": "server1.example.com.",
            "description": "This is an example record set.",
            "type": "NS",
            "ttl": 300,
            "records": [
                "node1.example.com.",
                "node2.example.com."
            ],
            "line":"default_view",
            "weight": 1
        }
        ```

    -   SRV类型

        ```
        {
            "name": "_sip._tcp.example.com.",
            "description": "This is an example record set.",
            "type": "SRV",
            "ttl": 300,
            "records": [
                "3 60 2176 sipserver.example.com.",
                "10 100 2176 sipserver.example.com."
            ],
            "line":"default_view",
            "weight":1
        
        }
        
        ```

    -   CAA类型

        ```
        {
            "name": "www.example.com.",
            "description": "This is an example record set.",
            "type": "CAA",
            "ttl": 300,
            "records": [
                "0 issue \"example.com\"",
                "0 issuewild \"www.certinomis.com\"",
                "0 iodef \"mailto:xx@example.org\"",
                "0 iodef \"http://iodef.example.com\""
            ],
            "line":"default_view",
            "weight":1
        }
        ```



## 响应<a name="section40090803161031"></a>

-   参数说明

    **表 4**  响应样例的参数说明

    <a name="table7669703175323"></a>
    <table><thead align="left"><tr id="row52466955175323"><th class="cellrowborder" valign="top" width="27.889999999999997%" id="mcps1.2.4.1.1"><p id="p2769858175323"><a name="p2769858175323"></a><a name="p2769858175323"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.810000000000002%" id="mcps1.2.4.1.2"><p id="p46296309175323"><a name="p46296309175323"></a><a name="p46296309175323"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.3%" id="mcps1.2.4.1.3"><p id="p62697904175323"><a name="p62697904175323"></a><a name="p62697904175323"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row47909891175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p64112397175323"><a name="p64112397175323"></a><a name="p64112397175323"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p1660870175323"><a name="p1660870175323"></a><a name="p1660870175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p1249204175323"><a name="p1249204175323"></a><a name="p1249204175323"></a>Record Set的ID。</p>
    </td>
    </tr>
    <tr id="row6942422175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p64097412175323"><a name="p64097412175323"></a><a name="p64097412175323"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p44990515175323"><a name="p44990515175323"></a><a name="p44990515175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p32019574175323"><a name="p32019574175323"></a><a name="p32019574175323"></a>Record Set的名称。</p>
    </td>
    </tr>
    <tr id="row61442071175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p51194416175323"><a name="p51194416175323"></a><a name="p51194416175323"></a>description</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p63301991175323"><a name="p63301991175323"></a><a name="p63301991175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p43966660175323"><a name="p43966660175323"></a><a name="p43966660175323"></a>Record Set的描述信息。</p>
    </td>
    </tr>
    <tr id="row2176746175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p11805366175323"><a name="p11805366175323"></a><a name="p11805366175323"></a>zone_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p1051908175323"><a name="p1051908175323"></a><a name="p1051908175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p10043845175323"><a name="p10043845175323"></a><a name="p10043845175323"></a>托管该记录的zone_id。</p>
    </td>
    </tr>
    <tr id="row61212722175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p8318586175323"><a name="p8318586175323"></a><a name="p8318586175323"></a>zone_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p31287919175323"><a name="p31287919175323"></a><a name="p31287919175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p16372315175323"><a name="p16372315175323"></a><a name="p16372315175323"></a>托管该记录的zone_name。</p>
    </td>
    </tr>
    <tr id="row38132372175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p37461920175323"><a name="p37461920175323"></a><a name="p37461920175323"></a>type</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p27536075175323"><a name="p27536075175323"></a><a name="p27536075175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p24813356175323"><a name="p24813356175323"></a><a name="p24813356175323"></a>记录类型。</p>
    <p id="p52445812175323"><a name="p52445812175323"></a><a name="p52445812175323"></a>取值范围：A，AAAA，MX，CNAME，TXT，NS（仅限公网Zone），SRV，CAA（仅限公网Zone）。</p>
    </td>
    </tr>
    <tr id="row20796819175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p4811553175323"><a name="p4811553175323"></a><a name="p4811553175323"></a>ttl</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p47559731175323"><a name="p47559731175323"></a><a name="p47559731175323"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p22097398175323"><a name="p22097398175323"></a><a name="p22097398175323"></a>域名的缓存时间，单位为秒，缓存时间越长更新生效越慢。</p>
    </td>
    </tr>
    <tr id="row13978060175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p43388342175323"><a name="p43388342175323"></a><a name="p43388342175323"></a>records</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p29596719175323"><a name="p29596719175323"></a><a name="p29596719175323"></a>List&lt;string&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p30492925175323"><a name="p30492925175323"></a><a name="p30492925175323"></a>域名解析后的值。</p>
    </td>
    </tr>
    <tr id="row23148559175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p36524189175323"><a name="p36524189175323"></a><a name="p36524189175323"></a>created_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p47080972175323"><a name="p47080972175323"></a><a name="p47080972175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p15737135175323"><a name="p15737135175323"></a><a name="p15737135175323"></a>创建时间。</p>
    </td>
    </tr>
    <tr id="row33465792175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p42570937175323"><a name="p42570937175323"></a><a name="p42570937175323"></a>updated_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p27449776175323"><a name="p27449776175323"></a><a name="p27449776175323"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p63703533175323"><a name="p63703533175323"></a><a name="p63703533175323"></a>更新时间。</p>
    </td>
    </tr>
    <tr id="row17850883175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p36228271175323"><a name="p36228271175323"></a><a name="p36228271175323"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p6480061175323"><a name="p6480061175323"></a><a name="p6480061175323"></a>enum</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p65781854175323"><a name="p65781854175323"></a><a name="p65781854175323"></a>资源状态。</p>
    <p id="p51374523175323"><a name="p51374523175323"></a><a name="p51374523175323"></a>取值范围：PENDING_CREATE，ACTIVE，PENDING_DELETE，PENDING_UPDATE，ERROR，FREEZE，DISABLE。</p>
    </td>
    </tr>
    <tr id="row61184424175323"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p49633411175323"><a name="p49633411175323"></a><a name="p49633411175323"></a>default</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p56048766175323"><a name="p56048766175323"></a><a name="p56048766175323"></a>boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p37768157175323"><a name="p37768157175323"></a><a name="p37768157175323"></a>标识是否由系统默认生成，系统默认生成的Record Set不能删除与修改。</p>
    </td>
    </tr>
    <tr id="row15199048201026"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p23163408201026"><a name="p23163408201026"></a><a name="p23163408201026"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p40653752201026"><a name="p40653752201026"></a><a name="p40653752201026"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p4619625201026"><a name="p4619625201026"></a><a name="p4619625201026"></a>该Record Set所属的租户ID。</p>
    </td>
    </tr>
    <tr id="row3965248419366"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p2132803819366"><a name="p2132803819366"></a><a name="p2132803819366"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p1127763319366"><a name="p1127763319366"></a><a name="p1127763319366"></a>object</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p4107308719366"><a name="p4107308719366"></a><a name="p4107308719366"></a>指向当前资源或者其他资源的链接。当查询需要分页时，需要包含一个next链接指向下一页。</p>
    </td>
    </tr>
    <tr id="row15869402143342"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p13813035143342"><a name="p13813035143342"></a><a name="p13813035143342"></a>line</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p45114021143342"><a name="p45114021143342"></a><a name="p45114021143342"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p30357067143342"><a name="p30357067143342"></a><a name="p30357067143342"></a>解析线路。</p>
    </td>
    </tr>
    <tr id="row5250267143345"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p46748947143345"><a name="p46748947143345"></a><a name="p46748947143345"></a>weight</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p28568349143345"><a name="p28568349143345"></a><a name="p28568349143345"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p32334952143345"><a name="p32334952143345"></a><a name="p32334952143345"></a>解析记录的权重。</p>
    </td>
    </tr>
    <tr id="row2642850715221"><td class="cellrowborder" valign="top" width="27.889999999999997%" headers="mcps1.2.4.1.1 "><p id="p6033434615221"><a name="p6033434615221"></a><a name="p6033434615221"></a>health_check_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.810000000000002%" headers="mcps1.2.4.1.2 "><p id="p5524385315221"><a name="p5524385315221"></a><a name="p5524385315221"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.3%" headers="mcps1.2.4.1.3 "><p id="p4556711715221"><a name="p4556711715221"></a><a name="p4556711715221"></a>健康检查ID。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "id": "2c9eb155587228570158722b6ac30007",
        "name": "www.example.com.",
        "description": "This is an example record set.",
        "type": "A",
        "ttl": 300,
        "records": [
            "192.168.10.1",
            "192.168.10.2"
        ],
        "status": "PENDING_CREATE",
        "links": {
            "self": "https://Endpoint/v2.1/zones/2c9eb155587194ec01587224c9f90149/recordsets/2c9eb155587228570158722b6ac30007"
        },
        "zone_id": "2c9eb155587194ec01587224c9f90149",
        "zone_name": "example.com.",
        "created_at": "2016-11-17T12:03:17.827",
        "updated_at": null,
        "default": false,
        "project_id": "e55c6f3dc4e34c9f86353b664ae0e70c",
        "line": "default_view",
        "weight": 1,
        "health_check_id":null
    }
    
    ```


## 返回值<a name="section42637797161043"></a>

请参考[通用请求返回值](通用请求返回值.md)。

