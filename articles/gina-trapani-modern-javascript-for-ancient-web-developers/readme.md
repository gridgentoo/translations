# Современный JavaScript для древних веб-разработчиков

*Перевод статьи [Gina Trapani](https://trackchanges.postlight.com/@ginatrapani?source=post_header_lockup): [Modern JavaScript for Ancient Web Developers](https://trackchanges.postlight.com/modern-javascript-for-ancient-web-developers-58e7cae050f9)*

*Оригинальная статья получила много откликов в англоязычном интернете. При кажущейся простоте и очевидности, она всё же содержит правильные мысли, а также даёт неплохой набор ссылок на обучающие материалы.*

![Изучение Javascript с помощью… JavaScript. learnyounode.](https://cdn-images-1.medium.com/max/800/1*_5XMNVNbpIDCDHU1YXZPyA.png)

Есть определённый вид бэкенд веб-разработчика старой школы, который давным давно освоил такие вещи, как Perl или Python, или PHP, или Java Server Pages, возможно, даже Rails или Django. Этот человек работал с гигантскими реляционными базами данных и встроенными API-интерфейсами, которые отдают JSON и даже (*ох!*) XML.

Этот человек — *бэкенд*-разработчик, поэтому в течение долгого времени JavaScript для него был просто забавной игрушкой, что добавляла немного трюков во фронтенд, которые могли заставить вещи на веб-странице менять цвет. Если бы JavaScript был действительно полезным, он добавил бы проверку формы, помогающую предотвратить попадание неверной информации в базу данных. Восемь лет назад jQuery взорвал разум этого человека. Сам JavaScript был языком, который он просто терпел, но никогда не использовал по максимуму.

Затем JavaScript и его современные фреймворки поглотили бэкенд, фронтенд и всё, что было между, и настало время вновь стать веб-разразбочиком в 2017 году — таким, что пишет на JavaScript.

Привет. Я древний веб-разработчик, изучающая современный JavaScript. Я только что начала, и мне одновременно и весело и больно. Есть несколько вещей в мире современного JavaScript, которые нужно понять и принять, прежде чем начать.

Вот некоторые из изменений, которые я должна была привнести в свое собственное мышление, и ожидания относительно изучения новой экосистемы, основанные на старом языке, долго бывшим моим основным ремеслом.

## Движущаяся мишень (точка JS)
Современный мир JS - это ничто, если он не молод и не изменчив, поэтому легко по незнанию выбрать платформу, шаблонизатор или инструмент для сборки, которые уже устарели. Или учебник, что обучает технике, больше не являющейся лучшей практикой (изменчиво даже общепринятое понятие о том, что такое «лучшая практика»).

В этом случае пришло время найти ближайшего дружественного разработчика на современном JavaScript и немного поболтать о том, как вам выбрать правильный путь обучения. Мне повезло получить фантастическое руководство от моих коллег-инженеров здесь, в Postlight (особенно от [Jeremy Mack](https://medium.com/@mutewinter)), и я благодарю их за то, что они терпели мои бесконечные вопросы.

Дело в том, что изучение современного JavaScript требует вмешательства живого человека. Ещё ничего не устаканилось достаточно крепко для учебных программ и руководств, а, чтобы лучшая практика получила авторитет, нужно больше, чем несколько месяцев. Если у вас нет под рукой эксперта, по крайней мере, проверьте дату в этой статье или учебнике, или последний коммит в этом репозитории на GitHub. Если ему больше года, это почти наверняка не то, на что стоит тратить время.

## Новые проблемы, пока-ещё-нестабильные решения
Таким образом: когда вы изучаете современный JavaScript, есть хороший шанс, что решение проблемы, с которой вы столкнулись, все еще разрабатывается. На самом деле, вполне возможно, что только один код ревью отделяет его от вливания в пакет, который вы используете.

Когда вы работаете с древним языком (например, PHP), вы гуглите ваш вопрос или проблему, и почти в 100% случаев вы найдете ответ 5-летней давности на Stack Overflow, или полноценное обсуждение в [документации](http://docs.php.net/docs.php) (тщательной, в значительной степени прокомментированной и беспрецедентной).

Но всё не так с современным JavaScript. Я обнаружила, что продираюсь через комментарии к открытым проблемам в GitHub и сквозь исходный код только для поиска информации, несколько противоречащей устаревшей документации (более чем в одном пункте). Разбор репозиториев GitHub - часть изучения и использования различных JavaScript пакетов, а для старого человека, подобного мне, работа, близкая к острию прогресса, может сбивать с толку.

## Перегруженность инструментами
Еще одна трудная вещь в изучении JavaScript в 2017 году: установка будет выглядеть так, как будто вы собираете приложение. Простого перечисления инструментов и плагинов, пакетов и зависимостей, настроек редактора и сборщика, необходимых для того, чтобы сделать всё это «правильным способом», достаточно, чтобы остановить вас до того, как вы начнете.

<blockquote class="twitter-tweet" data-conversation="none" data-lang="ru"><p lang="en" dir="ltr">Okay, I am ready to start coding now. <a href="https://t.co/VcwlbNAVkG">pic.twitter.com/VcwlbNAVkG</a></p>&mdash; Matt Jacobs (@capndesign) <a href="https://twitter.com/capndesign/status/832638513048850433">17 февраля 2017 г.</a></blockquote>

*Не позволяйте этому остановить вас.* Мне пришлось отказаться от «правильного пути» с самого начала, и я позволила себе переборщить с использованием неоптимальных или просто любительских настроек только для того, чтобы освоиться с отдельными инструментами. (Позвольте мне рассказать вам о том времени, когда я использовала [nodemon](https://nodemon.io), чтобы сделать свой линтинг...) Позже я находила лучшие способы и включала, что могла и когда могла, в каждый новый проект.

В мире JS предстоит большая работа. Опять же, эта область современного JavaScript — постоянно движущаяся мишень, но мои близкие дружественные разработчики на современном JavaScript говорят мне, что вот [этот урок  от Jonathan Verrecchia](https://github.com/verekia/js-stack-from-scratch) в настоящее время является подробным руководством по созданию современного стека JavaScript. На данный момент.

[Пошаговое руководство по созданию современного JavaScript стека](https://github.com/verekia/js-stack-from-scratch)

## Учебник / Проект / Бросьте его / Повторите
Когда вы изучаете любой новый язык, вы пишете код, чтобы затем его выбросить, а потом написать еще. Мое современное обучение JavaScript было шагом на пути к учебникам, затем - небольшой легко решаемый проект, в ходе которого я составила список вопросов и проблем, а затем - встреча с моими коллегами для получения ответов и объяснений. Дальше: больше учебников, чуть больший проект, больше вопросов, встреча - стирка, полоскание, повторение.

Вот неполный список некоторых семинаров и учебников, с которыми я столкнулась в этом процессе.

\* [HOW-TO-NPM](https://github.com/workshopper/how-to-npm) — npm это менеджер пакетов для JavaScript. Несмотря на то, что я тысячи раз вводила `npm`, прежде чем начала этот процесс, я не знала всех вещей, которые делает npm, пока я не завершила этот интерактивный семинар. (В некоторых проектах я перешла на использование yarn вместо npm, но все концепции сохранились.)

![npm i -g how-to-npm](https://cdn-images-1.medium.com/max/800/1*0NydvP4xLtp13z_HE2Xqyw.png)

\* [learnyounode](https://github.com/workshopper/learnyounode) — я решила сосредоточиться на серверном JavaScript, потому что там мне комфортно, так что мой выбор Node.js. Learnyounode это интерактивное введение в Node.js, аналогичное по структуре how-to-npm.

\* [expressworks](https://github.com/azat-co/expressworks) — подобно двум предыдущим воркшопам, Expressworks представляет собой введение в Express.js, веб-фреймворк для Node.js. Express особо не используется у нас в Postlight, но стоило изучить его как новичок, изучающий построение простого веб-приложения.

\* Теперь пришло время создать что-то реальное. Я нашла учебник Tomomi Imura [«Создание Slack Command Bot с помощью Scratch и Node.js»](http://www.girliemac.com/blog/2016/10/24/slack-command-bot-nodejs/), и мне было достаточно Node и Express чтобы применить мои новообретенные навыки. Поскольку я сфокусировалась на бэкэнде, создание слэш-команды для Slack было хорошей отправной точкой, потому что в данном случае не нужно думать о фронтенде (Slack сделает это для вас).

\* В процессе создания этой команды вместо использования ngrok или Heroku, как рекомендовано в пошаговом руководстве, я экспериментировала с [Zeit Now](https://zeit.co/now), являющемся бесценным инструментом для тех, кто хочет быстро запускать одноразовые JS-приложения.

\* Как только я начала писать настоящий код, я также начала падать в кроличью нору инструментов разработки. Установка Sublime плагинов, выбор правильной [версии Node](https://github.com/postlight/lux/blob/master/CONTRIBUTING.md#nodejs-version-requirements), настройка ESLint с помощью [стилей Airbnb (предпочтение Postlight)](https://github.com/airbnb/javascript) - все это замедляло меня, но всё же стоило первоначальных инвестиций. Я все еще в гуще этого, например, Webpack по-прежнему довольно загадочен для меня, но [это видео — отличное введение](https://www.youtube.com/watch?v=WQue1AN93YU).

\* В какой-то момент асинхронное выполнение JS (в частности, «[callback hell](http://callbackhell.com/)») начало покусывать меня. [«Промисы — это не больно»](https://github.com/stevekane/promise-it-wont-hurt) — это еще один семинар, который учит, как писать «чистый» асинхронный код, используя промисы, относительно новую абстракцию JS для работы с асинхронным исполнением кода. По правде говоря, промисы чуть не сломали меня — это настоящее смещение парадигмы мышления. Спасибо [Mariko Kosaka](http://kosamari.com/notes/the-promise-of-a-burger-party), теперь я думаю о них всякий раз, когда заказываю бургер.

![burger.resolve() — image via The Promise of a Burger Party.](https://cdn-images-1.medium.com/max/800/1*Gh5Pv0ujTuikxGZMeANfCg.png)

Дальше я поняла, что могу ввязаться во всевозможные неприятности, такие как эксперимент с [Jest](https://facebook.github.io/jest/) для тестирования, [Botkit](https://github.com/howdyai/botkit) для более интересного Slack-бота и [Serverless](https://serverless.com/) для того, чтобы действительно осознать ценность функционального программирования. Если вы не знаете, что это значит, это нормально. Это большой мир, и все мы идём по нему собственными путями.

## “Сначала сделайте это, затем сделайте это правильно, затем сделайте это лучше.”
В конечном счете, самое важное, что я должна была помнить: это обучение. Получается плохо? Это всё ещё обучение.

[Изучение современного JavaScript в наши дни](https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f#.kclvczou2) может показаться бесполезным упражнением в WTF (*"what the fuck?", пр. пер.*). Для тех моментов, когда вы задаетесь вопросом, не упустили ли вы свое призвание стать бариста, [Addy Osmani из Google даёт правильный совет](https://medium.com/@addyosmani/totally-get-your-frustration-ea11adf237e3#.t599ja0j3):

*Я призываю людей принять следующий подход к разработке, чтобы идти в ногу с экосистемой JavaScript: сначала сделайте это, затем сделайте это правильно, затем сделайте это лучше. [...]*

*Для овладения основами любой новой темы требуется время, эксперимент и навыки. Начинающие не должны чувствовать, что они терпят неудачу, если они не используют библиотеку "du jour" (фр. "библиотека дня", пр. пер.) или реактивный паттерн недели. Мне потребовалось несколько недель, чтобы начать правильно использовать Babel и React. Дольше, чтобы понять Isomorphic JS, WebPack и все другие библиотеки вокруг него. Начните с простого и постройте свои знания на базе этого.*

Спасибо [NodeSchool](https://nodeschool.io/) и [Free Code Camp](https://www.freecodecamp.com/), двум фантастическим ресурсам для тех, кто начинает изучать JavaScript.

- - - -

*Читайте нас на [Медиуме](https://medium.com/devschacht), контрибьютьте на [Гитхабе](https://github.com/devSchacht), общайтесь в [группе Телеграма](https://t.me/devSchacht), следите в [Твиттере](https://twitter.com/DevSchacht) и [канале Телеграма](https://t.me/devSchachtChannel), рекомендуйте в [VK](https://vk.com/devschacht) и [Facebook](https://www.facebook.com/devSchacht). Скоро подъедет подкаст, не теряйтесь.*

[Статья на Medium](https://medium.com/devschacht/modern-javascript-for-ancient-web-developers-e601e59e87a2)