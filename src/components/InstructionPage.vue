<!--
  Компонент страницы с инструкцией по использованию мобильного приложения.
  Содержит основные разделы:
    - Регистрация и вход
    - Основная навигация
    - Работа с группами
    - Работа с задачами
    - Вкладка Subjects
  Замените или дополните тексты при необходимости.
-->
<template>
  <section id="usage-instructions" class="usage-section">
    <h1 class="usage-title">Инструкция по использованию приложения</h1>
    <div class="usage-block">
      <h2>1. Регистрация и вход</h2>
      <p><strong>Профиль:</strong> перейдите на вкладку <em>Profile</em>. Для нового пользователя нажмите <em>Register</em>, заполните поля: Username, Email, Password и Confirm Password, затем нажмите <em>Register</em>. Для входа в систему заполните fields Username и Password и нажмите <em>Log In</em>.</p>
    </div>
    <div class="usage-block">
      <h2>2. Основная навигация</h2>
      <ul>
        <li><em>Subjects</em> – список всех предметов пользователя.</li>
        <li><em>Tasks</em> – список задач из всех групп.</li>
        <li><em>Groups</em> – раздел управления группами.</li>
        <li><em>Notifications</em> – заявки на вступление в группы.</li>
        <li><em>Profile</em> – информация о пользователе и выход.</li>
      </ul>
    </div>
    <div class="usage-block">
      <h2>3. Работа с группами</h2>
      <ol>
        <li>В <em>My Groups</em> отображаются ваши группы.</li>
        <li>Для создания новой группы нажмите <em>Create Group</em>, введите Group Name и Academic Group и подтвердите.</li>
        <li>Чтобы найти группу, нажмите <em>Search New Groups</em> и рядом с нужной нажмите <em>Join</em>.</li>
        <li>В <em>Group Details</em> можно просмотреть участников, предметы и задачи группы.</li>
        <li>Если вы администратор, доступны кнопки <em>Edit Group</em> и <em>Delete Group</em>.</li>
      </ol>
    </div>
    <div class="usage-block">
      <h2>4. Работа с задачами</h2>
      <ol>
        <li>На вкладке <em>Tasks</em> можно просматривать и создавать задачи.</li>
        <li>Для создания нажмите <em>+</em>, заполните Title, Description, Group, Subject, Deadline и нажмите <em>Create Task</em>.</li>
        <li>Задача появится в <em>Group Tasks</em> выбранной группы и в общем списке.</li>
      </ol>
    </div>
  </section>
</template>

<script>
export default {
  name: 'InstructionPage',
}
</script>

<style scoped>
.usage-section {
  max-width: 800px;
  margin: 0 auto 2rem;
  padding: 0 1.5rem 1.5rem;
  background: #ffffff;
  border-radius: 0.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}
.usage-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #1f2937;
}
.usage-block {
  margin-bottom: 1.5rem;
}
.usage-block h2 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #374151;
}
.usage-block p,
.usage-block ul,
.usage-block ol {
  font-size: 1rem;
  color: #4b5563;
  line-height: 1.5;
}
.usage-block ul {
  list-style: disc inside;
  margin: 0;
  padding-left: 1rem;
}
.usage-block ol {
  list-style: decimal inside;
  margin: 0;
  padding-left: 1rem;
}
.usage-block em {
  font-style: normal;
  font-weight: 500;
  color: #2563eb;
}
@media (max-width: 640px) {
  .usage-section {
    padding: 1rem;
  }
  .usage-title {
    font-size: 1.5rem;
  }
}
</style>
