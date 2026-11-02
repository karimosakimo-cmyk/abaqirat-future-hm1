
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>قسم الألعاب - عباقرة المستقبل</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Tahoma, Arial, sans-serif;
      background: #f4f7ff;
      color: #172554;
    }
    header {
      background: #173b78;
      color: white;
      text-align: center;
      padding: 25px 15px;
    }
    nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 10px;
      padding: 15px;
      background: white;
    }
    nav a {
      color: #173b78;
      text-decoration: none;
      font-weight: bold;
      padding: 10px 15px;
      border-radius: 20px;
      background: #e8efff;
    }
    main {
      max-width: 950px;
      margin: 25px auto;
      padding: 15px;
    }
    h2 { text-align: center; color: #173b78; }
    .games {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 18px;
    }
    .card {
      background: white;
      padding: 22px;
      border-radius: 16px;
      text-align: center;
      box-shadow: 0 4px 15px #00000012;
    }
    .emoji { font-size: 42px; }
    .card h3 { color: #2563eb; }
    .card button {
      background: #2563eb;
      color: white;
      border: 0;
      border-radius: 10px;
      padding: 11px 20px;
      font-size: 16px;
      cursor: pointer;
    }
    #result {
      text-align: center;
      font-size: 20px;
      font-weight: bold;
      margin-top: 20px;
    }
    footer {
      background: #173b78;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 30px;
    }
  </style>
</head>
<body>

<header>
  <h1>🎮 عالم الألعاب</h1>
  <p>العب وتعلم واختبر ذكاءك!</p>
</header>

<nav>
  <a href="index.html">الرئيسية</a>
  <a href="learn.html">التعلم</a>
  <a href="games.html">الألعاب</a>
  <a href="stories.html">القصص</a>
</nav>

<main>
  <h2>🌟 ألعاب ممتعة وذكية</h2>

  <div class="games">
    <div class="card">
      <div class="emoji">🔢</div>
      <h3>تحدي الحساب</h3>
      <p>كم يساوي 5 + 3؟</p>
      <button onclick="checkAnswer(8)">8</button>
      <button onclick="checkAnswer(9)">9</button>
      <button onclick="checkAnswer(7)">7</button>
    </div>

    <div class="card">
      <div class="emoji">🧠</div>
      <h3>اختبر ذكاءك</h3>
      <p>ما هو الشيء الذي له أسنان ولا يعض؟</p>
      <button onclick="checkRiddle('المشط')">المشط</button>
      <button onclick="checkRiddle('الكتاب')">الكتاب</button>
      <button onclick="checkRiddle('القلم')">القلم</button>
    </div>

    <div class="card">
      <div class="emoji">🌍</div>
      <h3>معلومات عامة</h3>
      <p>ما هو الكوكب الأحمر؟</p>
      <button onclick="checkPlanet('المريخ')">المريخ</button>
      <button onclick="checkPlanet('الأرض')">الأرض</button>
      <button onclick="checkPlanet('الزهرة')">الزهرة</button>
    </div>
  </div>

  <div id="result">اختر إجابتك وابدأ اللعب! ⭐</div>
</main>

<footer>
  <p>🌟 عباقرة المستقبل - العلم متعة والمستقبل أمل</p>
</footer>

<script>
  function showResult(correct) {
    document.getElementById("result").textContent =
      correct ? "🎉 أحسنت! إجابة صحيحة." : "حاول مرة أخرى! 💪";
  }

  function checkAnswer(answer) {
    showResult(answer === 8);
  }

  function checkRiddle(answer) {
    showResult(answer === "المشط");
  }

  function checkPlanet(answer) {
    showResult(answer === "المريخ");
  }
</script>

</body>
</html>
