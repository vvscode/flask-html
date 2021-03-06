### Часть 1

1. Распишите роуты, выведите текст:

    - главной / (выведите здесь будет главная)
    - цели /goals/<goal> (выведите здесь будет цель goals)
    - профиля учителя /profiles/<id учителя>/ (выведите здесь будет преподаватель)
    - поиска /search?s=aaaaa (выведите здесь будет поиск)
    - заявки на подбор /request
    - формы бронирования /booking/<id учителя>/

2. Скопируйте мок-данные в JSON-файл

    https://github.com/kushedow/flask-html/blob/master/Project%202/data.py

3. Скачайте или склонируйте репозиторий с шаблонами.

    https://github.com/kushedow/flask-html

Скопируйте шаблоны в вашу папку templates

    – index.html главной
    – goal.html цели
    – search.html подбора
    – profile.html профиль преподавателя
    – request.html заявки на подбор
    – booking.html заявки на бронирование

Скопируйте статику в static

4. Выведите страницу преподавателя

    – изучите мок-данные
    – перенесите данные о преподавателях в JSON-файл
    – отредактируйте шаблон
    – проверьте результат
    – выведите табличку занятости 

5. Реализуйте страницу бронирования с обратной связью

    – изучите мок данные
    – выведите форму, используя данные о преподавателе
    – проверьте результат
    – примите данные через request
    – сохраните данные в JSON файле booking.json
    – выведите сообщение что все успешно
    – проверьте результат

6. Реализуйте страницу запроса подбора

    – выведите форму
    – примите данные через request
    – сохраните данные в JSON файле request.json
    – выведите сообщение что все успешно
    – проверьте результат

7. Реализуйте страницу цели, например, "для переезда"
    
    – отфильтруйте преподавателей по цели 
    – выведите их на странице в порядке убывания рейтинга
    – проверьте результат

8. Выведите главную страницу
    
    – получите 6 случайных преподавателей
    – выведите их на странице 
    – добавьте ссылки на цели
    – проверьте результат
    
    
### Часть 2

Создайте модель Преподаватель

- Установите и подключите SQLAlchemy
- Опишите модель для преподавателя
- Проверьте, что первичный ключ, типы и констрейнты в порядке

Создайте модель Бронирование

- Опишите модель Бронирование
– Свяжите модель отношениями с Преподавателем (one to many)
- Проверьте, что первичный ключ, типы и констрейнты в порядке

Создайте модель Заявка на подбор

- Опишите модель 
- Проверьте, что первичный ключ, типы и констрейнты в порядке


Импортируйте данные

- Напишите скрипт, который запишет мок-данные из JSON в базу
- Запишите данные
- Проверьте, что все заимпортировалось
- Выкиньте файл, он вам больше не понадобится

Доработайте роут преподавателя

- Замените получение данных из файла на выполнение запроса в БД
– Когда преподавателя не существует, выбросьте 404


Доработайте роут цели, например, "для переезда"
    
– получите преподавателей с помощью запроса с фильтром и сортировкой


Доработайте роут главной

- Замените получение данных из файла на выполнение запроса в БД


Доработайте роут и страницу бронирования с обратной связью

– Перепишите форму с помощью WFT Forms
– Валидируйте форму: все поля должны быть заполнены
– Замените запись в файла на запись в базу

Доработайте роут и страницу заявки на подбор

– Перепишите форму с помощью WFT Forms
– Валидируйте форму: все поля должны быть заполнены
– Замените запись в файла на запись в базу

