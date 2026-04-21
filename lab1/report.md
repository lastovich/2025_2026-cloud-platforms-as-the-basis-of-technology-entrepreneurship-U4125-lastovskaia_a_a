University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://)  
Year: 2025/2026
Group: U4125  
Author: Lastovskaia Anna Alexandrovna  
Lab: Lab1  
Date of create: 20.04.2026  
Date of finished:   

## Preparation
Открыли доступ к проекту через Console > принятие прав и выбор региона (Армения)  
## Execution
- Создание сервис аккауната с ролью Storage Adimn  
<img width="1458" height="495" alt="image" src="https://github.com/user-attachments/assets/59ba2175-1908-480c-8efb-81dbd6c4ad2c" />

- Создание VM  
<img width="1424" height="292" alt="image" src="https://github.com/user-attachments/assets/d81a3bfa-2a6f-422e-aeb6-b2621d774eb3" />

- Обнаружила бакет  
<img width="493" height="149" alt="image" src="https://github.com/user-attachments/assets/ad749028-ee5d-47a4-8fcc-9794e65a6f92" />

- Создала папку и загрузила в нее файлы из бакета  
<img width="1034" height="306" alt="image" src="https://github.com/user-attachments/assets/f633537e-ff37-4779-a5ed-9fd0e0226e22" />

- Проверка файлов на VM  
<img width="520" height="87" alt="image" src="https://github.com/user-attachments/assets/37f14f03-e447-4473-b9c9-4aa407389e31" />

- Заменила права аккаунта  
<img width="1256" height="722" alt="image" src="https://github.com/user-attachments/assets/90d9abe6-86c8-4f07-842a-0d1f8cd6e1ba" />

- gsutil остался доступен, пришлось погрузиться в детали взаимодействия аккаунт-gsutil:
  - выяснила, что используется временный access token, но перезагрузить машину не помогло
  - пошла проверять, тот ли аккаунт подключается к машине, и упс..
  <img width="885" height="379" alt="image" src="https://github.com/user-attachments/assets/4f372fe0-97fc-44e6-b657-6703170d1918" />

  - исправила на созданный ранее
  - при запуске VM получила запрос на charge
    <img width="1348" height="336" alt="image" src="https://github.com/user-attachments/assets/71b37bd5-c0f6-4306-9af0-cb633a6fbfbb" />


