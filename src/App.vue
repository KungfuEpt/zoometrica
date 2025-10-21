<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faMagnifyingGlass, faLightbulb, faKey, faMobile, faTree } from '@fortawesome/free-solid-svg-icons';
import { faTelegram } from '@fortawesome/free-brands-svg-icons';

const isScrolled = ref(false);

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
const handleScroll = () => {
  isScrolled.value = window.scrollY > 0;
};
</script>

<template>
  <main class="main">
    <nav class="navbar" :class="{ 'scrolled': isScrolled }">
      <div class="navbar-content">
        <div class="navbar-icon">
          <a href="/" class="logo-link">
            <img class="logo" src="/zoometrica.png" alt="Logo">
            <p>Зоометрика</p>
          </a>
        </div>
        <div class="navbar-navigation">
          <a href="https://t.me/qssul" target="_blank" class="nav-link">
            Связь
          </a>
        </div>
      </div>
    </nav>
    <div class="header">
      <div class="header-content">
        <div class="header-block">
          <h1 class="header-title">Зоометрика</h1>
          <p>Зоометрика – ваш ключ к здоровому стаду и эффективному животноводству. Мы применяем IoT-решения и глубокую аналитику для раннего выявления проблем, снижая потери и заботясь о комфорте животных.</p>
        </div>
      </div>
    </div>
    <div class="information">
      <div class="information-content">
        <div class="why-us">
          <div class="why-us-title">
            <h1>Почему именно мы?</h1>
          </div>
          <div class="why-us-items">
            <div class="row">
              <div class="column">
                <div class="column-icon">
                  <FontAwesomeIcon :icon="faKey"></FontAwesomeIcon>
                </div>
                <div class="column-container">
                  <h3>Комплексный фиджитал-подход</h3>
                  <p>Мы объединяем физические устройства (датчик, ошейник, камера) и цифровую платформу в единую экосистему. Это позволяет получать непрерывные данные о состоянии животных и сразу видеть аналитику в приложении.</p>
                </div>
              </div>
              <div class="column">
                <div class="column-icon">
                  <FontAwesomeIcon :icon="faLightbulb"></FontAwesomeIcon>
                </div>
                <div class="column-container">
                  <h3>Технологии заботы о животных</h3>
                  <p>Наши сенсоры неинвазивны, безопасны и разработаны с учётом комфорта коровы. Мы используем IoT-технологии, чтобы наблюдать за здоровьем без стресса для животного.</p>
                </div>
              </div>
              <div class="column">
                <div class="column-icon">
                  <FontAwesomeIcon :icon="faMagnifyingGlass"></FontAwesomeIcon>
                </div>
                <div class="column-container">
                  <h3>Аналитика и раннее предупреждение</h3>
                  <p>Система не просто собирает данные — она их анализирует. Мы выявляем аномалии (температура, дыхание, метаболизм, pH рубца) на ранних стадиях, помогая предотвратить болезни до того, как они проявятся.</p>
                </div>
              </div>
              <div class="column">
                <div class="column-icon">
                  <FontAwesomeIcon :icon="faMobile"></FontAwesomeIcon>
                </div>
                <div class="column-container">
                  <h3>Удобное мобильное приложение</h3>
                  <p>Фермер получает все ключевые показатели в одном месте: графики, уведомления, прогнозы. Интерфейс максимально прост — даже без технической подготовки.</p>
                </div>
              </div>
              <div class="column">
                <div class="column-icon">
                  <FontAwesomeIcon :icon="faTree"></FontAwesomeIcon>
                </div>
                <div class="column-container">
                  <h3>Экономическая и экологическая эффективность</h3>
                  <p>Мы помогаем снижать потери из-за болезней, повышать продуктивность и сокращать избыточное использование медикаментов. Здоровье животных = устойчивое производство.</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="path">
          <div class="path-title">
            <h1>Наш путь к масштабированию.</h1>
          </div>
          <p>
            Ближайшие 4-6 недель (Тестирование):
            <br>1. Пилотные проекты на X фермах для валидации функционала и сбора обратной связи.
            <br>2. Оптимизация пользовательского интерфейса приложения на основе первых отзывов.
            <br>3. Тестирование надежности IoT-соединения в различных условиях.
          </p>
        </div>
        <div class="team">
          <div class="team-title">
            <h1>Команда Проекта:</h1>
          </div>
          <div class="team-items">
            <div class="row">
              <div class="column-person">
                <img src="/suleymanovasaida3.png"></img>
                <h3>Сулейманова<br>Саида</h3>
                <p>Маркетолог, юрист</p>
              </div>
              <div class="column-person">
                <img src="/masgutovamirkhan3.png"></img>
                <h3>Масгутов<br>Амирхан</h3>
                <p>Финансист, аналитик</p>
              </div>
              <div class="column-person">
                <img src="/saetovayaz3.png"></img>
                <h3>Саетов<br>Аяз</h3>
                <p>Разработчик</p>
              </div>
              <div class="column-person">
                <img src="/sokolovnikita3.png"></img>
                <h3>Соколов<br>Никита</h3>
                <p>Продуктолог</p>
              </div>
            </div>
          </div>
        </div>
        <div class="team">
          <div class="team-title">
            <h1>Приложения</h1>
          </div>
          <p>Файлы и другая полезная информация</p>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="footer-content">
        <a href="/" class="logo-link">
          <p>Зоометрика</p>
        </a>
        <!-- <div class="footer-socials">
          <a href="#" class="" >
            <FontAwesomeIcon :icon="faTelegram"></FontAwesomeIcon>
          </a>
        </div> -->
      </div>
    </div>
  </main>
