<!-- Intro --> <h3 align="center"> <samp>&gt; Hey There!, I am <b>Igor Guryan</b> </samp> </h3> <p align="center"> <samp> <br> 「 Backend Developer · <b>Go</b> · Krasnodar, Russia 」 <br> <br> </samp> </p> <p align="center"> <a href="https://sacujo.t.me" target="_blank"> <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="telegram" /> </a> <a href="https://github.com/Sacujo/url-shortener" target="_blank"> <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="go" /> </a> </p>
Обо мне :
Backend-разработчик на Go. Чтобы разобраться, как устроен веб изнутри, написал сервис коротких ссылок без фреймворков и без внешних зависимостей — с собственным разбором HTTP поверх TCP-сокетов.
До Go — iOS-разработка на Swift с 2021 года. Прошёл swiftbook.ru, Paul Hudson «100 Days of Swift», курс Angela Yu (Udemy), Harvard CS50, участвовал в Swift Marathon X.
Есть опыт командной работы над проектом — полный цикл от макета в Figma до собранного приложения, code review и работа в общем репозитории через ветки и pull request'ы.
Почему перешёл в бэкенд. В мобильной разработке мне всегда была интереснее не вёрстка экранов, а то, что происходит под ней: сеть, многопоточность, работа с данными. В Swift это были URLSession, GCD и async/await — в Go те же задачи решаются проще и явнее, через горутины и каналы. Поэтому переход получился не с нуля, а сменой инструмента при том же круге задач.
Сейчас изучаю: PostgreSQL, Docker, тестирование, устройство HTTP-серверов на уровне стандартной библиотеки.
Регулярно решаю алгоритмические задачи на LeetCode и Codewars (бейджи ниже).
Проекты :
Проект	Описание	Стек
url-shortener	Сервис коротких ссылок, написанный без net/http и без внешних зависимостей: собственный разбор HTTP/1.1 поверх TCP-сокетов, свой роутер, хранилище за интерфейсом, обработка соединений в горутинах	Go, net, bufio, encoding/json
EventHub	Командное приложение-афиша мероприятий	Swift, UIKit
BookStore	Приложение книжного магазина, Swift Marathon X	Swift, UIKit
MovieHub	Командное приложение-каталог фильмов	Swift, UIKit

Языки и инструменты :
<div> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" title="Go" alt="Go" width="40" height="40"/>&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original.svg" title="GitHub" alt="GitHub" width="40" height="40"/>&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" title="Linux" alt="Linux" width="40" height="40"/>&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/swift/swift-original.svg" title="Swift" alt="Swift" width="40" height="40"/>&nbsp; <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/xcode/xcode-original.svg" title="XCode" alt="XCode" width="40" height="40"/>&nbsp; </div>
Технологии :

Go

Язык: структуры, методы, интерфейсы, срезы и мапы, sentinel-ошибки
Сеть: TCP-сокеты (net.Listen / Accept), самостоятельный разбор и сборка HTTP/1.1, маршрутизация, JSON через encoding/json
Конкурентность: горутина на соединение, защита общего состояния через sync.RWMutex, отладка гонок с -race
Стандартная библиотека: bufio, io, strings, strconv, time, math/rand/v2
Тестирование: testing, табличные тесты
Инструменты: go mod, gofmt, go vet, Git (main / develop)

Общее

ООП, протокол-ориентированное программирование, SOLID
REST, клиент-серверное взаимодействие, работа с внешними API
Git: ветки, pull request'ы, code review
Алгоритмы и структуры данных

Swift / iOS (предыдущий опыт)

UIKit, вёрстка кодом (NSLayoutConstraint, SnapKit)
Работа с сетью: URLSession
Хранение данных: UserDefaults, CoreData, Realm
Архитектуры: MVC, MVP
Многопоточность: GCD, async/await
Зависимости: CocoaPods, SPM
