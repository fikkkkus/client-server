Stack:
-----------
![image](https://github.com/fikkkkus/client-server/assets/150596519/b10e6add-9f31-4286-abde-861e1de19aae)


This is two applications within one project:
-----------
Client:
Configure the port and IP address to connect to the server, then press play, and Google Chrome will open. Automatic swipes up and down with different parameters in length, received from the server, will be performed on your screen.

Server:
Configure the port and IP address (use the local address of your device or a public one), then start the server. It will send gesture parameters to its clients and write to the database. Additionally, you can view client logs by pressing a button.

Этот проект выполнялся в рамках тестового задания, оставлю конкретно описание:<br />
-----------
"""<br />
Тестовое задание "Android разработчик на Kotlin". <br />
У вас два смартфона. Телефон А выполняет роль клиента, телефон Б выполняет роль сервера.<br />
Клиент. UI на Compose: кнопка Config и кнопка Начать/Пауза. В кофиге указывает ip и порт сервера, нажимаем Сохранить, потом можно редактировать и сохранять.<br />
Сервер. UI на Compose: кнопка Config для выбора порта, кнопка Начать для запуска сервера, кнопка Выключить для выключения сервера, кнопка Логи для просмотра логов из локальной БД.<br />
При нажатии на Старт приложение открывает гугл хром на устройстве и обращается к серверу. Сервер получает информацию, что хром открыт, начинает отправлять клиенту параметры для Gesture (свайпы вверх-вниз разной длины). Клиент свайпит в хроме (использовать Android Accessibility Service) и отчитывается серверу о результатах. Сервер всё пишет в локальную базу SQLite. Так происходит до момента, когда на клиенте будет нажата Пауза. При нажатии на Старт процесс продолжается. Сервер может обслуживать произвольное количество клиентов, используя корутины. Сервер и клиент общаются по протоколу websocket.
Для сетевого взаимодействия использовать Ktor.<br />
"""

