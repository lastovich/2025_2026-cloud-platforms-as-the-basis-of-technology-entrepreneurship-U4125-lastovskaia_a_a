University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Cloud platforms as the basis of technology entrepreneurship](https://)  
Year: 2025/2026  
Group: U4125  
Author: Lastovskaia Anna Alexandrovna  
Lab: Lab3  
Date of create: 04.05.2026  
Date of finished:   

## Исследование Cloud Storage
1. Создание бакета
- [x] Региональный бакет - дешевле  
- [x] краткосрочного хранения (Standard) - дешевле   
- [x] без Data protection - нет необходимости следить за ретеншеном  
- [x] с отключенным Enforce public access prevention on this bucket, иначе не выйдет выполнить задание  
 
2. Укладывание файлов в папку внутри бакета
<img width="1062" height="453" alt="image" src="https://github.com/user-attachments/assets/96fd16aa-fede-4ea1-9253-a1a65accab5c" />

3. Внешний доступ к файлам
   - Попытка открыть файл по внешней URL не увенчалась успехом
     <img width="1906" height="297" alt="image" src="https://github.com/user-attachments/assets/d6f1010d-838c-42e2-bd3a-6e496e2834b9" />
   - Добавила в правах доступа allUsers → Storage Object Viewer
    <img width="1518" height="336" alt="image" src="https://github.com/user-attachments/assets/ebbe0d82-6c0a-4a9b-bb18-b4648290c230" />

   - Успех
     <img width="1292" height="892" alt="image" src="https://github.com/user-attachments/assets/d659eb61-c43d-4c46-9724-11b46f1c6136" />

 
