
# Практично-лабораторне заняття №9
## Тема: Неперервна доставка
## Мета: ознайомитися з принципами і практиками неперервної доставки, сформувати навички роботи з хмарними сервісами Azure
# Завдання
### 1. Створити Azure App Service у власній підписці Azure  
Створив Web-app  
![image](https://github.com/user-attachments/assets/6cafe15d-d331-4b48-b55c-79b6dd7e7826)  
![image](https://github.com/user-attachments/assets/8434a3b8-21c3-4f77-98bd-338aecd3a187)  
### 2. Створити у Azure Service principal, який буде використовуватись для доступу GitHub до вашої підписки Azure  
Створив principal через bash та отримав credentials
![image](https://github.com/user-attachments/assets/c50274a3-ee5e-492d-a57c-312e6fd7c47b)
### 3. Поверніться до вашого github-репозиторію. Перейдіть в settings -> secrets and variables -> actions, та натисніть New Repository Secret. В полі Name введіть AZURE_CREDENTIALS а в поле Secret скопіюйте повністю вивід команди з пункту 2е. Слідкуйте за тим щоб в кінці секрету на було пробілу або переходу рядка, натисніть Add Secret  
Додав новий secret AZURE_CREDENTIALS
![image](https://github.com/user-attachments/assets/2912d57f-cfd5-461a-bab7-e77db9972421)
### 4. Додати нову job в ваш github workflow, створений на попередньому занятті.  
Додав джобу для деплоя в azure
![image](https://github.com/user-attachments/assets/de92dbc0-87ec-4965-aafa-b3379ad39954)
### 5. Запустіть воркфлоу та пересвідчиться що він завершився успішно.  
Мануально запустив воркфлоу та воркфлоу успішно пройшов  
![image](https://github.com/user-attachments/assets/8da651dc-f303-4b7b-8a6b-ed42cc29ec48)
### 6. В логах степу Deploy to Azure Web App знайдіть рядок який починається з App Service Application Url та клікніть по посиланню. Ви маєте побачити веб сторінку з Вашим фронт-ендом. Якщо сторінку не видно – почекайте кілька хвилин та поверніться  
Сайт запустився
![image](https://github.com/user-attachments/assets/7f7544f1-2569-4997-8f5f-7d99f3cb7ef9)

# Висновок
Під час виконання практично-лабораторної роботи було створено Azure App Service та налаштовано автоматичне розгортання застосунку через GitHub Actions. Для цього було створено ресурсну групу, App Service, згенеровано облікові дані service principal та додано їх як секрет у репозиторій GitHub. У наявний workflow було додано нову job з логіном у Azure та деплоєм Docker-образу до App Service.
Після запуску workflow процес виконання пройшов успішно. Додаток було розгорнуто, і сайт відкрився за вказаною URL-адресою.
