# Тестовое задание для Школы Node.js

Демо доступно по адресу https://deadrime.github.io/yandex-form

Для запуска локально и без доступа к интернету необходимо либо запустить локальный сервер:

```
node server.js
```

Либо запустить хром с параметрами:

```
chrome.exe --allow-file-access-from-files --disable-web-security
```
Это нужно, так как иначе XMLHttp ругается на "Cross origin requests are only supported for HTTP" при запуске без локального сервера.  

Тип ответа от сервера(success.json, progress.json, error.json) можно поменять в раскрывающемся списке ```<select id="responceType">```.  

Немного о регулярных выражениях:  

![Reg](https://i.stack.imgur.com/MC2wS.png)  

В задании не было подробно указано, по каким стандартам и правилам валидировать email или учитывать ли В'ячеславов и Д'артаньянов при валидации ФИО, поэтому я не стал все усложнять и писать слишком сложные регулярки. Мне кажется что input type="email" для валидации почты вполне достаточно, а самый лучший способ проверить email - отправить туда письмо. Для телефона я использовал [маску](https://github.com/firstopinion/formatter.js), поэтому проверял номер только на количество цифр и сумму.
