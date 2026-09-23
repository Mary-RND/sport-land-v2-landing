# sport-land-v2-landing

**Лендинг бесплатного вебинара «5 привычек, которые приведут к телу мечты»**
от «Спорт-ленд» — самостоятельный маркетинговый проект в тёплой
бежево-коричневой палитре с editorial-типографикой (Oswald + Playfair Display
+ Commissioner) и чистым HTML/CSS/JS без фреймворков и сборщиков.

![Лендинг, полная версия (desktop)](screenshots/desktop-full.png)

**Live demo:** [yellow-pine-add3.mar-petrushina.workers.dev](https://yellow-pine-add3.mar-petrushina.workers.dev/) — деплой на Cloudflare Workers.

---

## О проекте

Страница построена по классической схеме прогрева под бесплатный вебинар:

```
Герой с оффером + счётчики
   -->
Боли ЦА (знакомо?)
   -->
Подход / привычки, которые станут новой жизнью
   -->
Программа на 3 месяца
   -->
Фильтр «есть / нет»
   -->
Оффер: бесплатный вебинар + форма регистрации
   -->
Кейсы до/после
   -->
Команда
   -->
FAQ
   -->
Финальный CTA
```

## Возможности

- Форма регистрации на вебинар «Имя + телефон + email» с валидацией и маской телефона.
- AJAX-отправка заявки на **FormSubmit** (без своего бэкенда).
- FAQ-аккордеон и бургер-меню.
- Reveal-анимации появления блоков (IntersectionObserver).
- Счётчики результатов с анимацией при скролле.
- Полностью адаптивная вёрстка (mobile / tablet / desktop).
- Editorial-типографика: **Oswald**, **Playfair Display**, **Commissioner**.

## Стек

| | |
|---|---|
| Разметка | HTML5 (семантические секции) |
| Стили | CSS3: custom properties, grid, flexbox, тёплая палитра |
| Логика | JavaScript (vanilla): валидация, маска телефона, аккордеон, reveal |
| Форма | FormSubmit — приём заявок на email |
| Деплой | Статический хостинг (Cloudflare Pages / Workers, Netlify Drop) |

## Запуск

```bash
# локальный просмотр
python -m http.server 8000
# http://localhost:8000/
```

Для деплоя достаточно выложить содержимое папки на любой статический
хостинг (Cloudflare Pages → Upload assets → перетащить папку).

## Структура

```
.
├─ index.html                 # разметка всех секций
├─ styles.css                 # дизайн-система и адаптив
├─ script.js                  # интерактив и отправка формы
├─ images/                    # фото (hero, привычки, кейсы, команда, шаги)
├─ screenshots/
│  ├─ desktop-full.png        # полная версия (desktop, 1440)
│  ├─ desktop-hero.png        # секция hero
│  ├─ desktop-form.png        # форма регистрации
│  └─ mobile-hero.png         # мобильный hero (390)
├─ README.md
└─ LICENSE                    # MIT
```

## Лицензия

MIT — см. `LICENSE`.