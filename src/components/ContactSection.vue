<!--
  Инструкция:
  1. Плейсхолдеры уже заменены базовыми стилями.
  2. Если нужно изменить цвета или отступы — правьте соответствующие свойства в этом блоке <style>.
-->
<template>
  <section id="contact" class="contact-section">
    <h2 class="contact-title">Контакты</h2>
    <p class="contact-subtitle">Ссылки на репозитории нашего проекта:</p>
    <ul class="contact-list">
      <li class="contact-item">
        <strong>Backend:</strong>
        <a class="contact-link" href="https://github.com/sub2pewdiepie/ToIP_Workspace" target="_blank" rel="noopener">ToIP_Workspace</a>
      </li>
      <li class="contact-item">
        <strong>Frontend:</strong>
        <a class="contact-link" href="https://github.com/Dave44617665/INDFRONT" target="_blank" rel="noopener">INDFRONT</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
}
</script>

<style scoped>
/* Основные стили секции */
.contact-section {
  background-color: #f9fafb;
  padding: 0 2rem 2rem;
  border-radius: 0.5rem;
  max-width: 800px;
  margin: 0 auto;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

/* Заголовок */
.contact-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  color: #1f2937;
}

/* Подзаголовок */
.contact-subtitle {
  font-size: 1rem;
  margin-bottom: 1.5rem;
  color: #4b5563;
}

/* Список контактов */
.contact-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
}

.contact-item {
  display: flex;
  flex-direction: column;
}

.contact-item strong {
  font-weight: 600;
  margin-bottom: 0.25rem;
  color: #374151;
}

.contact-text {
  color: #6b7280;
}

/* Ссылки */
.contact-link {
  color: #2563eb;
  text-decoration: none;
  font-weight: 500;
  word-break: break-all;
}

.contact-link:hover {
  text-decoration: underline;
}

/* Адаптив */
@media (max-width: 640px) {
  .contact-section {
    padding: 1rem;
  }
  .contact-title {
    font-size: 1.5rem;
  }
}
</style>
