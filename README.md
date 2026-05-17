![U.SC.A](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/banner_logo_new.png)
# <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/icon_logo.png" width="5%" height="5%"> Unofficial Stalcraft API
Документация внутреннего HTTP/HTTPS API лаунчера и игры.

[Расследование, изучение и объяснение работы внутреннего сетевого трафика игры](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/INVESTIGATION.md)

### Условные обозначения
<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> - GET-Запрос

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="35" height="35"> - POST-Запрос

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/steam_logo.png" width="35" height="35"> - Вызываются только на STEAM* клиенте

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> - Вызываются только на EXBO* лаунчере

*Если значок отсутствует - обе платформы используют эти запросы

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="35" height="35"> - Неофициальное "Зеркало" EAPI игры

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> EXBO Launcher/Steam (RU) <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/steam_logo.png" width="50" height="50">

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/metrics](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetmetrics) - Отправка метрики

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/test](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnettest) - Проверка соединения перед авторизацией

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/launcher?list=true](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetlauncherlisttrue) - Информация для технических файлов лаунчера

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/auth](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetauth) - Авторизация в лаунчере

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/distributor](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetdistributor) - Авторизация в лаунчере через Steam

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/listServers](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetlistservers) - Информация об игре: Онлайн, HTTP сиды, IP-адрес сервера и т.д.

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://tracker1.stalcraft.net | http://tracker2.stalcraft.net](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httptracker1stalcraftnet-----httptracker2stalcraftnet) - Torrent-трекеры (для раздачи файлов игры через протокол TORRENT)

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://m-cdn.exbo.net | http://exbo.b-cdn.net](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpm-cdnexbonet--httpexbob-cdnnet) - CDN-сервера (для скачивания файлов игры через CDN запросы)

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://dev-cdn.xexbo.ru](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#--httpdev-cdnxexboru) - CDN-сервер ОТС и ЗТС файлов игры

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/joinGame](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnetjoingame) - Запрос для входа в игру

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [http://launcher.stalcraft.net/torrentData](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httplauncherstalcraftnettorrentdata) - Ссылка подкачки stalcraft.torrent.bin (TORRENT-подобного файла для скачивания файлов игры)

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="35" height="35"> [https://backend.stalcraftx.ru/session/game](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpsbackendstalcraftxrusessiongame) - Запрос идентификатора текущей сессии игры (для back-end запросов) 

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://backend.stalcraftx.ru/address_list](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpsbackendstalcraftxruaddress_list) - Список IP-адресов игровых серверов

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://backend.stalcraftx.ru/characters/list](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpsbackendstalcraftxrucharacterslist) - Запрос для получения технической информации по поводу персонажей на текущем аккаунте/

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="35" height="35"> [https://backend.stalcraftx.ru/characters/create](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpsbackendstalcraftxrucharacterscreate) - Создание нового персонажа на аккаунте

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://stalcraft.net/webhook/region](https://github.com/Art3mLapa/unofficial-stalcraft-api?tab=readme-ov-file#-httpsstalcraftnetwebhookregion) - Запрос для получения IP пользователя для Discord-вебхука

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://a0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1.selstorage.ru/service.json](https://github.com/Art3mLapa/unofficial-stalcraft-api#--httpsa0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1selstorageruservicejson) - Эндпоинт для получения актуальной ссылки для скачивания драйвера анти-чита EXENS

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://a0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1.selstorage.ru/exens_service.exe](https://github.com/Art3mLapa/unofficial-stalcraft-api#--httpsa0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1selstorageruexens_serviceexe) - Ссылка для скачивания актуального драйвера EXENS

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://sc-exens.b-cdn.net](https://github.com/Art3mLapa/unofficial-stalcraft-api#--httpssc-exensb-cdnnet) - CDN сервер системы EXENS

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="35" height="35"> "Зеркала" Официального API игры

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://backend.stalnote.ru/noauthorize/GameItems/uniq](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/README.md#--httpsbackendstalnoterunoauthorizegameitemsuniq) - Скрытые и публичные ID предметов, используемых в EAPI

<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="35" height="35"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="35" height="35"> [https://cdn.stalcraft.wiki/exbo_item_parser/listing.json](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/README.md#--httpscdnstalcraftwikiexbo_item_parserlistingjson) - Сжатый статичный вариант stalcraft-database

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="50" height="50"> http://launcher.stalcraft.net/metrics
Ссылка, отвечающая за отправку метрики игрока для аналитики.
Метрика содержит:
- Сетевые данные (Объём трафика, длительность загрузок)
- Ошибки (Повреждённые файлы)
- Поведение пользователя в игре или на сайтах *exbo.net
- Профилирование (время выполнения операций)
- IP и геолокация 

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/test
Ссылка, которая вызывается при авторизации в лаунчере. Проверяет безопасность подключения. Если трафик нестандартный или подозрительный - вызывается предупреждение (см. изображение)
 <img width="827" height="120" alt="image" src="https://github.com/user-attachments/assets/432b0dc9-4189-413b-8dbc-553f01a8e3f4" />

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/launcher?list=true
Ссылка для получения хеш-суммы важных технических модулей в лаунчере.

Пример ответа:
```
// Размер файла в байтах | Путь к файлу | Хеш-сумма

6122354 native/jlibtorrent.dll 5b1adfe04f083a4d97aa5833f7ca2e9d537b0f73
179320 native/jmt.dll 21fd89dcd5372c73dec175fd51d295e67c23d576
203 args.txt f1ab170fc9b07f014c6d56ce11e9656ff387bdd5
4552962 launcher.jar 7c5b039cce00034993dd1fc544b96bdd29a6677b
148480 native/registry.dll 26e7733f0bc23c4078f91cb805cd504a8042556a
230 args_new.txt 19c98f70a11a7ec85d8d0ef05f942e97c7226251
373280 native/ExboOptimizer.exe d10e42af7d324091e35fe8f12263a04b49db8f47
```

Путь к файлу используется для установки конкретного модуля, через ссылку `http://launcher.stalcraft.net/launcher?name=`

Пример такой ссылки:
`http://launcher.stalcraft.net/launcher?name=native/jlibtorrent.dll`

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/auth
Ссылка для авторизации пользователя EXBO в лаунчере. Используется в лаунчере в четырёх вариациях.
Так-же у ссылки есть вариант домена для EU игроков лаунчера: http://launcher-global.stalcraft.net/

Более правильная и подробная информация есть в [этом](https://github.com/Nyrokume/Exbo-security) проекте
### 1. Авторизация по логину/паролю
Вызывается при обычном вводе логина и пароля в лаунчере. Нужен для получения хеша пароля

Пример ответа:
```
{
  "displayLogin": null,
  "genericError": null,
  "licenseAccepted": false,
  "loginURL": null,
  "mailAbbreviation": null,
  "newEmail": null,
  "newEmailHash": null,
  "secretHash": "asdasdasdasd.1231231",
  "session": null,
  "timeLeft": -1,
  "token": null,
  "trueLogin": null,
  "type": "POW_BCRYPT",
  "untilChangingFinish": null
}
```

Имеет параметры:

- `state=true` -
- `login=LoginUser` - Логин пользователя EXBO
- `pass=Qwerty123123` - Пароль
- `bootstrap=123123123123123132131321313213123213` - Хеш bootstrap.jar
- `hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123` - HardWare ID
- `id=43211234-1234-4321-1234-12312312312333` - ID авторизации
- `protocol_version=3` - Версия протокола лаунчера
- `start=true` - 

Пример правильной ссылки:

```http://launcher.stalcraft.net/auth?state=true&login=LoginUser&pass=Qwerty123123&bootstrap=123123123123123132131321313213123213&hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123&id=43211234-1234-4321-1234-12312312312333&protocol_version=3&start=true```

### 2. Авторизация с хешем пароля
Второй запрос авторизации, если на самом аккаунте нету 2FA аунтефикации то происходит вход в лаунчер.

Пример ответа:

```
{
  "displayLogin": null,
  "genericError": null,
  "licenseAccepted": true,
  "loginURL": null,
  "mailAbbreviation": null,
  "newEmail": null,
  "newEmailHash": null,
  "secretHash": null,
  "session": null,
  "timeLeft": -1,
  "token": null,
  "trueLogin": "UserLogin",
  "type": "GOOGLE_AUTH",
  "untilChangingFinish": null
}
```

Имеет параметры:

- `state=true` -
- `login=LoginUser` - Логин пользователя EXBO
- `pass=Qwerty123123` - Пароль
- `passhash=asd3$d2sa$a1bc$.12312asd12313asd213.123dsa` - Хеш пароля 
- `bootstrap=123123123123123132131321313213123213` - Хеш bootstrap.jar
- `hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123` - HardWare ID
- `id=43211234-1234-4321-1234-12312312312333` - ID авторизации
- `protocol_version=3` - Версия протокола лаунчера

Пример правильной ссылки:

```http://launcher.stalcraft.net/auth?state=true&login=LoginUser&pass=Qwerty123123&passhash=asd3$d2sa$a1bc$.12312asd12313asd213.123dsa&bootstrap=123123123123123132131321313213123213&hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123&id=43211234-1234-4321-1234-12312312312333&protocol_version=3```

### 3. Авторизация с использование 2FA кода (приложения/почты)

Пример ответа:

```
{
  "displayLogin": null,
  "genericError": null,
  "licenseAccepted": true,
  "loginURL": null,
  "mailAbbreviation": "art***@gmail.com",
  "newEmail": null,
  "newEmailHash": null,
  "secretHash": null,
  "session": "12345678-1234-1234-1234-123456789012",
  "timeLeft": -1,
  "token": "12345678-1234-1234-1234-123456789012",
  "trueLogin": "UserLogin",
  "type": "OK",
  "untilChangingFinish": null
}
```

Имеет параметры:

- `secret=123456` / `code=123456789` - Код приложения/почта
- `login=UserLogin` - Логин пользователя EXBO
- `id=43211234-1234-4321-1234-12312312312333` - ID авторизации
- `protocol_version=3` - Версия протокола лаунчера
- `hwid=...` - Используется при авторизации через почту

Пример правильной ссылки:

```http://launcher.stalcraft.net/auth?secret=123456&login=UserLogin&id=43211234-1234-4321-1234-1231231231233&protocol_version=3```

### 4. Автовход в лаунчер
Вызывается при запуске лаунчера при наличии сессии в реестре.

Пример ответа:
```
{
    "displayLogin": null,
    "genericError": null,
    "licenseAccepted": true,
    "loginURL": null,
    "mailAbbreviation": "mai***@mail.ru",
    "newEmail": null,
    "newEmailHash": null,
    "secretHash": null,
    "session": "12345678-1234-1234-1234-123456789012",
    "timeLeft": -1,
    "token": "12345678-1234-1234-1234-123456789012",
    "trueLogin": "userLogin",
    "type": "OK",
    "untilChangingFinish": null
}
```

Имеет параметры:

- `state=false` -
- `login=...` - Логин пользователя EXBO
- `session=...` - Сессия лаунчера (из реестра)
- `bootstrap=123123123123123132131321313213123213` - Хеш bootstrap.jar
- `hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123` - HardWare ID (есть защита от подмены, если HWID не совпадёт - WRONG_HWID)
- `id=43211234-1234-4321-1234-12312312312333` - ID авторизации
- `protocol_version=3` - Версия протокола лаунчера
- `start=true` - 

Пример правильной ссылки:

```http://launcher.stalcraft.net/auth?state=false&login=UserLogin&session=12345678-1234-1234-1234-123456789012&bootstrap=123123123123123132131321313213123213&hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123&protocol_version=3&id=43211234-1234-4321-1234-12312312312333&start=true```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/distributor
Авторизация через дистрибьютора. Используется при входе через Steam в лаунчере.
Так-же у ссылки есть вариант домена для EU игроков лаунчера: http://launcher-global.stalcraft.net/
### 1. Получение ссылки для логина через дистрибьютора
Вызывается при нажатии кнопки "Войти через Steam"
Пример ответа:
```json
{
  "displayLogin": null,
  "genericError": null,
  "licenseAccepted": false,
  "loginURL": "https://steamcommunity.com/openid/login?openid.ns=http://specs.openid.net/auth/2.0&openid.mode=checkid_setup&openid.return_to=https://exbo.net/social/launcherLogin/steam/123123123123123132131321313213123213/12345&openid.realm=https://exbo.net&openid.identity=http://specs.openid.net/auth/2.0/identifier_select&openid.claimed_id=http://specs.openid.net/auth/2.0/identifier_select",
  "mailAbbreviation": null,
  "newEmail": null,
  "newEmailHash": null,
  "secretHash": null,
  "session": "123123123123123132131321313213123213",
  "timeLeft": -1,
  "token": "steam",
  "trueLogin": null,
  "type": "DISTRIBUTOR_PENDING",
  "untilChangingFinish": null
}
```

Имеет параметры:
- `state=true` -
- `distributor=steam` - Дистрибьютор
- `socket_port=12345` - Порт сокета ExboLink
- `bootstrap=...` - Хеш bootstrap.jar
- `hwid=...` - HardWare ID
- `id=...` - ID авторизации
- `protocol_version=3` - Версия протокола лаунчера

Пример запроса:
```http://launcher.stalcraft.net/distributor?state=true&distributor=steam&socket_port=12345&bootstrap=123123123123123132131321313213123213&hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123&id=43211234-1234-4321-1234-12312312312333&protocol_version=3```

### 2. Возврат из браузера через URL-протокол
После логина на сайте вызывается URL-протокол EXBO, ведущий на файл ExboLink.exe:
```
exbo://launcher/12345?action=distributor_auth&auth_token=ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz012345678999&verify_token=AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPp&session_key=9876543210zyxwvutsrqponmlkjihgfedcbaZYXWVUTSRQPONMLKJIHGFEDCBA99
```

### 3. Авторизации через дистрибьютора
Последний этап, запрос информации для входа в лаунчер.

Пример ответа:
```json
{
  "displayLogin": "DisplayLogin",
  "genericError": null,
  "licenseAccepted": true,
  "loginURL": null,
  "mailAbbreviation": "art***@gmail.com",
  "newEmail": null,
  "newEmailHash": null,
  "secretHash": null,
  "session": "12345678-1234-1234-1234-123456789012",
  "timeLeft": -1,
  "token": "12345678-1234-1234-1234-123456789012",
  "trueLogin": "stm:ID",
  "type": "OK",
  "untilChangingFinish": null
}
```
Имеет параметры:

- `state=true` -
- `hwid=...` - HardWare ID
- `distributor=steam` - Имя дистрибьютора
- `id=...` - ID авторизации
- `distributor_session=...` - ID авторизации через дистрибьютора
- `verify_token=...` - Токен проверки авторизациии
- `protocol_version=3` - Версия протокола лаунчера

Пример запроса:
```http://launcher.stalcraft.net/distributor?state=true&hwid=asdabcasdabc123321asdbcasdabc321asdabcasdabc123asdabcasdbc32123123123&id=43211234-1234-4321-1234-12312312312333&protocol_version=3&distributor=steam&distributor_session=123123123123123132131321313213123213&verify_token=AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPp```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/listServers
Ссылка, отвечающая за получение информации об игровом сервере и игре STALCRAFT, такие как онлайн на сервере, HTTP сиды, размер игры в байтах и т.д.

Пример короткого ответа (full=false)
```json
{
  "success": true,
  "data": [
    {
      "id": "stalcraft", // ID сервера
      "onlineCurrent": 19862, // Онлайн на сервере в данный момент
      "onlineMax": 50000, // Максимальный онлайн сервера
      "runCommand": "\"<java>/java/bin/stalcraft.exe\" -classpath \"classes.jar;libs.jar;modassets\" -XX:-PrintCommandLineFlags -XX:ErrorFile=crash-reports/hs_err_pid%p.log -Xmx<mem>m \"-Djava.library.path=<java>/java/bin\" -Dfile.encoding=UTF-8 -Dshow_globally_enabled=false -Dread_derived=true -DCustomNpcsSoundCache=true -Dload_dumped_event_classes=true -DusePrestitchedAtlas=true -Ddisable_item_atlas=true -Ddisable_mod_parsing=true -Duse_system_class_loader=true -XX:+UseG1GC -XX:MaxGCPauseMillis=3 -Dmanagement-metrics=true exbo.stalcraft.client.Main --username=<usr> --session <sess> --gameDir \"<cd>\" --assetsDir \"<cd>/assets\" --dlogin \"<dlogin>\"", // Аргументы для запуска игры (stalcraft.exe)
      "version": "3f39f5281ec4c5c69d768769b6a1fe497b62956" // Версия игры
    }
  ],
  "preventRelog": true
}
```

Пример полного ответа (full=true):
```json
{
  "success": true,
  "data": "
  [
    {
      "background": "https://launcher.stalcraft.net/files?name=stalcraft.jpg", // Ссылка для подкачки фонового изображения в лаунчере
      "caption": "STALCRAFT: X", // Титульное название сервера
      "desc": [ // Описание
        "Stalcraft - это массовый многопользовательский онлайн-шутер от первого лица,",
        "погружающий Вас в альтернативную историю Чернобыльской зоны отчуждения.",
        "",
        "Сможете ли Вы выжить в этом мире?",
        "Опасные мутанты, уникальные артефакты, непроходимые катакомбы, кишащие ",
        "аномалиями и, конечно же, другие авантюристы, желающие разгадать загадки Зоны.",
        "",
        "Правда, даже самые сильные игроки не смогут добиться успеха в одиночку. ",
        "Объединяйтесь в Группировки, участвуйте в Захватах, бросайте вызов соперникам,",
        "планируйте вылазки и исследования.",
        "",
        "Зона ждёт.",
        "Всё в твоих руках, Сталкер!"
      ],
      "exclusions": [ // Исключения
        "activitylog",
        "autosaves",
        "crash-reports",
        "config",
        "saves",
        "screenshots",
        "logs",
        "stats",
        "customnpcs",
        "map_cache",
        "options.txt",
        "optionsof.txt",
        "optionsof_new1.txt",
        "gloomyoptions.txt",
        "gloomyoptions_new.txt",
        "smart_moving_options.txt",
        "alsoftrc.txt",
        "radio"
      ],
      "httpSeeds": [ // HTTP сиды для подкачки ассетов во время игры
        "http://exbo.b-cdn.net/stalcraft/",
        "http://m-cdn.exbo.net/stalcraft/"
      ],
      "icon": "https://launcher.stalcraft.net/files?name=stalcraft_icon.png", // Ссылка для подкачки иконки сервера
      "id": "stalcraft", // ID сервера
      "info": null, // info сервера
      "onlineCurrent": 20565, // Онлайн на сервере на данный момент
      "onlineMax": 50000, // Максимальный онлайн сервера
      "pingTarget": "85.119.149.112:30037", // IP адрес сервера
      "runCommand": "\"<java>/java/bin/stalcraft.exe\" -classpath \"classes.jar;libs.jar;modassets\" -XX:-PrintCommandLineFlags -XX:ErrorFile=crash-reports/hs_err_pid%p.log -Xmx<mem>m \"-Djava.library.path=<java>/java/bin\" -Dfile.encoding=UTF-8 -Dshow_globally_enabled=false -Dread_derived=true -DCustomNpcsSoundCache=true -Dload_dumped_event_classes=true -DusePrestitchedAtlas=true -Ddisable_item_atlas=true -Ddisable_mod_parsing=true -Duse_system_class_loader=true -XX:+UseG1GC -XX:MaxGCPauseMillis=3 -Dmanagement-metrics=true exbo.stalcraft.client.Main --username=<usr> --session <sess> --gameDir \"<cd>\" --assetsDir \"<cd>/assets\" --dlogin \"<dlogin>\"", // Аргументы для запуска игры (stalcraft.exe)
      "totalSize": 36295702714, // Размер игры (в байтах)
      "version": "3f39f5281ec4c5c69d768769b6a1fe497b62956" // Версия игры
    }
  ]",
  "preventRelog": true
}
```

Так-же у ссылки есть вариант домена для EU игроков лаунчера: `http://launcher-global.stalcraft.net/`

Имеет параметры:
- `full=false` - Отвечает за количество информации в ответе. если равен true, ответ будет содержать более детальную информацию об серверах, файлах и ссылках
- `token=11111111-2222-3333-4444-555555555555` - Токен сессии пользователя EXBO (не токен из реестра!)
- `login=User` - Логин пользователя EXBO

Пример ссылки с правильными параметрами:
- ```http://launcher.stalcraft.net/listServers?full=false&token=11111111-2222-3333-4444-555555555555&login=User```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://tracker1.stalcraft.net  |   http://tracker2.stalcraft.net
Torrent трекеры, используются для раздачи файлов игры через файл `stalcraft.torrent.bin`

Имеет параметры:
- `info_hash=12345678900987654321` - Хеш скачиваемого файла
- `peer_id=-LT12J0-abc-de123456` - ID пира скачивания/раздачи
- `port=52525` - Порт
- `uploaded=0` `downloaded=0` `left=292552704` `corrupt=0` - Информация об скачивании/раздаче файлов (в байтах)
- `key=C87A7012` - Ключ для доступа к трекеру
- `event=paused` - Состояние скачивания/раздачи
- `numwant=200` `compact=1` `no_peer_id=1` `supportcrypto=1` `redundant=0` - Прочая информация, необходимая для трекера

Пример ссылки с правильными параметрами:
- ```http://tracker1.stalcraft.net:6767/announce?info_hash=%af%1e%3d%ad%25j%b7%0d%bcrH0Z%a8%d3%a68%3c%27%7b&peer_id=-LT12J0-nMr-gyluoL.3&port=52580&uploaded=0&downloaded=0&left=292552704&corrupt=0&key=C87A7012&event=paused&numwant=200&compact=1&no_peer_id=1&supportcrypto=1&redundant=0```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://m-cdn.exbo.net | http://exbo.b-cdn.net | http://sc-client-dev.cdn77.exbo.net/stalcraft/
CDN ссылки, используются для скачивания файлов игры непосредственно с серверов EXBO

Оба домена отвечают за скачивание файлов игры (модели, текстуры, спрайты, анимации, классы игры, технические исполняемые файлы)

Имеет параметры:
- `stalcraft` - [ID сборки](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/INVESTIGATION.md)
- `stalcraft` - [ID сервера](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/INVESTIGATION.md)
- `ab123c321abc123abccab123321123` - [Хеш-сумма файла из структуры torrentData](https://sc-file.readthedocs.io/en/latest/formats.html#map-mapping-hashes-hashmap-bt)

- `stalcraft_global` - ID сборки/сервера на EU регионе

Пример ссылки с правильными параметрами:
- ```http://exbo.b-cdn.net/stalcraft/stalcraft/4afe071af1859daef6e360b74eaca32cd8324f5d```
- ```http://m-cdn.exbo.net/stalcraft/stalcraft/4afe071af1859daef6e360b74eaca32cd8324f5d```
- ```http://sc-client-dev.cdn77.exbo.net/stalcraft/stalcraft/4afe071af1859daef6e360b74eaca32cd8324f5d```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://dev-cdn.xexbo.ru/
CDN ссылка для скачивания файлов ОТС игры (и, предположительно, файлов ЗТС, Админской сборки игры)

Имеет параметры:
- `stalcraft_ots` - [ID сборки](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/INVESTIGATION.md)
- `stalcraft_ots` - [ID сервера](https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/INVESTIGATION.md)
- `ab123c321abc123abccab123321123` - [Хеш-сумма файла из структуры torrentData](https://sc-file.readthedocs.io/en/latest/formats.html#map-mapping-hashes-hashmap-bt)

Пример ссылки с правильными параметрами:
- ```http://dev-cdn.xexbo.ru/stalcraft_ots/stalcraft_ots/650b0b1fe42db383ada4a257abbea87171c87102```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="50" height="50"> http://85.119.149.147:33000
Альтернативный эндпоинт backend.stalcraftx.ru для ОТС серверов. Имеет те же ссылки как и оригинальный домен:

- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="25" height="25"> [/address_list
](http://85.119.149.147:33000/address_list?login=stm%3A76561199886632490)
- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="25" height="25"> /session/game

- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="25" height="25"> /check_version

- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="25" height="25"> /characters/list

- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="25" height="25"> /characters/accept_legal

- <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="25" height="25"> /backup_email

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/joinGame
Ссылка, которая вызывается при входе в игру.

Имеет параметры:
- `token=11111111-2222-3333-4444-555555555555` - Токен пользователя EXBO (не токен с реестра!)
- `login=User`- Логин пользователя EXBO
- `protocol_version=3` - Версия сетевого протокола

Пример ссылки с правильными параметрами:
- ```http://launcher.stalcraft.net/joinGame?token=11111111-2222-3333-4444-555555555555&login=User&protocol_version=3```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/kontora_mrazei.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> http://launcher.stalcraft.net/torrentData
Ссылка, отвечающая за подкачку stalcraft.torrent.bin (TORRENT-подобного файла для скачивания файлов игры), которая вызывается во время игры и во время обновления игры.

Само содержимое представляет из себя немного изменённую копию технического файла [stalcraft.torrent.bin](https://github.com/onejeuu/sc-file/blob/master/templates/TORRENT.BIN.bt), сжатый методом [gzip](https://ru.wikipedia.org/wiki/Gzip). Сама структура представляет из себя список файлов и хеша, который используется CDN серверами для подкачки сломанных, недостающих файлов игры (или для загрузки новых файлов при обновлении)

<img width="824" height="945" alt="image" src="https://github.com/user-attachments/assets/513c8a31-ed52-462c-90cd-5051e027eee8" />


Имеет параметры:
- `id=stalcraft`- ID сервера на который произошел вход
- `token=11111111-2222-3333-4444-555555555555` - Токен пользователя EXBO (не токен с реестра!)
- `login=User`- Логин пользователя EXBO

Пример ссылки с правильными параметрами:
- ```http://launcher.stalcraft.net/torrentData?id=stalcraft&token=11111111-2222-3333-4444-555555555555&login=User```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="50" height="50"> https://backend.stalcraftx.ru/session/game
Ссылка, отвечающая за получение ключей для доступа к backend.stalcraft.ru, через значение session. Для правильной работы сессии в работе с другими ссылками, значение проходит через ряд криптографических вычислений, с использованием "ключа" который невозможно извлечь из запросов или игры. Эта методика работает со всеми backend запросами (/joinGame<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="15" height="15">; /characters/list<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="15" height="15">)

Пример ответа:
```json
{
   "connectToken" : "...",
   "session" : "...",
   "udp_mode" : "RECOMMENDED"
}
```

Имеет параметры:
- `login=User` - Логин пользователя EXBO / `login=stm:123123123123123123` - ID аккаунта STEAM
- `session=wIHhcjLP%abcde123456789009876543211234567890` - Сессия (из ответа /joinGame<img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="15" height="15">)
- `distributor=EXBO` - Дистрибьютор игры
- `connectPubKey=abcdeedcba123456789009887654321%3D` - Ключ для подключения

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://backend.stalcraftx.ru/address_list
Ссылка, отвечающая за выдачу список IP адресов всех доступных игровых серверов.

Пример ответа:
```json
{
   "clientToTunnelRttWeight" : 1,000000000000000,
   "mode" : "roxy",
   "pools" : [
      {
         "name" : "CLOUD-RU-7",
         "tunnels" : [
            {
               "address" : "111.222.33.444:12345",
               "name" : "SRVMGR-ACCESSOR-OFT-RU-7A"
            }
         ]
      },
      {
         "name" : "MSK2",
         "tunnels" : [
            {
               "address" : "111.222.33.444:12345",
               "name" : "MSK2-1"
            },
            ...
            {
               "address" : "111.222.33.444:12345",
               "name" : "MSK2-16"
            }
         ]
      },
      ...
            }
         ]
      }
   ]
}
```

Имеет параметры:
- `login=User` - Логин пользователя EXBO / `login=stm:123123123123123123` - ID аккаунта STEAM

Пример ссылки с правильными параметрами:
- ```https://backend.stalcraftx.ru/address_list?login=User```

Для остальных регионов (EU, SEA, NA) нету эндпоинтов для получения списка адресов туннелей, но есть вручную добытые списки серверов:

- EU ```https://raw.githubusercontent.com/Art3mLapa/unofficial-stalcraft-api/refs/heads/main/static/address_list/EU.json```
- SEA ```https://raw.githubusercontent.com/Art3mLapa/unofficial-stalcraft-api/refs/heads/main/static/address_list/SEA.json```
- NA ```https://raw.githubusercontent.com/Art3mLapa/unofficial-stalcraft-api/refs/heads/main/static/address_list/NA.json```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://backend.stalcraftx.ru/characters/list
Ссылка, которая выдаёт очень много технической информации об персонажах на аккаунте

Пример ответа:
```json
{
   "accepted_legal_version" : "v8_ru_launcher",
   "characters" : [
      {
         "allianceId" : "freedom",
         "armor" : {
            "Count_i" : {
               "type" : "integer",
               "value" : 1
            },
            "Damage" : {
               "type" : "short",
               "value" : 0
            },
            "id" : {
               "type" : "short",
               "value" : 25352
            },
            "s_hasUuid" : {
               "type" : "byte",
               "value" : 1
            },
            "s_uuidL" : {
               "type" : "long",
               "value" : -6387157833297061400
            },
            "s_uuidM" : {
               "type" : "long",
               "value" : 946651913389492576
            },
            "tag" : {
            ...
            },
                  "owner" : {
                     "type" : "string",
                     "value" : "User"
                  },
                  "sm" : {
                     "type" : "string",
                     "value" : ""
                  },
                  "src" : {
                     "type" : "byte",
                     "value" : 22
                  },
                  "u1" : {
                     "type" : "long",
                     "value" : 6737737881701861134
                  },
                  "u2" : {
                     "type" : "long",
                     "value" : -6489271771595462926
                  }
               }
            }
         },
         "clan" : "Название клана",
         "clanIcon" : {
            "color" : {
               "type" : "integer",
               "value" : -12324269
            },
            "icon" : {
               "type" : "string",
               "value" : "freedom"
            }
         },
         "gearScore" : 756,
         "isLegacy" : false,
         "lastLogin" : 1755092351744,
         "locationUnlocalized" : "location.base_freedom.name",
         "maxGearScore" : 1486,
         "money" : 372937,
         "playedTime" : 3254772226,
     ...
   ],
   "characters_limit" : 10,
   "had_characters" : true,
   "reserved_names" : []
}
```

Имеет параметры:
- `login=User` - Логин пользователя EXBO / `login=stm:123123123123123123` - ID аккаунта STEAM
- `session=abcde123456789009876543211234567890` - Сессия
- `distributor=EXBO` - Дистрибьютор игры

Пример ссылки с правильными параметрами:
- ```https://backend.stalcraftx.ru/characters/list?login=User&session=abcde12345678900988765432112345678900987654321234567890253D&distributor=EXBO```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="50" height="50"> https://backend.stalcraftx.ru/characters/create
POST-Запрос для создания нового персонажа на аккаунте

Пример ответа:
```json
{
   "message" : "Character created",
   "status" : 200
}

```

Имеет параметры:

- `login=User` - Логин пользователя
- `session=bxOgSrHHhRs5...` - Сессия игры
- `character=Артемий_Лапа` - Имя персонажа
- `distributor=STEAM` - Дистрибьютор игры

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://stalcraft.net/webhook/region
Ссылка для Discord вебхука игры, в ответе отображает IP, регион серверов и страну пользователя

Пример ответа:
```json
{
   "country" : {
      "default_game_region" : "RU",
      "id" : "RU",
      "name" : "Россия",
      "native_name" : "Россия"
   },
   "ip" : "111.222.333.444",
   "region" : {
      "default_lang" : "ru",
      "id" : "RU"
   }
}
```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://a0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1.selstorage.ru/service.json
Ссылка, предназначенная для получения актуальной ссылки для скачивания драйвера анти-чита EXENS. В отличии от других бекенд-доменов имеет жесткую проверку HTTPS сертификатов

Пример ответа:
```json
{
    "groups": [
        {
            "id": "empty",
            "split": 0,
            "files": [],
            "service": {
                "filename": "",
                "serviceName": "exens"
            }
        },
        {
            "id": "main",
            "split": 0,
            "files": [
                {
                    "name": "ExensService.exe",
                    "hash": "fe8f677bc03cecaa28d73d79598a305fffde23595799854bc42fa8c1230d0137",
                    "url": "files/fe8f677bc03cecaa.exe",
                    "size": 12320408,
                    "signature": "440a2d752fb9266f21cc30226d2eca9f23c79397dfb9c84466d5e4dbd0401fa9507a568ec93698b9394cbdcd58cd18156480f482186bc27e9a2c45d91c450a02"
                },
                {
                    "name": "ExensInstaller.exe",
                    "hash": "1376e6dbf655bbc2ecf4625fe8d2e0e2653e3f8bb35758dca33255f057c6aa61",
                    "url": "files/1376e6dbf655bbc2.exe",
                    "size": 1046168,
                    "signature": "b7fd7089dcfe47cc3e3287fa56af54f5091584af4a4be418b40a3d563f974ffb5bd3d3a958a0aff3e73de1b8c18e41e3e2c1d525a98266bddce733a90f88b002"
                }
            ],
            "service": {
                "filename": "ExensService.exe",
                "serviceName": "exens"
            }
        },
        {
            "id": "kick",
            "split": 1,
            "files": [
                {
                    "name": "ExensService.exe",
                    "hash": "fe8f677bc03cecaa28d73d79598a305fffde23595799854bc42fa8c1230d0137",
                    "url": "files/fe8f677bc03cecaa.exe",
                    "size": 12320408,
                    "signature": "440a2d752fb9266f21cc30226d2eca9f23c79397dfb9c84466d5e4dbd0401fa9507a568ec93698b9394cbdcd58cd18156480f482186bc27e9a2c45d91c450a02"
                },
                {
                    "name": "ExensInstaller.exe",
                    "hash": "1376e6dbf655bbc2ecf4625fe8d2e0e2653e3f8bb35758dca33255f057c6aa61",
                    "url": "files/1376e6dbf655bbc2.exe",
                    "size": 1046168,
                    "signature": "b7fd7089dcfe47cc3e3287fa56af54f5091584af4a4be418b40a3d563f974ffb5bd3d3a958a0aff3e73de1b8c18e41e3e2c1d525a98266bddce733a90f88b002"
                }
            ],
            "service": {
                "filename": "ExensService.exe",
                "serviceName": "exens"
            }
        }
    ]
}
```
Так-же есть альтернативные домены: 
`https://12d8333a-ecfe-4e46-8cda-022675468cc9.selcdn.net/update.json`
`https://sc-exens.b-cdn.net/update.json`

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://sc-exens.b-cdn.net
CDN сервер для системы EXENS

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/exens.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://a0a070fc-75cc-4e3f-8dd2-7c1ea74c9ab1.selstorage.ru/exens_service.exe
Ссылка скачивания исполняемого файла сервиса EXENS

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://backend.stalcraft.net/class_preload/config
Прелоад классов, выполняется перед запуском игры

Имеет параметры:

- `version=abc12345678909876543211234567890` - GMV(GaMe Version) игры

Пример ссылки с правильными параметрами:

- ```https://backend.stalcraft.net/class_preload/config?version=fb20ef732a044adb984228a13becab80```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/post_logo.png" width="50" height="50"> https://backend.stalcraft.net/class_preload/report
Проверка классов на целостность, выполняется регулярно во время игры

Пример ответа: байткод классов(?)
<img width="2048" height="1314" alt="image psd(42)" src="https://github.com/user-attachments/assets/709eb52b-b603-481b-b950-ebd6d949b7c1" />

Имеет параметры:

- `version=abc12345678909876543211234567890` - GMV(GaMe Version) игры
- `login=User` - Логин пользователя
- `session=bqХaКphE03183568...` - Backend сессия игры
- `distributor=EXBO` - Дистрибьютор

# <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="50" height="50"> "Зеркала" официального API игры
На данный момент, EXBO всё меньше поддерживают EAPI, из-за чего появляется проблема с доступом и получению ключа авторизации. Для решения проблемы вы можете использовать домены сайтов, авторизованных ранее в EAPI.

**ВСЕ АВТОРСКИЕ ПРАВА ПРИНАДЛЕЖАТ ВЛАДЕЛЬЦАМ САЙТОВ**


## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://backend.stalnote.ru/noauthorize/GameItems/uniq
Статическая информация об вещах с аукциона API и датабазы игры, которая содержит вещи, которых нету в этих двух официальных ресурсах.

Пример ответа:
```json
[
  {
    "id": 245602,
    "name": "Самодельный светошум",
    "type": "grenade",
    "pottential": null,
    "quality": null,
    "color": "DEFAULT"
  },
  {
    "id": 245603,
    "name": "РГД-5",
    "type": "grenade",
    "pottential": null,
    "quality": null,
    "color": "RANK_STALKER"
  },
  ...
]
```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://cdn.stalcraft.wiki/exbo_item_parser/listing.json

Сжатый вариант [stalcraft-database](https://github.com/EXBO-Studio/stalcraft-database) в виде JSON структуры с основной информацией об каждом предмете оттуда

Пример ответа:
```json
[
  {
    "id": "1rk6g",
    "category": "armor/clothes",
    "name": {
      "ru": "Бандитский кожак",
      "en": "Bandit Coat",
      "es": "Abrigo de bandido",
      "fr": "Veste de Bandit"
    },
    "color": "DEFAULT"
  },
  ...
]
```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://lunar-client.ru/web-api/stalcraft/auction.php

Получение истории купленных и активных лотов аукциона конкретного предмета.

Пример ответа:
```json
{
  "total": 144,
  "prices": [
    {
      "amount": 1,
      "price": 750000000,
      "time": "2025-12-30T21:08:23Z",
      "additional": {
        "currentMotifDefault": 0,
        "currentVisualDefault": 0,
        "it_transf_count": 2,
        "compens_2024_upgrade_attempts": -1,
        "buyer": "ЗолотойНоми"
      }
    },
    {
      "amount": 1,
      "price": 1250000000,
      "time": "2025-11-28T16:47:31Z",
      "additional": {
        "compens_2024_upgrade_attempts": -1
      }
    },
    ...
    ]
}
```

Имеет параметры:
`action=history` - history - история купленных лотов, lots - история активных лотов
`item=knmdv` - ID предмета из stalcraft-database
`region=ru` - регион аукциона
`limit=200` - лимит на кол-во лотов

Пример правильной ссылки:
- ```https://lunar-client.ru/web-api/stalcraft/auction.php?action=history&item=knmdv&region=ru&limit=200```

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/zerkalo_api.png" width="50" height="50"> <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/get_logo.png" width="50" height="50"> https://lunar-client.ru/web-api/stalcraft/arsenal.php?action=prices

JSON таблица предметов для фарма репутации арсенала, с учетом цены предметов на аукционе в реальном времени

Пример ответа:
```json
{
  "success": true,
  "data": {
    "meta": {
      "description": "Предметы для сдачи Арсену в STALCRAFT:X",
      "targetReputation": 10000,
      "lastUpdated": "2025-01-15"
    },
    "items": [
      {
        "name": "Малый артефактный фрагмент",
        "id": "z3k1m",
        "icon": "/icons/misc/z3k1m.png",
        "color": "DEFAULT",
        "reputation": 1,
        "weight": 0.2,
        "perTenK": 10000,
        "weightPerTenK": 2000,
        "avgPrice": 404,
        "totalPrice": 4040000
      },
      ...
    ]
}
```

# <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/dev_bless.png" width="5%" height="5%"> Based on UAPI
- https://github.com/FakeAngles/Stalcraft-Server-Blocker - Сбежать с MSK2 возможно
- https://github.com/Nyrokume/Exbo-security - Интерактивная веб-страница с исследованием системы верификации владельцев аккаунтов EXBO (Stalcraft)
- https://github.com/Art3mLapa/stalcraftx.status - Сайт с отображением онлайна на РУ серверах STALCRAFT:X и отображением пинга игровых серверов
- https://github.com/Art3mLapa/Krevetka-ts - re-writted and automatic Krevetka on TypeScript 

## <img src="https://github.com/Art3mLapa/unofficial-stalcraft-api/blob/main/assets/icon_logo.png" width="50" height="50"> Благодарность

Анализ и поиск ссылок - [HTTP Debugger](https://httpdebugger.com/)

Некоторая информация об ссылках - [@oarer](https://github.com/oarer)

JSON сервера (address_list) EU региона - Kesame (kwlxx)

Добавил авторизацию через дистрибьютора - [@TeamDima](https://t.me/TeamDima)







