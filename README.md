# Strimco test task

Використані інструменти: Make.com (замість Pipedreams), Insomnia (замість Postman), Google Looker Studio, Google Forms, Google Sheets.

## Реалізовані юзкейси:
#### 1) Реєстрація
Реєстрація відбувається через google форму, що доступна за цим [посиланням](https://forms.gle/XaqqFu3t8xHJLMBD6). Важливо зауважати, що через певні ліміти безкоштовного акаунта Make.com повідомлення на пошту може прийти із затримкою до 15 хв. 
Приклад емейлу після реєстрації:</br> ![image](https://github.com/user-attachments/assets/548a8c22-807a-4cd7-9c06-d9286e3ccaca).

#### 2) Парсинг фільмів
Є можливість відправити запит на вказану адресу - https://hook.eu2.make.com/bm2gfobl5x297pwyo1ibfbed427uj98f щоб почати процес парсингу.

Приклад запиту:</br> ![image](https://github.com/user-attachments/assets/48810802-f9c2-404d-a2f9-073ae3dd98d5) </br>
Приклад відповіді:</br> ![image](https://github.com/user-attachments/assets/c2240699-c77b-4bf0-9a92-e165989bcb20) </br>
Після обробки запиту відправляється відповідний емейл, його приклад:</br> ![image](https://github.com/user-attachments/assets/0a3e3115-8cea-46a7-858d-7b59cc90f62b) </br>
Скріншот того як виглядає google таблиця, що зберігає дані:</br> ![image](https://github.com/user-attachments/assets/a16ce0ff-ccdb-4d59-8043-3b620750c5ba)

#### 3) Візуалізація
Візуалізація у Google Looker Studio із всіма вказаними фільтрами доступна за наступним [посиланням](https://lookerstudio.google.com/reporting/9506afaa-e6d8-4b67-bd7e-77168145867e).
Скріншот репорту:</br> ![image](https://github.com/user-attachments/assets/0a833c43-fa1e-4c13-be97-2effa2032c2b)


## Архітектура
На платформі Make.com було створено 2 сценарія, що опрацьовують 2 з 3 юзкейсів.
#### registration-handler
Скріншот флоу, що опрацьовує реєстрація, із пояснювальними коментарями:</br>
![image](https://github.com/user-attachments/assets/2bdea72a-0bf7-4703-8bde-22bfffe46bb9)

#### api-handler
Перший скріншот з флоу. Валідує вхідні дані: </br> ![image](https://github.com/user-attachments/assets/d1767f05-f003-4b77-bcce-0fdd539c3063) </br>
Другий скріншот з флоу. Опрацьовує сам запит і робить всі потрібні речі: </br> ![image](https://github.com/user-attachments/assets/83902432-0807-49dc-8128-74f6deeef883)
