# EDtunnel

<p align="left">
  <br><img src="https://github.com/NiREvil/Emotional-Damage/assets/126243832/66c9bdfb-9e74-4a91-a7d3-9a180450c690" width="320px">
</p>

[🇮🇷Persian](README.fa.md)  


[🇬🇧English](README.md)


###### Many thanks to 3KmFi6HP
[![Repository](https://img.shields.io/badge/View%20on-GitHub-blue.svg)](https://github.com/3Kmfi6HP/EDtunnel)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)


## Table of Contents
- [deploy in pages.dev](#Deploy-in-pages.dev)
- [deploy in worker.dev](#Deploy-in-worker.dev)
- [uuid Setting](#UUID-Setting)
  - [uuid Setting Example](#UUID-Setting-Example)
- [subscribe vless link](#Subscribe-vless-link)
- [cf domain or IP's](#CF_Domain_or_IP's)
- [multiple port support](#Multiple-port-support)
- [proxyIP](#ProxyIP)
- [usage](#Usage)
![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

## Deploy in pages.dev

1. See YouTube Video:

   [youtube.com/watch](https://www.youtube.com/watch?v=8I-yTNHB0aw)

2. Clone this repository deploy in cloudflare pages.

## Deploy in worker.dev

1. Copy `_worker.js` code from [here](_worker.js).

2. Alternatively, you can click the button below to deploy directly.

   [![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/sahar-km/Arcaneed)


## UUID Setting

1. When deploy in cloudflare pages, you can set uuid in `wrangler.toml` file. variable name is `uuid`. `wrangler.toml` file is also supported. (recommended) in case deploy in webpages, you can not set uuid in `wrangler.toml` file.

2. When deploy in worker.dev, you can set uuid in the __11th line__ of `_worker.js` file. variable name is `userID`. `wrangler.toml` file is also supported. (recommended) in case deploy in webpages, you can not set uuid in `wrangler.toml` file. in this case, you can also set uuid in `uuid` enviroment variable.

Note: `UUID` is the uuid you want to set. pages.dev and worker.dev all of them method supported, but depend on your deploy method.


### UUID Setting Example

1. single uuid environment variable

   ```.environment
   uuid = "uuid here your want to set"
   ```

2. multiple uuid environment variable

   ```.environment
   uuid = "uuid1,uuid2,uuid3"
   ```

   note: uuid1, uuid2, uuid3 are separated by commas`,`.
   when you set multiple uuid, you can use `https://edtunnel.pages.dev/uuid1` to get the clash config and vless:// link.


## Subscribe vless link

- visit `https://edtunnel.pages.dev/uuid your set` to get Aggregate general v2ray, Singbox and Clash Subscription links.

  - Visit `https://edtunnel.pages.dev/uuid your set/pty` to get the aggregate universal subscription link.

  - Visit `https://edtunnel.pages.dev/uuid your set/psb` to get Hiddify/Singbox subscription link

  - Visit `https://edtunnel.pages.dev/uuid your set/pcl` to get the Clash-Meta subscription link.



- done. if have any questions please join [@edtunnel](https://t.me/edtunnel)
OR
 [@F_NiREvil](https://t.me/F_NiREvil)



## CF Domain or IP's

You can change the single CF-pages/workers custom domain for vless+ws+tls node in the 15th line of `_worker.js` file, default is `www.speedtest.net`
and also you can replaced all CF clean IP or domains with your preferred from lines `17 ~ 31`.

```POV-Ray SDL
let CDNIP = 'www.speedtest.net'
```

```CSS
// http_ip
let IP1 = 'www.visa.com'
let IP2 = 'cis.visa.com'
let IP3 = 'africa.visa.com'
let IP4 = 'www.visa.com.sg'
let IP5 = 'sky.rethinkdns.com'
let IP6 = 'go.inmobi.com'
let IP7 = 'icook.hk'

// https_ip
let IP8 = 'usa.visa.com'
let IP9 = 'www.speedtest.net'
let IP10 = 'creativecommons.org'
let IP11 = 'sky.rethinkdns.com'
let IP12 = 'zula.ir'
let IP13 = 'www.wto.org'
```


## Multiple port support

For a list of Cloudflare supported ports, please refer to the [official documentation](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/ports).

By default, the port is 8080 and 8443. If you want to modifying ports, you can use the following ports:


```CSS
let portArray_http = [
// line 33
let PT1 = '80'
let PT2 = '8080'
let PT3 = '8880'
let PT4 = '2052'
let PT5 = '2082'
let PT6 = '2086'
let PT7 = '2095
];

let portArray_https = [
// line 42 
let PT8 = '443'
let PT9 = '8443'
let PT10 = '2053'
let PT11 = '2083'
let PT12 = '2087'
let PT13 = '2096'
];
```

> [!NOTE]
> if you deploy in cloudflare pages, https port is not supported. Simply add multiple ports node drictly use subscribe link,
> subscribe content will return all Cloudflare supported ports.



## ProxyIP

1. When deploy in cloudflare pages, you can set proxyIP in `wrangler.toml` file or set in `_worker.js` file in the __line 13__.  Or i recommended to set in environment variable with name `proxyip` in your page/cloudflare account.

2. When deploy in worker.dev, you can set proxyIP in `_worker.js` file. variable name is `proxyIP`.
you can find proxyIP Here: https://github.com/NiREvil/vless/blob/main/sub/ProxyIP.md


> [!CAUTION]
>  `proxyIP` is the ip or domain you want to set. this means that the proxyIP is used to route traffic through a proxy rather than directly to a website that is using Cloudflare's (CDN). if you don't set this variable, connection to the Cloudflare IP will be cancelled (or blocked)...
>
> resons: Outbound TCP sockets to Cloudflare IP ranges are temporarily blocked, please refer to the [tcp-sockets documentation](https://developers.cloudflare.com/workers/runtime-apis/tcp-sockets/#considerations)


![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)


### Usage

frist, open your pages.dev/uuid like: `https://edtunnel.pages.dev/uuid your set` in your browser, to get the vless/singbox and clash sublinks.

Credits: [3Kmfi6HP](https://github.com/3Kmfi6HP/EDtunnel)  &  [zizifn](https://github.com/zizifn/edgetunnel)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)
