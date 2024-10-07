<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Пожежна безпека</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .slide {
            display: none;
            padding: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin: 20px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .active {
            display: block;
        }
        h1, h2 {
            color: #333;
        }
        button {
            padding: 10px 20px;
            margin: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

    <div class="slide active">
        <h1>Пожежна безпека</h1>
        <h2>Як уникнути та діяти під час пожежі</h2>
    </div>

    <div class="slide">
        <h2>Цілі презентації</h2>
        <ul>
            <li>Ознайомити з основними причинами виникнення пожеж.</li>
            <li>Навчити правилам поведінки під час пожежі.</li>
            <li>Показати правильне використання засобів пожежогасіння.</li>
            <li>Розглянути плани евакуації та першу допомогу.</li>
        </ul>
    </div>

    <div class="slide">
        <h2>Основні причини виникнення пожеж</h2>
        <ul>
            <li>Неправильне використання електроприладів – перевантаження мережі, несправні прилади.</li>
            <li>Небезпека від відкритого вогню – сірники, свічки, вогонь без нагляду.</li>
            <li>Куріння в недозволених місцях – кинуті недопалки.</li>
            <li>Неправильне зберігання легкозаймистих речовин – бензин, газ та інші горючі матеріали.</li>
        </ul>
    </div>

    <div class="slide">
        <h2>Правила поведінки під час пожежі</h2>
        <ol>
            <li><strong>Зберігайте спокій</strong> – уникайте паніки.</li>
            <li><strong>Повідомте про пожежу</strong> – викличте рятувальників за номером 101.</li>
            <li><strong>Евакуація</strong> – швидко покидайте будівлю, не користуючись ліфтом.</li>
            <li><strong>Захист від диму</strong> – прикривайте рот і ніс вологою тканиною.</li>
            <li><strong>Допомога іншим</strong> – допоможіть дітям, літнім людям і тим, хто потребує підтримки.</li>
        </ol>
    </div>

    <div class="slide">
        <h2>Евакуація та використання вогнегасників</h2>
        <ul>
            <li>Дотримуйтесь плану евакуації.</li>
            <li>Не відкривайте двері, якщо вони гарячі.</li>
            <li>Використовуйте вогнегасник, якщо це безпечно.</li>
        </ul>
    </div>

    <div class="slide">
        <h2>Підсумок</h2>
        <p>Пожежна безпека – це відповідальність кожного. Знання правил і дій під час пожежі допоможуть зберегти життя та здоров'я.</p>
    </div>

    <button id="prev">Назад</button>
    <button id="next">Далі</button>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');

        document.getElementById('next').addEventListener('click', () => {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        });

        document.getElementById('prev').addEventListener('click', () => {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide - 1 + slides.length) % slides.length;
            slides[currentSlide].classList.add('active');
        });
    </script>

</body>
</html>
