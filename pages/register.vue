<template>
  <section class="section is-align-self-center">
    <section>
      <Header class="top-header">Регистрация</Header>
    </section>
    <b-field>
      <b-input v-model="email" size="is-design" placeholder="Email"></b-input>
    </b-field>
    <b-field>
      <b-input
        v-model="password"
        placeholder="Пароль"
        type="password"
        size="is-design"
      ></b-input>
    </b-field>
    <b-button type="is-primary" class="mt-64 is-big"
      >Зарегистрироваться</b-button
    >
    <p class="mt-64">
      Уже зарегистрированы?
      <nuxt-link to="/login">Войти</nuxt-link>
    </p>
  </section>
</template>

<script>
export default {
  name: 'HomePage',

  components: {},

  layout: 'one-side',

  data() {
    return {
      email: '',
      password: '',
    }
  },
}
</script>

<style lang="scss" scoped>
@import 'assets/style/colors';

.top-header {
  margin-bottom: 72px;
}

.mt-64 {
  margin-top: 64px;
}

a {
  font-weight: 700;
  color: black;

  &:hover {
    text-decoration: underline;
    text-underline-color: $secondary;
  }
}
</style>
