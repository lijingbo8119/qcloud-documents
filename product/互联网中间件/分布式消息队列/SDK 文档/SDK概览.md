消息队列 TDMQ 现支持 TDMQ 腾讯云版 SDK 和 Pulsar 社区版 SDK。以下是消息队列 TDMQ 所支持的多语言 SDK：

>!
>- 为了更好地和 Pulsar 开源社区统一，自2021年4月30日起，腾讯云版 SDK 将停止功能更新，TDMQ 推荐您使用社区版本的 SDK。
>-  如果您已使用了腾讯云 SDK，并且确定未使用以下文中说明的 [额外功能](#external)，可以直接替换成社区版的 SDK。

<table>
<tr>
<th>协议类型</th><th>SDK 语言</th>
</tr>
<tr>
<td>TCP 协议（Pulsar 社区版）</td>
<td><li><a href="https://cloud.tencent.com/document/product/1179/48552">Java SDK</a></li><li><a href="http://pulsar.apache.org/docs/en/client-libraries-go/"> Go SDK</a></li><li><a href="http://pulsar.apache.org/docs/en/client-libraries-cpp/">C++ SDK</a></li><li><a href="http://pulsar.apache.org/docs/en/client-libraries-python/">Python SDK</a></li><li><a href="http://pulsar.apache.org/docs/en/client-libraries-node/">Node.js</a></li></td>
</tr>
<tr>
<td>TCP 协议（腾讯云版，仅限存量客户使用）</td>
<td><li><a href="https://cloud.tencent.com/document/product/1179/44832">Java SDK</a></li><li><a href="https://cloud.tencent.com/document/product/1179/44831">Go SDK</a></li></td>
</tr>
</table>


### 腾讯云版 SDK 额外支持的功能[](id:external)
| 功能               | 说明                                                         |
| ------------------ | ------------------------------------------------------------ |
| 标签过滤           | 可以为消息附上 Tag 属性，消息支持绑定多个标签，订阅者可按照标签筛选决定是否处理消息。这样可以利用标签优化业务架构，节省 Topic 资源消耗。 |
| 支持退避式延时消息 | 对于失败超时重试场景，并不需要在短时间内大量重试，因为很可能还是失败，依次扩大时间间隔进行重试是比较合理的。 |

