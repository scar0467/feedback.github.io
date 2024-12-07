<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Оставить отзыв</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f9;
        }
        form {
            max-width: 500px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #333;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #555;
        }
    </style>
</head>
<body>

<h1>Оставить отзыв</h1>
<form id="feedbackForm">
    <label for="name">Ваше имя:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Ваш email:</label>
    <input type="email" id="email" name="email" required>

    <label for="message">Ваш отзыв:</label>
    <textarea id="message" name="message" rows="4" required></textarea>

    <button type="submit">Отправить</button>
</form>

<script>
    document.getElementById('feedbackForm').addEventListener('submit', function(e) {
        e.preventDefault();
        
        const name = document.getElementById('name').value;
        const email = document.getElementById('email').value;
        const message = document.getElementById('message').value;

        console.log("Отзыв отправлен:", { name, email, message });

        // Здесь вы можете добавить код для отправки формы на сервер
        alert('Спасибо за ваш отзыв!');
        e.target.reset();
    });
</script>

</body>
</html>
