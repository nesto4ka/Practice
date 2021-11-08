Пункт 2 представлен в файлах server.py и client.py 2. Модифицировать простой эхо-сервер таким образом, чтобы при подключении клиента создавался новый поток, в котором происходило взаимодействие с ним. Новые потоки для каждого клиента создаются тут
 ![image](https://user-images.githubusercontent.com/70269164/140776749-4b24afba-1fd5-4a4f-907e-2fb7a7604184.png)

Результат подключения клиентов представлен здесь
 ![image](https://user-images.githubusercontent.com/70269164/140776762-d6809357-9ee2-4d24-91b6-de944086406a.png)

 ![image](https://user-images.githubusercontent.com/70269164/140776777-27f66a13-b02c-454a-b9bf-6c923243a486.png)

 ![image](https://user-images.githubusercontent.com/70269164/140776794-adbdbdb6-9589-4fc2-a201-fcc9e7cf8992.png)

3.	Реализовать простой чат сервер на базе сервера аутентификации. Сервер должен обеспечивать подключение многих пользователей одновременно, отслеживание имен пользователей, поддерживать историю сообщений и пересылку сообщений от каждого пользователя всем остальным. Чат реализован на TCP сокетах О клиентах следующие данные: информация об IP клиента хранится в зашифрованном виде, логин, пароль тоже в зашифрованном виде Они хранятся построчно в csv файле история сообщений хранится в файле .csv Регистрация клиента
 ![image](https://user-images.githubusercontent.com/70269164/140776815-60ff0cc1-0ed9-423e-b106-524750e27a50.png)

Регистрация второго клиента
 ![image](https://user-images.githubusercontent.com/70269164/140776831-be307e1d-17d4-4c00-a7d7-3e639c715561.png)

Файл регистрации теперь выглядит так clients.csv
 
 ![image](https://user-images.githubusercontent.com/70269164/140776845-ee84294f-5f87-4c35-a80b-c44e5b807630.png)

![image](https://user-images.githubusercontent.com/70269164/140776865-295a5e4a-73ee-450a-bf4c-80032efa1b46.png)

Посмотрим что выводит сервер
 ![image](https://user-images.githubusercontent.com/70269164/140776881-baa213c2-59ca-4c8b-8b74-e3ecb2b64bb4.png)

Посмотрим как выглядит переписка у пользователей и сервера
 ![image](https://user-images.githubusercontent.com/70269164/140776899-c9107b7c-8164-48ea-a8e5-3049142b2c42.png)

 ![image](https://user-images.githubusercontent.com/70269164/140776911-8ec28bdd-8b28-4025-a265-c4eb4ccfed11.png)

 ![image](https://user-images.githubusercontent.com/70269164/140776924-bc13d1c1-8b8d-4ea2-ad1d-88e324fc68bf.png)

История сообщений
 ![image](https://user-images.githubusercontent.com/70269164/140776944-f5babc6a-d081-4535-ad33-28a470aaa7c2.png)

4.	Реализовать сервер с управляющим потоком. При создании сервера прослушивание портов происходит в отдельном потоке, а главный поток программы в это время способен принимать команды от пользователя. Необходимо реализовать следующие команды: Отключение сервера (завершение программы) командой shutdown
 ![image](https://user-images.githubusercontent.com/70269164/140776962-198a3b81-d780-443f-ba49-5fd075851947.png)

Пауза (остановка прослушивание порта) командами ключения и отключения stop listen start listen
 ![image](https://user-images.githubusercontent.com/70269164/140776979-122d6448-886e-4ba8-81b1-7d7faae146aa.png)

У клиента ничего не происходит, он ожидает соединения, так как мы запретили подключения Если мы введем start listen то клиент сразу подключится
 ![image](https://user-images.githubusercontent.com/70269164/140776993-604b9659-fdfe-4b34-b640-dd27598694d7.png)

 ![image](https://user-images.githubusercontent.com/70269164/140777002-ee4a7bf2-46b9-43ce-b125-98c8010d4174.png)

Показ логов выключается и включается командами stop log start log
 ![image](https://user-images.githubusercontent.com/70269164/140777012-c8a6baea-3fa7-4613-9cf1-18f38497472a.png)

Очистка логов очищается сам файл логов и консоль командой clear log
 ![image](https://user-images.githubusercontent.com/70269164/140777025-f62135fd-86fb-49e8-9022-dbcab027430d.png)

![image](https://user-images.githubusercontent.com/70269164/140777043-f7a86f8c-2715-4813-95af-e33a94de4e15.png)
 
Очистка файла идентификации выполняется командой clear file
 ![image](https://user-images.githubusercontent.com/70269164/140777064-4801bb9d-4417-43b7-8b00-07d6386fdf33.png)

 ![image](https://user-images.githubusercontent.com/70269164/140777073-42e6a4c6-6243-4199-8fc0-e28b026c442e.png)


