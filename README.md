<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Квест для сестры</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive;
      background-color: #fff0f5;
      text-align: center;
      padding: 50px;
    }
    #game {
      margin-top: 30px;
    }
    .hidden {
      display: none;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #ff69b4;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      color: white;
    }
    input {
      padding: 8px;
      font-size: 16px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    img {
      margin-top: 20px;
      border-radius: 15px;
    }
  </style>
</head>
<body>
  <h1>🎉 С Днём Рождения, сестрёнка! 🎉</h1>
  <p>Добро пожаловать в волшебный квест! Пройди все этапы, чтобы открыть свой сюрприз 🎁</p>

  <div id="game">
    <div id="step1">
      <p>🔍 Загадка 1: Я прихожу раз в год, приношу подарки и торт. Что это?</p>
      <input type="text" id="answer1" placeholder="Твой ответ...">
      <button onclick="checkAnswer1()">Ответить</button>
      <p id="feedback1"></p>
    </div>

    <div id="step2" class="hidden">
      <p>🧠 Загадка 2: Я всегда с тобой, но ты не можешь меня увидеть. Я — это...</p>
      <input type="text" id="answer2" placeholder="Твой ответ...">
      <button onclick="checkAnswer2()">Ответить</button>
      <p id="feedback2"></p>
    </div>

    <div id="step3" class="hidden">
      <p>🎁 Поздравляю! Ты прошла квест! Нажми кнопку, чтобы открыть свой сюрприз:</p>
      <button onclick="showGift()">Открыть подарок</button>
    </div>

    <div id="gift" class="hidden">
      <h2>💖 Ты самая лучшая сестра на свете!</h2>
      <p>Пусть твой день будет наполнен радостью, смехом и волшебством!</p>
      <img src="https://media.giphy.com/media/3o6ZtpxSZbQRRnwCKQ/giphy.gif" alt="Подарок" width="300">
      <h3>🎊 Бонус-сюрприз от Вселенной 🎊</h3>
      <p>Поздравляем! Ты выиграла <strong>1000 долларов</strong> в магической лотерее счастья! 💸</p>
      <p>Получение приза: <em>примерно через... несколько месяцев. 😉</em></p>
      <p>А пока — наслаждайся жизнью!</p>
    </div>
  </div>

  <script>
    function checkAnswer1() {
      const answer = document.getElementById('answer1').value.toLowerCase();
      if (answer.includes('день рождения')) {
        document.getElementById('feedback1').textContent = '✅ Правильно!';
        document.getElementById('step2').classList.remove('hidden');
      } else {
        document.getElementById('feedback1').textContent = '❌ Попробуй ещё!';
      }
    }

    function checkAnswer2() {
      const answer = document.getElementById('answer2').value.toLowerCase();
      if (answer.includes('тень') || answer.includes('мысль')) {
        document.getElementById('feedback2').textContent = '✅ Отлично!';
        document.getElementById('step3').classList.remove('hidden');
      } else {
        document.getElementById('feedback2').textContent = '❌ Не совсем... Подумай ещё!';
      }
    }

    function showGift() {
      document.getElementById('gift').classList.remove('hidden');
    }
  </script>
</body>
</html>
