# Headers of HTTP

#### Рассмотреть и проанализировать заголовки я решил на примере сайта `github.com`.

Вот такой запрос на сервер отправил мой браузер(Request):

```yaml
:authority: github.com
:method: GET
:path: /
:scheme: https
accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
accept-encoding: gzip, deflate, br
accept-language: ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7
cache-control: max-age=0
cookie: _octo=GH1.1.561396701.1623894977; _device_id=1b762288eee5f70b15ba84549fe69950; user_session=d1-G0u_RAIUj3EKCBZWWBTfYS_smpTvNS5RnlN1phOHYFhE6; __Host-user_session_same_site=d1-G0u_RAIUj3EKCBZWWBTfYS_smpTvNS5RnlN1phOHYFhE6; logged_in=yes; dotcom_user=elisey20; has_recent_activity=1; color_mode=%7B%22color_mode%22%3A%22dark%22%2C%22light_theme%22%3A%7B%22name%22%3A%22light%22%2C%22color_mode%22%3A%22light%22%7D%2C%22dark_theme%22%3A%7B%22name%22%3A%22dark%22%2C%22color_mode%22%3A%22dark%22%7D%7D; tz=Asia%2FVladivostok; _gh_sess=SlvMKi3PSlnHJQn%2BneVkqMJlZIXlZdebpwlsSnv2Kp3HRfgGR9iLoUFqoV%2Bza%2BY%2FiBi7HJaFGVPvjqdVpha0oUipaTdLh4U%2FwXcbqgWrWC%2FLoSb%2BcG%2F%2BM4D3UM%2B3yu8OohVgr4UR46jGmFQr1GVSKC1PbcqidXreWu45idT%2FaeHTV%2Bf2Byl4wbvutqGuNnzN5nSdSLzBP1zsmIxVx2M%2B2Ht4824gOJnpdjbVo1P2R4eG%2BPTs%2FmtVEpnrvIZYYLFYhPWVau2tTZHOjFPQznXTq6k%2FV8o0j1C774ss3EamLEQ8DetF%2F5pDAjYA5AQadn4szMDad4%2F2X8PMi5oh87ZY0WL%2Bq5Z0eta174Vf3TfLnE1SclgMcPDPkSu8XBqP%2BN%2F2yULxKJpKDHS40vCMTe7G1v8G5m2dlCFQHj%2F8i%2BFsSVyfCYgJiKl7jkAt4ho%2BJcW33G%2Bg2j7QfRCfAph3YCX9zFZvq6Jathu%2BKyEqObd%2F2vT6LGZoZb36vlRzeoKAatJhgAmKbUUCI2khIvW%2FAmBFK7OT5P%2FcOpPRXcAWOg%3D%3D--6HJWjmXRwxIWkH2Y--8d3myKSVdz3y2BCp0q2Kbw%3D%3D
if-none-match: W/"7e792e88ac3354a443d887060c885d56"
referer: https://github.com/elisey20/OPZ_in_OOP
sec-ch-ua: "Chromium";v="94", "Google Chrome";v="94", ";Not A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
sec-fetch-dest: document
sec-fetch-mode: navigate
sec-fetch-site: same-origin
sec-fetch-user: ?1
upgrade-insecure-requests: 1
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.81 Safari/537.36
```

Рассмотрим некоторые поля запроса:

- `Accept` - указывает, какие типы контента, выраженные как MIME типы, клиент может понять;
- `Accept-Encoding` - определяет кодирование содержания(сжатие);
- `Accept-Language` - используется для указания языка;
- `cookie` - очевидно куки;
- `user-agent` - идентифицирует бразуер.

Ответ, который прислал нам сервер(Response):
 
