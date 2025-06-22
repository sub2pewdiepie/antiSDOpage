<template>
  <section class="description-section">
    <h1 class="description-title">Описание проекта</h1>
    <p class="description-text">
      Этот проект представляет собой образовательный портал, предназначенный для помощи студентам в организации их учебной деятельности. Он состоит из бэкенд API, разработанного на Go, и мобильного фронтенд-приложения, созданного с использованием React Native.
    </p>
    <p class="description-text">
      Система позволяет пользователям регистрироваться, входить в систему, создавать учебные группы и присоединяться к ним, управлять задачами и просматривать предметы. Ключевые особенности включают аутентификацию на основе JWT, использование паттерна «Репозиторий» для доступа к данным и CI/CD-пайплайн с использованием GitHub Actions для автоматизированного развертывания.
    </p>
  </section>
</template>

<script>
export default {
  name: 'DescriptionPage',
}
</script>

<style scoped>
.description-section {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 1.5rem 1.5rem;
  background: #ffffff;
  border-radius: 0.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  color: #333;
  text-align: left;
}

.description-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #1f2937;
  text-align: center;
}

.description-text {
  font-size: 1rem;
  color: #4b5563;
  line-height: 1.6;
  margin-bottom: 1rem;
}
</style> 