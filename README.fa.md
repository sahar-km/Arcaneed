# تونل ED

<p align="left">
  <br><img src="https://github.com/NiREvil/Emotional-Damage/assets/126243832/66c9bdfb-9e74-4a91-a7d3-9a180450c690" width="320px">
</p>

[🇮🇷فارسی](README.fa.md)

[🇬🇧انگلیسی](README.md)

###### با تشکر فراوان از 3KmFi6HP

[![Repository](https://img.shields.io/badge/View%20on-GitHub-blue.svg)](https://github.com/3Kmfi6HP/EDtunnel)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

## فهرست مطالب

-   [استقرار در pages.dev](#Deploy-in-pages.dev)
-   [استقرار در worker.dev](#Deploy-in-worker.dev)
-   [uuid تنظیمات](#UUID-Setting)
    -   [مثال تنظیم uuid](#UUID-Setting-Example)
-   [اشتراک vless لینک](#Subscribe-vless-link)
-   [دامنه cf یا IP](#CF_Domain_or_IP's)
-   [پشتیبانی از چند پورت](#Multiple-port-support)
-   [پروکسی IP](#ProxyIP)
-   [استفاده](#Usage)![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

## استقرار در pages.dev

1.  ویدیوی یوتیوب را ببینید:

    [youtube.com/watch](https://www.youtube.com/watch?v=8I-yTNHB0aw)

2.  این استقرار مخزن را در صفحات cloudflare کلون کنید.

## استقرار در worker.dev

1.  کپی کنید`_worker.js`کد از[اینجا](_worker.js).

2.  همچنین، می‌توانید روی دکمه زیر کلیک کنید تا مستقیماً مستقر شود.

    [![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/NiREvil/Emotional-Damage)

## تنظیمات UUID

1.  هنگام استقرار در صفحات cloudflare، می توانید uuid را در آن تنظیم کنید`wrangler.toml`فایل نام متغیر است`uuid`.`wrangler.toml`فایل نیز پشتیبانی می شود. (توصیه می شود) در صورت استقرار در صفحات وب، نمی توانید uuid را در آن تنظیم کنید`wrangler.toml`فایل

2.  هنگام استقرار در worker.dev، می توانید uuid را در آن تنظیم کنید**خط یازدهم**از`_worker.js`فایل نام متغیر است`userID`.`wrangler.toml`فایل نیز پشتیبانی می شود. (توصیه می شود) در صورت استقرار در صفحات وب، نمی توانید uuid را در آن تنظیم کنید`wrangler.toml`فایل در این مورد، می توانید uuid را نیز تنظیم کنید`uuid`متغیر محیطی

توجه:`UUID`uuid است که می خواهید تنظیم کنید. روش pages.dev و worker.dev همه آنها پشتیبانی می شود، اما به روش استقرار شما بستگی دارد.

### مثال تنظیم UUID

1.  متغیر محیطی تک uuid

    ```.environment
    uuid = "uuid here your want to set"
    ```

2.  چند متغیر محیطی uuid

    ```.environment
    uuid = "uuid1,uuid2,uuid3"
    ```

    توجه: uuid1، uuid2، uuid3 با کاما از هم جدا می شوند`,`.
    وقتی چند uuid را تنظیم می کنید، می توانید استفاده کنید`https://edtunnel.pages.dev/uuid1`برای دریافت پیوند clash config و vless://.

## اشتراک vless لینک

-   بازدید کنید`https://edtunnel.pages.dev/uuid your set`برای دریافت لینک های اشتراک کلی v2ray، Singbox و کلش.

    -   بازدید کنید`https://edtunnel.pages.dev/uuid your set/pty`برای دریافت پیوند اشتراک جهانی کل.

    -   بازدید کنید`https://edtunnel.pages.dev/uuid your set/psb`برای دریافت لینک اشتراک Hiddify/Singbox

    -   بازدید کنید`https://edtunnel.pages.dev/uuid your set/pcl`برای دریافت لینک اشتراک Clash-Meta.


-   انجام شد. اگر سوالی دارید لطفا بپیوندید[@edtunnel](https://t.me/edtunnel)یا[@F_NiREvil](https://t.me/F_NiREvil)

## دامنه یا IP CF

می توانید دامنه سفارشی CF-pages/workers را برای گره vless+ws+tls در خط پانزدهم تغییر دهید.`_worker.js`فایل، پیش فرض است`www.speedtest.net`و همچنین می توانید تمام IP یا دامنه های CF تمیز را با خطوط دلخواه خود جایگزین کنید`17 ~ 31`.

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

## پشتیبانی از چند پورت

برای لیستی از پورت های پشتیبانی شده از Cloudflare، لطفاً به ادامه مطلب مراجعه کنید[اسناد رسمی](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/ports).

به طور پیش فرض، پورت 8080 و 8443 است. اگر می خواهید پورت ها را تغییر دهید، می توانید از پورت های زیر استفاده کنید:

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

> [توجه داشته باشید!]اگر در صفحات cloudflare مستقر می شوید، پورت https پشتیبانی نمی شود. به سادگی چندین پورت گره را اضافه کنید و از لینک اشتراک استفاده کنید،
> محتوای اشتراک همه پورت های پشتیبانی شده از Cloudflare را برمی گرداند.

## پروکسی IP

1.  هنگام استقرار در صفحات cloudflare، می توانید پروکسی IP را در آن تنظیم کنید`wrangler.toml`فایل یا تنظیم کنید`_worker.js`فایل در**خط 13**.  یا من توصیه کردم متغیر محیطی را با نام تنظیم کنید`proxyip`در حساب صفحه/cloudflare شما.

2.  هنگام استقرار در worker.dev، می توانید پروکسی IP را در آن تنظیم کنید`_worker.js`فایل نام متغیر است`proxyIP`.
    می توانید پروکسی آی پی را در اینجا پیدا کنید:<https://github.com/NiREvil/vless/blob/main/sub/ProxyIP.md>

> [!احتیاط]`proxyIP`آی پی یا دامنه ای است که می خواهید تنظیم کنید. این بدان معنی است که پروکسی IP برای هدایت ترافیک از طریق یک پروکسی به جای مستقیم به وب سایتی که از Cloudflare (CDN) استفاده می کند، استفاده می شود. اگر این متغیر را تنظیم نکنید، اتصال به IP Cloudflare لغو (یا مسدود می شود)...
>
> دلایل: سوکت های خروجی TCP به محدوده IP Cloudflare به طور موقت مسدود هستند، لطفاً به[اسناد tcp-sockets](https://developers.cloudflare.com/workers/runtime-apis/tcp-sockets/#considerations)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)

### استفاده

اول، pages.dev/uuid خود را باز کنید مانند:`https://edtunnel.pages.dev/uuid your set`در مرورگر خود، برای دریافت لینک های فرعی vless/singbox و clash.

اعتبارات:[آن را استریل کنید](https://github.com/3Kmfi6HP/EDtunnel)&[zizifn](https://github.com/zizifn/edgetunnel)

![rainbow](https://github.com/NiREvil/vless/assets/126243832/1aca7f5d-6495-44b7-aced-072bae52f256)
