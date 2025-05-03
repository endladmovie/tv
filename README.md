# Endlad TV 📺

**Endlad TV** — это простой и бесплатный онлайн-плеер для просмотра ТВ-каналов через веб-браузер. Каналы берутся из открытого JSON API и отображаются с иконками и названиями. Всё работает прямо из браузера без рекламы, регистрации и платных подписок.

## 🚀 Как это работает

1. Страница [`tv.html`](https://endladmovies.github.io/tv/tv.html) перенаправляет на `index.html`.
2. `index.html` загружает список каналов из JSON-файла:
https://raw.githubusercontent.com/endladmovie/tv/main/tv.json

pgsql
Копировать
Редактировать
3. Каждый канал отображается с названием, иконкой, и по клику открывается `tv-watch.html`.
4. Страница `tv-watch.html` загружает канал в `iframe`.

## 📦 Пример структуры JSON (`tv.json`)

```json
[
{
 "title": "Discovery Channel",
 "icon": "https://example.com/discovery.png",
 "url": "https://rutube.ru/play/embed/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
},
{
 "title": "ЩПНР: Щас поедем на рыбалку | 24/7",
 "icon": "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAAD...",
 "url": "https://rutube.ru/play/embed/yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy"
}
]
```





🖥️ Использование - 
Зайди на: tv.html

Выбери канал и смотри в tv-watch.html без рекламы.

🔌 API
Ты можешь использовать файл tv.json как простой публичный API:


GET https://raw.githubusercontent.com/endladmovie/tv/main/tv.json
Ответ — массив каналов:

title: Название канала

icon: Ссылка на иконку (может быть base64)

url: Прямая ссылка для встраивания в iframe

⚠️ Ограничения
Некоторые каналы могут требовать VPN или быть недоступны из-за ограничений Rutube или других платформ.



💡 Хочешь добавить свой канал?
Форкни репозиторий: https://github.com/endladmovie/tv

Отредактируй tv.json, добавь свой канал.

Создай pull request.

🧑‍💻 Автор
Telegram: t.me/endladsa

GitHub: @endladmovie

📄 Лицензия
MIT — используй, редактируй, делись.
