# 内网DNS并发有什么限制？<a name="dns_faq_033"></a>

为了营造一个良性安全的内网解析环境，保证每个租户虚拟机内网DNS的解析效率，内网DNS服务器会限制来自单个IP地址的解析流量，QPS最高为2000。如果某个服务器请求DNS解析的频率特别高，超出了阈值，内网DNS将丢弃针对此IP超出阈值的流量。

如果您的业务确实会产生超高的并发解析请求，建议您开启DNS缓存功能，以提升解析效率。

