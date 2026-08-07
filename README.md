<div align="center">

<samp>&gt; Hey There!, I am <b>Igor Guryan</b></samp>

# Backend Developer · Go

<samp>「 Krasnodar, Russia 」</samp>

<br>

[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://sacujo.t.me)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/Sacujo)
[![Codewars](https://img.shields.io/badge/Codewars-B1361E?style=for-the-badge&logo=codewars&logoColor=white)](https://www.codewars.com/users/Sacujo)

</div>

---

## Обо мне

Пишу бэкенд на **Go**. Последний проект — HTTP-сервер с нуля поверх TCP, без веб-фреймворков и без единой внешней зависимости.

До этого четыре года в iOS-разработке на Swift. Выпускник **Школы мобильной разработки Яндекса (ШМР, 2025)**: в финале — командный проект из ~20 человек, где отвечал за чат с ИИ-ассистентом.

> **Почему бэкенд.** В мобильной разработке мне всегда была интереснее не вёрстка экранов, а то, что под ней: сеть, многопоточность, данные. В Swift это были `URLSession`, `GCD` и `async/await` — в Go те же задачи решаются проще и явнее. Переход получился не с нуля, а сменой инструмента при том же круге задач.

---

## Стек

<div align="center">

**Основное**

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![JSON](https://img.shields.io/badge/REST_/_JSON-005571?style=flat-square)

**Предыдущий опыт**

![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-0071E3?style=flat-square&logo=swift&logoColor=white)
![UIKit](https://img.shields.io/badge/UIKit-2396F3?style=flat-square&logo=uikit&logoColor=white)
![Xcode](https://img.shields.io/badge/Xcode-147EFB?style=flat-square&logo=xcode&logoColor=white)

</div>

<details>
<summary><b>Подробный список технологий</b></summary>

<br>

**Go**

| | |
| --- | --- |
| Язык | структуры, интерфейсы, методы, обработка ошибок через `error` и sentinel-значения |
| Сеть | TCP-сокеты (`net`), устройство HTTP/1.1, ручной разбор и сборка запросов и ответов |
| Конкурентность | горутины, `sync` |
| Инфраструктура | PostgreSQL (`database/sql` + драйвер `pgx`), Docker, Docker Compose |
| Данные | `encoding/json`, `bufio`, `strings.Builder` |
| Инструменты | `go mod`, `gofmt`, `go vet`, детектор гонок |

**Общее**

ООП, протокол-ориентированное программирование, SOLID, внедрение зависимостей · REST и работа с внешними API · Git: ветки, pull request'ы, code review в команде · алгоритмы и структуры данных

**Swift / iOS**

| | |
| --- | --- |
| UI | SwiftUI, UIKit, вёрстка кодом (`NSLayoutConstraint`, SnapKit) |
| Сеть | `URLSession`, multipart-загрузка файлов |
| Многопоточность | `async/await`, `@MainActor`, GCD |
| Хранение | FileManager + JSON, UserDefaults, CoreData, Realm |
| Архитектуры | MVVM, MVC, MVP, DI-контейнер |
| Зависимости | SPM, CocoaPods |

</details>

---

## Проекты

### url-shortener — сервис коротких ссылок

[![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)](https://github.com/Sacujo/url-shortener)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
[![Repo](https://img.shields.io/badge/код-GitHub-181717?style=flat-square&logo=github)](https://github.com/Sacujo/url-shortener)

HTTP-протокол реализован вручную поверх TCP-сокета, без `net/http`. В базовой
(in-memory) конфигурации — ноль внешних зависимостей; единственная зависимость
во всём проекте — драйвер PostgreSQL, и только если он подключён.

- **Свой HTTP-слой** — разбор request line и заголовков, чтение тела по `Content-Length`, сборка ответа со статус-кодами 200/201/302/400/404/500, покрыт табличными тестами
- **Свой роутер и хендлеры** — создание ссылки, редирект, статистика переходов в JSON
- **Хранилище за интерфейсом** `Storage` — in-memory и PostgreSQL-реализации, переключаются конфигом (`STORAGE_DRIVER`) без изменений в остальном коде
- **PostgreSQL в Docker Compose** — таблица создаётся автоматически при старте, счётчик кликов инкрементируется атомарным `UPDATE` на стороне БД
- **Конкурентность** — каждое соединение обрабатывается в отдельной горутине; доступ к in-memory хранилищу защищён `sync.RWMutex`, проверено `go test -race`
- **Структура** `cmd/` + `internal/`: web → router → handler → storage → model
---

### Goowee — ассистент для родителя

![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-0071E3?style=flat-square&logo=swift&logoColor=white)
![Команда](https://img.shields.io/badge/команда-~20_человек-blue?style=flat-square)
![NDA](https://img.shields.io/badge/код-под_NDA-lightgrey?style=flat-square)

Финальный проект **Школы мобильной разработки Яндекса, 2025**. Продукт из четырёх частей: iOS, Android, Python-микросервисы и RAG-пайплайн. Работа по git flow — ветки, pull request'ы, code review.

Мой вклад в iOS-приложение:

- **Экран чата с ИИ-ассистентом целиком** — список сообщений, ввод с ограничением и счётчиком символов, рендер markdown, состояния загрузки и ошибок, история диалогов, выбор и отправка файлов
- **`ChatService`** — сетевой слой на `async/await` за протоколом, включая multipart-загрузку файлов
- **`ChatStorageService`** — персистентное хранение диалогов и файлов в JSON, тоже за протоколом: сервисы подменяются моками
- **`AppRouter`** — навигация приложения: модальное открытие чата поверх табов, скрытие таббара, возврат на исходную вкладку
- **`DIContainer`** и вынос `TabBar` в отдельный SPM-пакет `AppComponents`

*Исходный код закрыт по NDA — готов подробно рассказать об архитектуре и решениях на собеседовании.*

---

### Ранние iOS-проекты

![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white)
![UIKit](https://img.shields.io/badge/UIKit-2396F3?style=flat-square&logo=uikit&logoColor=white)

[**EventHub**](https://github.com/Sacujo/EventHub) — афиша мероприятий · [**BookStore**](https://github.com/Sacujo/BookStore) — книжный магазин, Swift Marathon X · [**MovieHub**](https://github.com/Sacujo/MovieHub) — каталог фильмов

---

## Обучение

**ШМР — Школа мобильной разработки Яндекса**, 2025 · **Harvard CS50** · **swiftbook.ru** · **Paul Hudson «100 Days of Swift»** · **Angela Yu, Udemy** · **Swift Marathon X**

---

<div align="center">

<a href="https://leetcode.com/Sacujo">
  <img src="https://leetcard.jacoblin.cool/Sacujo?theme=dark&font=Domine&ext=heatmap" alt="LeetCode" />
</a>

<br><br>

<a href="https://www.codewars.com/users/Sacujo">
  <img src="https://www.codewars.com/users/Sacujo/badges/large" alt="Codewars" />
</a>

</div>
