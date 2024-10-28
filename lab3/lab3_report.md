University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FTMI](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://)  
Year: 2024/2025  
Group: U4225  
Author: Rusakova Dinara Ihabovna  
Lab: Lab3  
Date of create: 28.10.2023  
Date of finished: 


# Лабораторная работа №3 "Исследование Cloud Storage"


## Введение 

Cloud Storage — это облачный сервис от Google Cloud Platform (GCP), предоставляющий инфраструктуру для хранения и управления данными в интернете. Он позволяет загружать, хранить и организовывать различные типы данных — от текстовых файлов до мультимедиа — и предоставляет гибкий доступ к этим данным через интернет.

## Задание 1 
Создадим Cloud Storage bucket. 
Cloud Storage bucket — это контейнер для хранения данных в облаке Google Cloud Platform (GCP). Он служит как единица организации и управления данными, что позволяет пользователю загружать, хранить, организовывать и контролировать доступ к файлам различных типов и размеров. Фактически, бакет можно представить как папку в облаке, которая вмещает файлы (или "объекты") и предоставляет к ним безопасный доступ.
![](/lab1/screenshots/lab3_task1.png)

## Задание 2
Загрузим 3 изображения в Cloud Storage bucket.
![](/lab1/screenshots/lab3_task2.png)

## Задание 3 
Создадим папку с названием images и переместить файлы туда в пределах бакета.
![](/lab1/screenshots/lab3_task3_2.png)
![](/lab1/screenshots/lab3_task3_3.png)
Успешно перемешено.

## Задание 4
Настроим публичный доступ для ваших файлов в настройках приватности. В данном случае сделаем публичные доступ для всего бакета.
![](/lab1/screenshots/lab3_task4.png)
![](/lab1/screenshots/lab3_task4_2.png)
Как мы видим доступ открыт всем пользователям в интернете. 

## Задание 5 
Создадим ссылки на ваши файлов через контекстное меню файла.
Public URL:
1. https://storage.googleapis.com/rusakova-bucket-1/images/IMG_0978.jpeg
2. https://storage.googleapis.com/rusakova-bucket-1/images/IMG_0979.jpeg
3. https://storage.googleapis.com/rusakova-bucket-1/images/IMG_5213.jpeg
Увидеть изображение может любой пользователь. 

## Выво
В ходе лабораторной работы было изучение создание Cloud Storage bucket. Была создана директория images и загружены три файла. Также были изменены права доступа для бакета, в следствие чего публичная ссылка на файлы, содержащиеся в бакете, доступна любому пользователю.







