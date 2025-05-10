<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Тесты по уходу за кожей</title>
  <style>
    body {
      background-color: #fff0f5;
      font-family: Arial, sans-serif;
      padding: 40px;
      line-height: 1.6;
    }
    h1 {
      color: #d63384;
    }
    form {
      font-size: 18px;
      margin-bottom: 30px;
    }
    label {
      display: block;
      margin-top: 10px;
      padding: 4px;
      border-radius: 5px;
    }
    button {
      background-color: #ffb6c1;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 20px;
    }
    a {
      display: inline-block;
      margin-top: 30px;
      text-decoration: none;
      background-color: #ffb6c1;
      padding: 10px 20px;
      border-radius: 8px;
      color: #000;
    }
  </style>
  <script>
    const correctAnswers = {
      q1: null,
      q2: 'Гидрофильное масло',
      q3: 'PHA',
      q4: 'Каждые 2–3 часа',
      q5: 'Центелла азиатская',
      q6: 'После сыворотки',
      q7: 'Это может вызвать раздражение и повреждение кожи',
      q8: 'Хроническое воспалительное заболевание кожи',
      q9: 'Мягкие отшелушивающие ферменты',
      q10: 'Утром — витамин C, вечером — ниацинамид',
      q11: 'PHA и LHA',
      q12: 'Увлажняют и решают конкретные задачи (пигментация, акне, возраст)',
      q13: 'Гликолевая и молочная кислоты',
      q14: 'Выходить на солнце без защиты',
      q15: 'Пантенол',
      q16: 'Витамин C',
      q17: 'Ниацинамид',
      q18: 'Жирная',
      q19: 'Диоксид титана',
      q20: 'Фактор защиты от солнца',
      q21: 'Стимулирует обновление клеток',
      q22: 'Только вечером',
      q23: 'Салициловая',
      q24: 'Центеллу и азелаиновую кислоту',
      q25: 'PHA',
      q26: 'Фруктовые ферменты',
      q27: 'Витамин C',
      q28: 'Ниацинамид',
      q29: 'Три и более',
      q30: 'Глубоко увлажняет',
      q31: 'Пантенол',
      q32: 'Витамин C',
      q33: 'Центелла',
      q34: 'Восстанавливает pH и подготавливает кожу',
      q35: 'Гиалуроновая кислота, алоэ',
      q36: 'Пудра или спрей',
      q37: 'Диоксид титана',
      q38: 'Может закупорить поры',
      q39: 'Салициловая кислота',
      q40: 'Сыворотка — крем — SPF'
    };

    function checkAnswers(event) {
      event.preventDefault();
      let score = 0;
      for (const [question, correct] of Object.entries(correctAnswers)) {
        const options = document.querySelectorAll(`input[name="${question}"]`);
        options.forEach(option => {
          const label = option.closest('label');
          label.style.backgroundColor = '';
          if (option.nextSibling.nodeValue.trim() === correct) {
            label.style.backgroundColor = '#c1f0c1';
          }
          if (option.checked && option.nextSibling.nodeValue.trim() !== correct) {
            label.style.backgroundColor = '#f7bcbc';
          }
          if (option.checked && option.nextSibling.nodeValue.trim() === correct) {
            score++;
          }
        });
      }
      alert(`Ваш результат: ${score} из 40`);
    }
  </script>
</head>
<body>
  <h1>Тест по уходу за кожей</h1>
  <form onsubmit="checkAnswers(event)">
    <!-- Вопросы 1–40 добавлены здесь (сокращено для вывода) -->
    <!-- ... -->
    <button type="submit">Проверить ответы</button>
  </form>
  <a href="index.html">⬅ Назад на главную</a>
</body>
</html>
