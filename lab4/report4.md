University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://)  
Year: 2025/2026  
Group: U4125  
Author: Lastovskaia Anna Alexandrovna  
Lab: Lab4  
Date of create: 04.05.2026  
Date of finished:   

## Разработка инфраструктуры MVP AI приложения

### AI-ассистент “Ничто не забыто”  
Приложение, которое помогает человеку снизить стресс от "внезапно" навалившихся дел:
- продление документов (паспорта, визы, страховки)
- контроль подписок (Netflix, SaaS, спортзал)
- договоры (аренда, кредиты)
- регулярные задачи (налоги, медосмотры)

AI-функции:
- извлечение данных из документов (OCR + NLP)
- автоматическое определение сроков действия
- умные напоминания 
- чат-интерфейс
### Stage 1 — MVP (до 500 пользователей)

#### Пользователь
- регистрация и авторизация  
- просмотр личного кабинета  


#### Внутренняя подписка (бесплатный тариф с ограничениями)
- до 3 документов  
- до 3 подписок  

#### Документы
- загрузка документов (PDF, изображения)  
- хранение метаданных (дата истечения, тип)  

#### Подписки
- добавление внешних подписок (например, Netflix, аренда)  
- контроль сроков оплаты и продления  

#### Уведомления
- push-уведомления о скором окончании подписок  
- еженедельные напоминания  

##### Общая архитектура (логика потоков)

- Пользователь отправляет запрос с мобильного приложения  
- Cloud Run (монолит) обрабатывает запрос  
- Данные сохраняются в Cloud SQL  
- Файлы загружаются в Cloud Storage  
- Cloud Scheduler запускает проверку событий  
- Cloud Tasks передаёт задачи уведомлений  
- Firebase Cloud Messaging отправляет push-уведомления на устройство

<img width="751" height="404" alt="image" src="https://github.com/user-attachments/assets/a820c50e-026d-412e-9e83-874cfa7d6129" />

### Stage 2 — тест (1000 - 10000 пользователей)
Основные изменения в функционале приложения:  

#### AI функционал
- извлечение текста (OCR)
- поиск ключевых данных

#### Документы
- асинхронная обработка

#### Аналитика
- базовая статистика пользователя (подписки, расходы, лимиты)
- накопление событий для дальнейшей аналитики

##### Общая архитектура 

#### AI Processing Service
- Google Cloud Vision API
- Document AI

#### Очереди и события
- внедрение Cloud Pub/Sub или расширенного Cloud Tasks
- обработка событий (создание подписки, истечение, загрузка документа)

#### Обработка файлов
- фоновые воркеры (Cloud Run Jobs / Cloud Functions)
- предварительная обработка документов

#### Мониторинг
- подготовка данных для аналитики (BigQuery)
<img width="749" height="471" alt="image" src="https://github.com/user-attachments/assets/e17cc0f9-bdf1-4039-aed0-7820ed00a8b5" />

   
### Stage 3 - Production (от 10000 пользователей) 
В инфраструктуру добавлены:
- API Gateway
- GKE для управления микросервисами
- кластер БД
 <img width="810" height="472" alt="image" src="https://github.com/user-attachments/assets/6e3d69ea-0faa-4e0a-bcdb-4b501b21b36f" />
 
### Экономическая модель
### Stage 1 — MVP
Total estimated cost    
$627.22 / month  
<img width="368" height="324" alt="image" src="https://github.com/user-attachments/assets/8e2f8aa4-d4bd-4379-9e5b-0556d027a882" />

<img width="350" height="231" alt="image" src="https://github.com/user-attachments/assets/9c5e80fd-dba0-439b-9365-a7d39e9ee9e4" />

### Stage 2 — тест 
Total estimated cost  
$1,730.25/ mo  
Добавлены:  
AI & ML $799.25  
Data Analytics (Pub/Sub)  $303.78  

### Stage 3 - Production
Total estimated cost  
$3,391.78/ mo  
https://cloud.google.com/products/calculator?dl=CjhDaVExWkROaVptUmlNUzB3T0RJM0xUUTBOek10WWpJMVl5MWpNV1pqWmpNek5UWXlPR1VRQVE9PRAJGiQ2NDNFNkNEQy1CQ0Y2LTRBNjItOUNCNi1CRTU2NjQzRDJBMDU  
Добавлены:  
Compute  $1,551.64
GKE (Kubernetes Engine)  $586.64  
Apigee  $965.00  
Databases (x2)  $287.46  
Storage (5 TiB)  $102.40   



### Обоснование 
