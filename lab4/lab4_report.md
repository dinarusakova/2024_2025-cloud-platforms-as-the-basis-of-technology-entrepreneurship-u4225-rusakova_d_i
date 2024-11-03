University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FTMI](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://)  
Year: 2024/2025  
Group: U4225  
Author: Rusakova Dinara Ihabovna  
Lab: Lab4  
Date of create: 3.11.2023  
Date of finished:  


# Лабораторная работа №4 "Разработка инфраструктуры MVP AI приложения."

## Ход работы
## 1 Описание системы
Для выполнения задания возьмем систему Smart Tutor for Kids, это прототип AI-приложения, разработанного для поддержки персонализированного обучения младших школьников в возрасте 6–12 лет. Приложение адаптируется к уровню знаний ребенка, предоставляет индивидуальные рекомендации, интерактивные задания и тесты по таким предметам, как математика, чтение и естественные науки. Приложение будет использовать машинное обучение для анализа прогресса и адаптации материалов к потребностям ребенка, помогая поддерживать интерес и развивать важные навыки.

## 2 Архитектура инфраструктуры инфраструктуры 

1. Google Cloud Storage (GCS):
- Хранение мультимедийных материалов (видео, аудио, изображения, документы).
- Хранение обучающих материалов, созданных пользователями (задания, тесты).
- Организация материалов по категориям и возрастным группам, а также управление доступом к ним.

2. PostgreSQL:
- Профили пользователей (имя, возраст, настройки).
- Прогресс обучения (завершенные уроки, результаты тестов).
- Категории и метаданные для мультимедийных материалов.

3. Google Cloud Functions:
- Функции для обработки событий (загрузка новых материалов или изменение данных).
- Обработка запросов от пользователей для извлечения информации из СУБД.

4. API Gateway:
- Управляет входящими запросами от клиента, аутентификацией, маршрутизацией к нужным сервисам и кэшированием.

5. Google Cloud AI/ML Services:
- Модели машинного обучения для анализа данных о пользователях и предоставления персонализированных рекомендаций.
- Обработка естественного языка (NLP) для понимания и обработки запросов пользователей.

6. Google App Engine (или Google Cloud Run):
- Размещение веб-приложения, которое будет служить интерфейсом для пользователей.
Обработка запросов от фронтенда и взаимодействие с API.

7. Frontend (веб-приложение)
- Интерфейс для детей и родителей.

Схема архитектуры:
![](/lab4/screenshots/lab4_task2.png)

Пример взаимодействия:
1. Ребенок (или родитель) взаимодействует с интерфейсом, отправляя запросы к API Gateway.
2. API Gateway принимает запросы от фронтенда, обрабатывает аутентификацию и маршрутизирует запросы к соответствующим backend-сервисам.
3. Запросы от API Gateway передаются на обработку в Google App Engine или Google Cloud Functions, которые затем взаимодействуют с PostgreSQL.
4. Google Cloud Storage хранит все учебные материалы и медиафайлы. Когда пользователи загружают новые материалы (например, видео или изображения), они сохраняются.
5. Метаданные о загруженных материалах хранятся в СУБД.
6. Модели машинного обучения могут быть вызваны из Google Cloud Functions для анализа данных о пользователях и предоставления персонализированных рекомендаций.
7. После обработки запросов, результаты возвращаются обратно через API Gateway, который отправляет ответ клиенту. Если требуется, возвращаются ссылки на материалы, хранящиеся в Google Storage.

## 3 Экономическая модель
1. Начальное состояние
100-200 активных пользователей, 30,000-150,000 запросов в месяц.
![](/lab4/screenshots/lab4_task3_1.png)

2. Тестирование с партнерами 
500-1000 активных пользователей, 150,000-450,000 запросов в месяц.
![](/lab4/screenshots/lab4_task3_2.png)

3. Продакшн-решение
2000-5000 активных пользователей, 450,000-1,500,000 запросов в месяц.
![](/lab4/screenshots/lab4_task3_3.png)

## Вывод

В ходе выполнения лабораторной работы была разработана архитектура инфраструктуры для проекта Smart Learning Assistant for Kids, предназначенного для создания персонализированного помощника в обучении детей. Все выбранные ресурсы направлены на создание удобного и быстрого интерфейса для пользователей. С учетом предполагаемой нагрузки и количества пользователей была создана структура, способная поддерживать оптимальную работу приложения в различных режимах его функционирования. 