```yaml
cache-control: max-age=0, private, must-revalidate
content-encoding: gzip
content-security-policy: default-src 'none'; base-uri 'self'; block-all-mixed-content; child-src github.com/assets-cdn/worker/ gist.github.com/assets-cdn/worker/; connect-src 'self' uploads.github.com objects-origin.githubusercontent.com www.githubstatus.com collector.githubapp.com api.github.com github-cloud.s3.amazonaws.com github-production-repository-file-5c1aeb.s3.amazonaws.com github-production-upload-manifest-file-7fdce7.s3.amazonaws.com github-production-user-asset-6210df.s3.amazonaws.com cdn.optimizely.com logx.optimizely.com/v1/events translator.github.com wss://alive.github.com github.githubassets.com; font-src github.githubassets.com; form-action 'self' github.com gist.github.com objects-origin.githubusercontent.com; frame-ancestors 'none'; frame-src render.githubusercontent.com viewscreen.githubusercontent.com viewscreen-lab.githubusercontent.com; img-src 'self' data: github.githubassets.com identicons.github.com collector.githubapp.com github-cloud.s3.amazonaws.com secured-user-images.githubusercontent.com/ *.githubusercontent.com customer-stories-feed.github.com spotlights-feed.github.com; manifest-src 'self'; media-src github.com user-images.githubusercontent.com/ github.githubassets.com; script-src github.githubassets.com; style-src 'unsafe-inline' github.githubassets.com; worker-src github.com/assets-cdn/worker/ gist.github.com/assets-cdn/worker/
content-type: text/html; charset=utf-8
date: Wed, 13 Oct 2021 00:01:20 GMT
etag: W/"284141146295fe27a93eb73876b8a786"
expect-ct: max-age=2592000, report-uri="https://api.github.com/_private/browser/errors"
permissions-policy: interest-cohort=()
referrer-policy: origin-when-cross-origin, strict-origin-when-cross-origin
server: GitHub.com
set-cookie: has_recent_activity=1; path=/; expires=Wed, 13 Oct 2021 01:01:20 GMT; secure; HttpOnly; SameSite=Lax
set-cookie: _gh_sess=5NNjAMJpytMbgeXHPn3GKNu6GCFInQkaNKn70DFVehWJJMhdT3nZD0BtBYjyIlXYRGN7XpRznV2bbLJpK6Z4bD7NPhVw7IwJb086t8rZMuVXFvTdc5mGIBqGAFUn5GRe%2BI43PgGtVbQfI6S95ovCarRfOooSe6AZmxqzWs91Z9UdFBh4%2F9nJKQDs3tJ8LFPft%2BRmoQ7hbJpKOhVfEEDrDPyeRPon6dY%2BtXfFy6TI%2Fw5KCFT9X2k3kkptqbA%2BGjn9MJXQxmqtO83qBWgO7znes4cHG6q%2BkpZV6F79nbnT1yp38SXNf0GrjIUGTR1i5wTgW%2B5lddLlPRTVUtevKzucev9d3ZDcq5l3AFTEMPdRC67Io3B%2B6tu6ibMgg%2Blo11PlnTKguqZIKU3IDi%2F1sOAB3lxnuOhlefaGna4o%2Bat5youW49jSA2PUFHe0C%2FQ5VxYsZu9KgX1Y93jTwX48xjGQs6yJSFcteTTO%2FoxeeW7rHu%2BfbyvIWEO85DN7F4PhQVLk2OhJY0sOEd6rmxY%2BEyuNfjGVbzh0FGq1jXd0mg%3D%3D--Lyoh1GXLrnNlUyXl--bJDIyyv4y6%2Fq9isCnqbeZg%3D%3D; path=/; secure; HttpOnly; SameSite=Lax
strict-transport-security: max-age=31536000; includeSubdomains; preload
vary: X-PJAX, X-PJAX-Container
vary: Accept-Encoding, Accept, X-Requested-With
x-content-type-options: nosniff
x-frame-options: deny
x-github-request-id: E45C:E986:1BEC6AF:1D07623:616621C4
x-xss-protection: 0
```

Разберём несколько полей полученного ответа:

- `cache-control` - для задания инструкций кеширования;
- `content-type` - используется для того, чтобы определить MIME тип ресурса;
- `expect-ct` - запрашивает у браузера проверку наличия сертификата для этого сайта. Браузеры игнорируют заголовок над HTTP, заголовок влияет только на HTTPS-соединения;
- `vary` - определяет, как сопоставить будущие заголовки запроса, чтобы решить, можно ли использовать кешированный ответ, а не запрашивать новый с исходного сервера;
- `x-content-type-options` - является маркером, используемым сервером для указания того, что типы MIME, объявленные в заголовках Content-Type, должны соблюдаться и не изменяться/.

#### Анализ 10-ти самых интересных(по моему мнению) полей запроса и ответа `github.com` считаю оконченным.
