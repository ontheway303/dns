# 查询PTR Record<a name="ZH-CN_TOPIC_0042318614"></a>

## 功能介绍<a name="section18389930"></a>

查询单个弹性IP的PTR记录。

## URI<a name="section31291646"></a>

GET /v2/reverse/floatingips/\{region\}:\{floatingip\_id\}

参数说明请参见[表1](#table21421675)。

**表 1**  URI格式的参数说明

<a name="table21421675"></a>
<table><thead align="left"><tr id="zh-cn_topic_0042318613_row3442661918149"><th class="cellrowborder" valign="top" width="22.64%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0042318613_p3709279118149"><a name="zh-cn_topic_0042318613_p3709279118149"></a><a name="zh-cn_topic_0042318613_p3709279118149"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="17.37%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0042318613_p5172606218149"><a name="zh-cn_topic_0042318613_p5172606218149"></a><a name="zh-cn_topic_0042318613_p5172606218149"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.349999999999998%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0042318613_p2906151418149"><a name="zh-cn_topic_0042318613_p2906151418149"></a><a name="zh-cn_topic_0042318613_p2906151418149"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.64%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0042318613_p517246718149"><a name="zh-cn_topic_0042318613_p517246718149"></a><a name="zh-cn_topic_0042318613_p517246718149"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0042318613_row1631668818149"><td class="cellrowborder" valign="top" width="22.64%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0042318613_p4658337018149"><a name="zh-cn_topic_0042318613_p4658337018149"></a><a name="zh-cn_topic_0042318613_p4658337018149"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="17.37%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0042318613_p1515661618149"><a name="zh-cn_topic_0042318613_p1515661618149"></a><a name="zh-cn_topic_0042318613_p1515661618149"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0042318613_p1972638718149"><a name="zh-cn_topic_0042318613_p1972638718149"></a><a name="zh-cn_topic_0042318613_p1972638718149"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="42.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0042318613_p5433349018149"><a name="zh-cn_topic_0042318613_p5433349018149"></a><a name="zh-cn_topic_0042318613_p5433349018149"></a>租户的区域信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0042318613_row1923936518149"><td class="cellrowborder" valign="top" width="22.64%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0042318613_p1488470218149"><a name="zh-cn_topic_0042318613_p1488470218149"></a><a name="zh-cn_topic_0042318613_p1488470218149"></a>floatingip_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.37%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0042318613_p6481017518149"><a name="zh-cn_topic_0042318613_p6481017518149"></a><a name="zh-cn_topic_0042318613_p6481017518149"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0042318613_p1513281718149"><a name="zh-cn_topic_0042318613_p1513281718149"></a><a name="zh-cn_topic_0042318613_p1513281718149"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="42.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0042318613_p1779865118149"><a name="zh-cn_topic_0042318613_p1779865118149"></a><a name="zh-cn_topic_0042318613_p1779865118149"></a>弹性IP的ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求<a name="section13189358"></a>

无

## 响应<a name="section51595365"></a>

-   参数说明

    **表 2**  响应样例的参数说明

    <a name="table28278595"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0042318613_row5725206118456"><th class="cellrowborder" valign="top" width="18.18%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0042318613_p690539418456"><a name="zh-cn_topic_0042318613_p690539418456"></a><a name="zh-cn_topic_0042318613_p690539418456"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.189999999999998%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0042318613_p2246606418456"><a name="zh-cn_topic_0042318613_p2246606418456"></a><a name="zh-cn_topic_0042318613_p2246606418456"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.629999999999995%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0042318613_p781187018456"><a name="zh-cn_topic_0042318613_p781187018456"></a><a name="zh-cn_topic_0042318613_p781187018456"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0042318613_row2878170018456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p4961636318456"><a name="zh-cn_topic_0042318613_p4961636318456"></a><a name="zh-cn_topic_0042318613_p4961636318456"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p5950245818456"><a name="zh-cn_topic_0042318613_p5950245818456"></a><a name="zh-cn_topic_0042318613_p5950245818456"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p5496981818456"><a name="zh-cn_topic_0042318613_p5496981818456"></a><a name="zh-cn_topic_0042318613_p5496981818456"></a>PTR记录的ID，格式形如{region}:{floatingip_id}。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row3274940018456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p3545576918456"><a name="zh-cn_topic_0042318613_p3545576918456"></a><a name="zh-cn_topic_0042318613_p3545576918456"></a>ptrdname</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p5334507918456"><a name="zh-cn_topic_0042318613_p5334507918456"></a><a name="zh-cn_topic_0042318613_p5334507918456"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p2598415318456"><a name="zh-cn_topic_0042318613_p2598415318456"></a><a name="zh-cn_topic_0042318613_p2598415318456"></a>PTR记录对应的域名。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row3253079218456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p1774845918456"><a name="zh-cn_topic_0042318613_p1774845918456"></a><a name="zh-cn_topic_0042318613_p1774845918456"></a>description</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p2833911218456"><a name="zh-cn_topic_0042318613_p2833911218456"></a><a name="zh-cn_topic_0042318613_p2833911218456"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p1376672518456"><a name="zh-cn_topic_0042318613_p1376672518456"></a><a name="zh-cn_topic_0042318613_p1376672518456"></a>对PTR记录的描述。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row5679166318456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p3672198418456"><a name="zh-cn_topic_0042318613_p3672198418456"></a><a name="zh-cn_topic_0042318613_p3672198418456"></a>ttl</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p2169069318456"><a name="zh-cn_topic_0042318613_p2169069318456"></a><a name="zh-cn_topic_0042318613_p2169069318456"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p1211568618456"><a name="zh-cn_topic_0042318613_p1211568618456"></a><a name="zh-cn_topic_0042318613_p1211568618456"></a>PTR记录的有效缓存时间，以秒为单位，默认值为300s。</p>
    <p id="zh-cn_topic_0042318613_p4184654118456"><a name="zh-cn_topic_0042318613_p4184654118456"></a><a name="zh-cn_topic_0042318613_p4184654118456"></a>取值范围：</p>
    <p id="zh-cn_topic_0042318613_p4107454918456"><a name="zh-cn_topic_0042318613_p4107454918456"></a><a name="zh-cn_topic_0042318613_p4107454918456"></a>300～2147483647。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row3412662318456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p1279309418456"><a name="zh-cn_topic_0042318613_p1279309418456"></a><a name="zh-cn_topic_0042318613_p1279309418456"></a>address</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p2960772218456"><a name="zh-cn_topic_0042318613_p2960772218456"></a><a name="zh-cn_topic_0042318613_p2960772218456"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p4941528218456"><a name="zh-cn_topic_0042318613_p4941528218456"></a><a name="zh-cn_topic_0042318613_p4941528218456"></a>弹性IP的IP地址。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row4208435918456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p5338995318456"><a name="zh-cn_topic_0042318613_p5338995318456"></a><a name="zh-cn_topic_0042318613_p5338995318456"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p2961896418456"><a name="zh-cn_topic_0042318613_p2961896418456"></a><a name="zh-cn_topic_0042318613_p2961896418456"></a>enum</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p5032586318456"><a name="zh-cn_topic_0042318613_p5032586318456"></a><a name="zh-cn_topic_0042318613_p5032586318456"></a>资源状态。</p>
    <p id="zh-cn_topic_0042318613_p55721846144628"><a name="zh-cn_topic_0042318613_p55721846144628"></a><a name="zh-cn_topic_0042318613_p55721846144628"></a>取值范围：PENDING_CREATE，ACTIVE，PENDING_DELETE，PENDING_UPDATE，ERROR 。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row4986307418456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p1237719818456"><a name="zh-cn_topic_0042318613_p1237719818456"></a><a name="zh-cn_topic_0042318613_p1237719818456"></a>action</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p6302897818456"><a name="zh-cn_topic_0042318613_p6302897818456"></a><a name="zh-cn_topic_0042318613_p6302897818456"></a>enum</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p507362318456"><a name="zh-cn_topic_0042318613_p507362318456"></a><a name="zh-cn_topic_0042318613_p507362318456"></a>对该资源的当前操作。</p>
    <p id="zh-cn_topic_0042318613_p9217462145017"><a name="zh-cn_topic_0042318613_p9217462145017"></a><a name="zh-cn_topic_0042318613_p9217462145017"></a>取值范围：CREATE，UPDATE，DELETE。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0042318613_row831034118456"><td class="cellrowborder" valign="top" width="18.18%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0042318613_p204899518456"><a name="zh-cn_topic_0042318613_p204899518456"></a><a name="zh-cn_topic_0042318613_p204899518456"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.189999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0042318613_p3175087318456"><a name="zh-cn_topic_0042318613_p3175087318456"></a><a name="zh-cn_topic_0042318613_p3175087318456"></a>object</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0042318613_p2168392018456"><a name="zh-cn_topic_0042318613_p2168392018456"></a><a name="zh-cn_topic_0042318613_p2168392018456"></a>指向当前资源或者其他相关资源的链接。</p>
    <p id="zh-cn_topic_0042318613_p6093755518456"><a name="zh-cn_topic_0042318613_p6093755518456"></a><a name="zh-cn_topic_0042318613_p6093755518456"></a>当响应需要分页时，需要包含一个next链接来进行分页。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    {
        "id": "region_id:c5504932-bf23-4171-b655-b87a6bc59334",
        "ptrdname": "www.example.com.",
        "description": "Description for this PTR record",
        "address": "10.154.52.138",
        "action": "CREATE",
        "ttl": 300,
        "status": "ACTIVE",
        "links": {
            "self": "https://Endpoint/v2/reverse/floatingips/region_id:c5504932-bf23-4171-b655-b87a6bc59334"
        }
    }
    ```


## 返回值<a name="section61705107"></a>

请参考[通用请求返回值](通用请求返回值.md)。

