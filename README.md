<!DOCTYPE html><html lang="uk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ACASOM ROC-6</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #fdfdfd;
      color: #1a1a1a;
    }
    header {
      padding: 40px 20px;
      text-align: center;
      background: #fff;
    }
    header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }
    .images {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 20px;
    }
    .images img {
      width: 300px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .specs {
      max-width: 800px;
      margin: auto;
      padding: 20px;
      font-size: 1.1rem;
      line-height: 1.6;
    }
    .cta {
      text-align: center;
      margin: 30px 0;
    }
    .cta a {
      display: inline-block;
      background-color: #1f4fe2;
      color: white;
      padding: 14px 28px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
    }
    .form-section {
      background: #f3f3f3;
      padding: 30px;
    }
    .form-section form {
      max-width: 600px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    .form-section input, .form-section textarea {
      padding: 12px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 1rem;
    }
    .form-section button {
      background: #1f4fe2;
      color: white;
      border: none;
      padding: 12px;
      font-size: 1rem;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>ACASOM ROC-6</h1>
    <p>твоя перевага у повітрі</p>
  </header>
  <section class="images">
    <img src="https://i.imgur.com/1E0s8yy.jpg" alt="ROC-6 Front" />
    <img src="https://i.imgur.com/6gfOYwN.jpg" alt="ROC-6 Back" />
  </section>
  <section class="specs">
    <p><strong>Частоти:</strong> 2.4G / 5.2G / 5.8G</p>
    <p><strong>Потужність:</strong> 2x10W, вихід до 20W</p>
    <p><strong>Підтримка дронів:</strong> DJI, Autel, Parrot</p>
    <p><strong>Акумулятор:</strong> 7.4V, 5000mAh</p>
    <p><strong>Час роботи:</strong> до 6 годин</p>
    <p><strong>Водозахист:</strong> так, корпус захищений</p>
    <p><strong>Покращення сигналу:</strong> до 8 разів у порівнянні з базовою антеною</p>
  </section>
  <div class="cta">
    <a href="https://www.instagram.com/avenge_ukrainian" target="_blank">Instagram</a>
  </div>
  <section class="form-section">
    <form id="contactForm">
      <input type="text" name="name" placeholder="Ваше ім'я" required>
      <input type="tel" name="phone" placeholder="Номер телефону" required>
      <textarea name="message" placeholder="Повідомлення або питання"></textarea>
      <button type="submit">Замовити</button>
    </form>
  </section>  <script>
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = e.target.name.value;
      const phone = e.target.phone.value;
      const message = e.target.message.value;

      const text = `Нова заявка з сайту:%0A%0AІм'я: ${name}%0AТелефон: ${phone}%0AПовідомлення: ${message}`;
      const telegramURL = `https://api.telegram.org/bot7525034641:AAEr25RRg_VQQ48eJ_vXdq8rDqPeZjmS02w/sendMessage?chat_id=@Vovk_Andri&text=${text}`;

      fetch(telegramURL)
        .then(response => {
          if (response.ok) {
            alert('Заявку надіслано! Очікуйте на відповідь у Telegram.');
            e.target.reset();
          } else {
            alert('Помилка при відправленні. Спробуйте пізніше.');
          }
        });
    });
  </script></body>
</html>