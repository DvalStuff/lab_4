# lab_4
# Розробка додатку для візуалізації вимірювань радару

Мета роботи:

Розробити додаток, який зчитує дані з емульованої вимірювальної частини радару,
наданої у вигляді Docker image, та відображає задетектовані цілі на графіку в полярних
координатах.

![Image alt](screenshots/1.png)

Основні функції сторінки:

1. На сторінці є графік, який оновлюється в режимі реального часу. Він показує відстань до цілі та її потужність на полярному графіку.

2. Встановлюється з'єднання з WebSocket-сервером (ws://localhost:4000) для отримання даних радару. При отриманні нових даних вони обробляються і відображаються на графіку. Колір цілі змінюється в залежності від потужності, відображається згідно шкали.

3. Форма, яка дозволяє користувачу змінювати налаштування радару, такі як кількість вимірювань за оберт, швидкість обертання та швидкість цілі.

4. При натисканні кнопки "Оновити налаштування" дані з форми відправляються на сервер через HTTP-запит (PUT на http://localhost:4000/config) для оновлення параметрів радару.