</template>

<style scoped>
.path h1 {
  text-align: left;
  margin-bottom: 40px;
  font-weight: 600;
  font-size: 32px;
}

.path {
  border: 2px solid #EFF2F8;
  border-radius: 64px;
  padding: 32px;
}

.footer-socials a {
  width: 32px;
  height: 32px;
  color: gray;
  font-size: 24px;
  margin-bottom: 16px;
}

.footer-content {
  margin: auto;
  max-width: calc(1232px + 8px * 2 + 40px * 2);
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.footer {
  box-sizing: border-box;
  background-color: white;
  width: 100%;
  box-shadow: inset 0 1px 0 rgba(0, 0, 0, 0.1)
}

.column-person p {
  font-size: 16px;
  font-weight: 400;
  text-align: center;
  margin: 0 0 8px 0 ;
}

.column-person h3 {
  font-size: 24px;
  font-weight: 500;
  text-align: center;
  margin: 0 0 8px 0 ;
}

.column-person img {
  margin-bottom: 16px;
  height: 128px;
  width: 128px;
  background-color: lightgray;
  border: 4px solid lightgray;
  border-radius: 9999px;
  object-fit: cover;
  box-sizing: border-box;
}

.column-person {
  display: flex;
  flex: 1 1 calc(25% - 20px);
  flex-wrap: wrap;
  flex-direction: column;
  align-items: center;
  padding: 32px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 32px;
  width: 100%;
  box-sizing: border-box;
}

.team h1 {
  text-align: left;
  margin-bottom: 40px;
  font-weight: 600;
  font-size: 32px;
}

.team {
  padding-top: 64px;
  padding-bottom: 64px;
}

.information {
  background-color: white;
  width: 100%;
}

.information-content {
  margin: auto;
  max-width: calc(1232px + 8px * 2 + 40px * 2);
  padding: 48px 16px 48px 16px;
}

.why-us-title h1 {
  text-align: left;
  margin-bottom: 40px;
  font-weight: 600;
  font-size: 32px;
}

.why-us {
  padding-bottom: 64px;
}

.row {
  display: flex; 
  flex-wrap: wrap; 
  gap: 20px;
  justify-content: center; 
}

.column {
  flex: 1 1 calc(33.333% - 20px);
  min-width: 280px;
  display: flex; 
  flex-direction: column;
  align-items: flex-start;
  padding: 20px 0 20px 0;
  box-sizing: border-box;
  top: 0;
  opacity: 1;
  transition: top .8s cubic-bezier(.25,.46,.45,.94),opacity .8s cubic-bezier(.25,.46,.45,.94);
  transition-delay: .1s;
}

.column-icon {
  width: 32px;
  height: 32px;
  color: gray;
  font-size: 24px;
  margin-bottom: 16px;
}

.column-container {
  flex-grow: 1;
}

.column-container h3 {
  margin-top: 0;
  margin-bottom: 8px;
  font-size: 1.3em;
  font-weight: 500;
}

.column-container p {
  margin: 0;
  font-size: 1em;
  line-height: 1.5;
}

@media (max-width: 768px) {
  .column {
    flex: 1 1 calc(50% - 20px);
  }
}

@media (max-width: 480px) {
  .column {
    flex: 1 1 100%;
    min-width: unset;
  }

  .why-us-title h1 {
    font-size: 2em;
  }

  .column-icon {
    width: 50px;
    height: 50px;
    margin-right: 15px;
  }

  .column-container h3 {
    font-size: 1.1em;
  }

  .column-container p {
    font-size: 0.95em;
  }
}

.header-title {
  font-size: 48px;
  font-weight: 600;
}

.header-block {
  max-width: 50%;
}

@media (max-width: 1000px) {
  .header-block {
    max-width: 100%;
  }
}

.header-content {
  display: flex;
  flex-direction: row;
  max-width: calc(1232px + 8px * 2 + 40px * 2);
  margin-left: auto;
  margin-right: auto;
  padding: 0 16px 0 16px;
}

.header {
  padding: 128px 0 128px 0;
  width: 100%;
  background-image: url("/background-header2.jpg");
  background-size: cover;
  color: white;
}

.main {
  height: 200vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #EFF2F8;
}

.navbar-profile {
  height: 100%;
  line-height: 64px;
  justify-content: flex-end;
}

.navbar-navigation {
  display: flex;
  flex-direction: row;
  height: 100%;
  line-height: 64px;
  justify-content: flex-end;
  gap: 20px;
}

.logo-link p {
  font-weight: 500;
  font-size: 20px;
}

.logo {
  height: 40px;
  width: 40px;
  margin-right: 8px;
}

.logo-link {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
}

.scrolled {
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.1)
}

.navbar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: calc(1232px + 8px * 2 + 40px * 2);
  padding: 0 16px 0 16px;
  box-sizing: border-box;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: center;
  position: sticky;
  top: 0;
  width: 100%;
  z-index: 1000;
  background-color: white;
  height: 64px;
}

a {
  text-decoration: inherit;
  color: inherit;
}
</style>
