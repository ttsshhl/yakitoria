# YAKISTORI — сайт доставки суши (Ессентуки)

Статический сайт: один `index.html` + папка `img`.

## Публикация на GitHub Pages

1. Загрузить ВСЕ файлы в корень репозитория (index.html, img/, иконки, .nojekyll).
2. Settings → Pages → Source: Deploy from a branch → Branch: `main`, папка `/ (root)`.
3. Settings → Pages → Custom domain: вписать домен → Save.
   GitHub сам создаст файл CNAME в репозитории.
4. Включить "Enforce HTTPS" (появится через 10–60 минут после проверки DNS).

## DNS на reg.ru

Для домена без www (например yakistori.ru) — 4 записи типа A, поле "Субдомен" = `@`:

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153

Плюс одна запись CNAME: субдомен `www` → `ВАШ-ЛОГИН.github.io.` (с точкой в конце)

Старые записи A / CNAME для `@` и `www` (парковка reg.ru) — удалить.

## Проверка

    nslookup yakistori.ru

Должны вернуться 4 адреса 185.199.x.153.
