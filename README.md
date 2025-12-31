# Bright Data データセンタープロキシ

[![Promo](https://github.com/luminati-io/Datacenter-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.jp/proxy-types/datacenter-proxies?promo=github15)

## Overview
比類ない規模と速度を備えた Bright Data の広範な [データセンタープロキシネットワーク](https://brightdata.jp/proxy-types/datacenter-proxies) を活用し、信頼性の高いデータ収集と Webスクレイピング を実現します。

- **770,000+ データセンターIP**
- **[共有](https://brightdata.jp/solutions/shared-proxies)および[専用](https://brightdata.jp/solutions/dedicated-proxies)IPオプション**
- **平均レスポンスタイム 約0.24秒**
- **HTTP(S) & [SOCKS5](https://brightdata.jp/solutions/socks5-proxies) 対応**
- **国レベルのターゲティングが無料**

## Key Features
- **グローバルリーチ**: [98か国](https://brightdata.jp/locations) にわたるデータセンターIPへアクセスできます。
- **高い成功率**: スクレイピングタスクで最大 99.9% の成功率を実現します。
- **高速かつ信頼性が高い**: ネットワーク稼働率 99.99% と高速な接続速度を提供します。
- **カスタマイズ可能なオプション**: ニーズに応じて共有IPまたは専用IPを選択できます。
- **無制限のスケーリング**: 制限なく同時接続セッションをサポートします。

## Pricing Plans
- **Pay As You Go**: 月次コミット不要で $0.6/GB。
- **月額サブスクリプション - 共有**:
  - **10 IPs**: $1.40/IP、$14/月 + VAT。
  - **100 IPs**: $1.00/IP、$100/月 + VAT。
  - **500 IPs**: $0.95/IP、$475/月 + VAT。
  - **1,000 IPs**: $0.90/IP、$900/月 + VAT。
  - **Enterprise Plans**: 大規模なデータ収集向けに最適化されたソリューションです。

- **月額サブスクリプション - 専用**:
  - **10 IPs**: $2.20/IP、$22/月 + VAT。
  - **100 IPs**: $1.70/IP、$170/月 + VAT。
  - **500 IPs**: $1.50/IP、$750/月 + VAT。
  - **1,000 IPs**: $1.30/IP、$1300/月 + VAT。
  - **Enterprise Plans**: 大規模なデータ収集向けに最適化されたソリューションです。


- **月額サブスクリプション - Pay/GB**:
  - $0.51/GB、$499/月 + VAT。
  - $0.45/GB、$999/月 + VAT。
  - $0.42/GB、$1999/月 + VAT。
  - **Enterprise Plans**: 大規模なデータ収集向けに最適化されたソリューションです。

登録して、初回入金額に対してドル建てで同額のマッチを受けられます（最大 $500 まで）！

## Getting Started with Datacenter Proxies
1. **無料トライアルを開始**: クレジットカードは不要です。
2. **統合**: API または Bright Data Control Panel で IP と設定を管理します。
3. **対応言語**: Python、Java、C#、Node.js、Shell のクイックスタートガイドをご利用いただけます。

## Code Examples

### Python

```python
import sys

# Replace '[your customerID]', 'datacenter', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-datacenter", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-datacenter", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-datacenter:"[your password]"@brd.superproxy.io:22225',
    })
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-residential:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## Integrations
当社のデータセンタープロキシは、以下を含む一般的な自動化ツールと互換性があります。

- [**Puppeteer**](https://brightdata.jp/integration/puppeteer)
- [**Selenium**](https://brightdata.jp/integration/selenium)
- [**Playwright**](https://brightdata.jp/integration/playwright)
- [**AdsPower**](https://brightdata.jp/integration/adspower)
- [**MultiLogin**](https://brightdata.jp/integration/multilogin)

## Use Cases
データセンタープロキシの一般的な用途:

- [**eCommerce**](https://brightdata.jp/use-cases/ecommerce): 価格と商品の在庫状況を追跡します。
- [**Social Media**](https://brightdata.jp/use-cases/social-media-for-marketing): トレンドとエンゲージメントをモニタリングします。
- [**Real Estate**](https://brightdata.jp/use-cases/real-estate): 物件リスティングに関するデータを収集します。
- [**Travel**](https://brightdata.jp/use-cases/travel): 地域ごとに旅行プランの取引条件を比較します。

## FAQ

### Datacenter Proxy とは何ですか？
データセンタープロキシはサーバーに割り当てられた IP を提供し、Webスクレイピング やその他の用途で IPアドレス とロケーションを変更できるようにします。

### Datacenter Proxies の利点は何ですか？
データセンタープロキシは高速でコスト効率が高く、シンプルなデータ収集タスク、アカウント管理、基本的なジオ制限の回避に最適です。

### 企業は Datacenter Proxies をどのように利用していますか？
競合分析からデジタル資産の保護まで、データセンタープロキシはさまざまな業界における幅広いタスクを支援します。

### Bright Data の Datacenter Proxies はどこに配置されていますか？
当社のプロキシは世界 98 のロケーションにまたがっており、[USA](https://brightdata.jp/locations/united-states)、[Canada](https://brightdata.jp/locations/ca)、[UK](https://brightdata.jp/locations/gb)、[Germany](https://brightdata.jp/locations/de)、[France](https://brightdata.jp/locations/fr) では特に多数の IP を提供しています。

### Datacenter Proxies は高速ですか？
はい。ルーティングが最小限であるため、データセンタープロキシは高速な接続を提供し、時間にシビアな用途に最適です。

### 共有と専用の Datacenter Proxies はどちらを使用すべきですか？
専用アクセスが必要な場合は専用プロキシを、一般的なスクレイピングやテストタスクに対してコスト効率を重視する場合は共有プロキシをご利用ください。