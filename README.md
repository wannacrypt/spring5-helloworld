1. Чтобы скачать проект запускаем команду:  
   `git clone https://github.com/wannacrypt/spring5-helloworld.git`
   
2. Заходим в папку:  
    *spring5-helloworld*

3. Запускаем команду:  
    `./mvnw spring-boot:run`

4. Ждём когда запуститься сервер. После запуска сервера заходим в браузере по адресу:  
    `http://localhost:8080`

5. Нажимаем на кнопку **Get Message**. И видим результат.

6. Меняем сообщение в базе данных так:
    1. Открываем новую страницу и вводим следующий адрес:  
    `http://localhost:8080/h2-console`
        - Убедитесь, что в качестве **JDBC URL** используется `jdbc:h2:mem:testdb`.
    2. Нажимаем на кнопку **Connect**.
    3. В поле **SQL statement** вводим следующий запрос:  
        `UPDATE message SET message = '...' WHERE id = 1` *(вместо трех точек пишем сообщение которое хотим увидеть при нажатий на кнопку **Get Message**)*
    4. Нажимаем на кнопку **Run**.
7. Еще раз нажимаем на кнопку **Get Message** и смотрим что сообщение обновилось.