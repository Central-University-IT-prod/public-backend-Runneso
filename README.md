<b> Ссылка на бота </b> - https://t.me/Travel_Helper_prod_bot

<h1><b>Инструкция по запуску приложения</b></h1><br><p>Достаточно лишь запустить команду <code>docker compose up -d</code>.
Если же хочется запустить проект на другом боте или на другой базе данных, то достаточно поменять переменные окружения в файле <code>.env</code>.
Также можно приобрести платные планы используемых API и поменять ключи в том же файле <code>.env</code>.</p><br>
<h1>Демонстрация работы приложения</h1><br><p>
  
https://github.com/Runneso/NTO1/assets/111322016/a44e8ebb-45d1-4b46-9789-4d6a03c772b8
</p>
<p>
<b>P.S.</b> плохое качество в видео из-за ограничения размера.<br>
Изначально пользователей регистрируется в системе. Позже он может поменять свой возраст, биографию и место жительство в своём профиле.
После регистрации пользователю открывается полный функционал. Создав путешествие, пользователь может управлять друзьями внутри путешествия (только если он автор), создавать и просматривать заметки (если он автор заметки или если она публична), получить картинку
маршрута, посмотреть прогноз погоды во всех пунктах и интересные места в этих пунктах. Также автор может удалить путешествие или изменить данные о нём, поменяв название, даты начала, тип транспорта или добавив новый пукнт в путешествие.
</p>
<h1> 	Описание внешних интеграций</h1><br><p>
<b>TomTomAPI</b> (https://developer.tomtom.com/) - внешний сервис, который помог мне прокладывать маршруты и получать инфраструктуру городов. <br>
<b>OpenWeather</b> (https://openweathermap.org/api) - внешний сервис, который позволил мне получать данные о погоде в населённых пунктах. <br>
<b>GeoPy</b> (https://github.com/geopy/geopy) - библиотека на Python для работы с координатами,именно она была использована вместе с OSM шаблоном. <br>
<b>CurrencyConverter</b> (https://github.com/alexprengere/currencyconverter) - библиотека на Python для конвертации валют, в процессе разработки было принято решение приводить все валюты к доллару, а не к рублю, потому что данные мировых банков давно не обновляли
информацию о курсе российского рубля. <br>
<b>StaticMap</b> (https://github.com/komoot/staticmap) - библиотека на Python для работы с изображением карт, которую я использова для получения изображения маршрута. <br>
<b>Loguru</b> (https://github.com/Delgan/loguru) - библиотека на Python для логирования. <br>
</p>
<h1>Обоснованность выбора технологий</h1>
<b>Python</b> (https://www.python.org/) - данный язык программирования является одним из самых популярных и быстрых для разработки ботов из-за своего простого синтаксиса. Также на данном языке написано огромной количество библиотек, который помогают "не изобретать велосипед". <br>
<b>Aiogram</b> (https://github.com/aiogram/aiogram) - одна из самых мощных асинхронных библиотек на Python для создания телеграмботов, она очень сильно выигрывает всех своих конкурентов. Позволяет интегрировать SQLAlchemy для работы с базой данных и Redis для кэширования данных. <br>
<b>SQLAlchemy</b> (https://github.com/sqlalchemy/sqlalchemy) - одна из самых мощных асинхронных ORM на Python. На данный момент сложно найти, что-то более удобное и универсальное для работы с базами данных на Python. <br>
<b>TomTomAPI</b> - данное API выручало меня несколько раз, я имею опыт разработки именно с использование него. Именно это повлияло на выбор. <br>
<b>OpenWeather</b> - данное API является бесплатным простым способ получить погоду, поэтому было принято решение использовать его. <br>
<b>GeoPy</b> - является удобной надстройкой над несколькими API (среди которых OSM), она легка в использовании. Именно это повлияло на выбор, я понимаю её минусы, однако в рамках олимпиады она идеально выполняет задачу. <br>
<b>StaticMap</b> - использовать данную библиотеку пришлось из-за безысходности, было сложно найти что-то лучше. <br>
<b>Loguru</b> - я считаю её необходимой для любого бота, потому что, когда бот находится на хостинге, очень сложно отслеживать ошибки и баги. <br>
