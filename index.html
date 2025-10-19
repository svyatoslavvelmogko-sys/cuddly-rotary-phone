<!doctype html>
<html lang="ru">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Пример полноэкранного эффекта (этичный)</title>
<style>
  body { font-family: Arial, sans-serif; display:flex; align-items:center; justify-content:center; height:100vh; margin:0; }
  .container { text-align:center; }
  .btn { padding:12px 20px; font-size:16px; cursor:pointer; }
  /* полноэкранный оверлей */
  #overlay {
    position:fixed; inset:0; display:none; align-items:center; justify-content:center;
    background:#000; z-index:9999; color:#fff; flex-direction:column;
  }
  #overlay img { max-width:100%; max-height:100%; object-fit:cover; }
  #overlay .close-hint { position:absolute; top:10px; right:12px; font-size:14px; opacity:0.8; }
</style>
</head>
<body>
  <div class="container">
    <h2>Этичный полноэкранный эффект</h2>
    <p>Нажмите кнопку — вы увидите предупреждение и сможете согласиться или отменить.</p>
    <button id="start" class="btn">Запустить полноэкранный эффект</button>
  </div>

  <!-- Оверлей, который покажется в полноэкране -->
  <div id="overlay">
    <div class="close-hint">Нажмите Esc или кнопку выход, чтобы выйти</div>
    <!-- замените src на своё изображение -->
    <img id="bigImage" src="screamer.jpg" alt="Полноэкранный эффект">
    <button id="exitBtn" class="btn" style="position:absolute;bottom:30px;">Выйти</button>
  </div>

  <!-- Звук (опционально). Загрузите свой scream.mp3 в ту же папку -->
  <audio id="sound" src="scream.mp3" preload="auto"></audio>

<script>
const startBtn = document.getElementById('start');
const overlay = document.getElementById('overlay');
const exitBtn = document.getElementById('exitBtn');
const sound = document.getElementById('sound');

function goFullscreen() {
  const el = document.documentElement;
  if (el.requestFullscreen) return el.requestFullscreen();
  if (el.webkitRequestFullscreen) return el.webkitRequestFullscreen();
  if (el.msRequestFullscreen) return el.msRequestFullscreen();
  return Promise.reject('Fullscreen API not supported');
}

function exitFullscreen() {
  if (document.exitFullscreen) return document.exitFullscreen();
  if (document.webkitExitFullscreen) return document.webkitExitFullscreen();
  if (document.msExitFullscreen) return document.msExitFullscreen();
  return Promise.resolve();
}

// 1) Сначала явное предупреждение и запрос подтверждения
startBtn.addEventListener('click', () => {
  const ok = confirm('Внимание: будет запрошен полноэкранный режим и показан эффект. Продолжить?');
  if (!ok) return;

  // 2) Запрос полноэкрана (это пользовательский жест — у большинства браузеров разрешает дальнейшее воспроизведение звука)
  goFullscreen()
    .then(() => {
      // Показываем оверлей в полноэкранном состоянии
      overlay.style.display = 'flex';

      // 3) Дополнительно просим последнее согласие на звук (если хотите звук)
      const playSound = confirm('Разрешить воспроизведение звука? (если нет — нажмите Отмена)');
      if (playSound) {
        // попытка воспроизвести звуковой файл (поскольку это инициировано кликом — обычно разрешено)
        sound.currentTime = 0;
        const p = sound.play();
        if (p && p.catch) p.catch(e => {
          // Ошибка воспроизведения (например: формат, блокировка)
          console.warn('Не удалось воспроизвести звук:', e);
        });
      }
    })
    .catch(err => {
      alert('Не удалось перейти в полноэкранный режим: ' + err);
    });
});

// Закрытие
exitBtn.addEventListener('click', () => {
  overlay.style.display = 'none';
  sound.pause();
  exitFullscreen();
});

// Если пользователь вышел из полноэкранного режима (Esc), скрываем оверлей
document.addEventListener('fullscreenchange', () => {
  if (!document.fullscreenElement) {
    overlay.style.display = 'none';
    sound.pause();
  }
});
</script>
</body>
</html>
