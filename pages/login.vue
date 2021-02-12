<template>
  <section class="section is-align-self-center">
    <section>
      <Header class="top-header">Вход</Header>
    </section>
    <b-field>
      <b-input
        v-model="login.email"
        size="is-design"
        placeholder="Email"
      ></b-input>
    </b-field>
    <b-field>
      <b-input
        v-model="login.password"
        placeholder="Пароль"
        type="password"
        size="is-design"
      ></b-input>
    </b-field>
    <b-button type="is-primary" class="mt-64 is-big">Войти</b-button>
    <p class="mt-64">
      Забыль пароль?
      <nuxt-link to="/recover">Восстановить</nuxt-link>
    </p>
    <p>
      <nuxt-link to="/register">Регистрация</nuxt-link>
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
      login: {
        email: '',
        password: '',
      },
    }
  },
  methods: {
    async userLogin() {
      try {
        const response = await this.$auth.loginWith('local', {
          data: this.login,
        })
        console.log(response)
      } catch (err) {
        console.log(err)
      }
    },
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
