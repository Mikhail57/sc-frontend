<template>
  <div>
    <b-navbar :fixed-top="true" wrapper-class="container">
      <template #brand>
        <b-navbar-item tag="router-link" :to="{ path: '/' }">
          <img width="64" height="64" src="~assets/icon.svg" alt="Company" />
        </b-navbar-item>
      </template>
      <template #start>
        <b-navbar-item v-for="item in links" :key="item.title" :href="item.to">
          {{ item.title }}</b-navbar-item
        >
      </template>

      <template #end>
        <b-navbar-item tag="div">
          <v-template v-if="!loggedIn">
            <div class="buttons">
              <router-link class="button is-primary" to="/login">
                Вход
              </router-link>
              <router-link class="button is-light" to="/register">
                Регистрация
              </router-link>
            </div>
          </v-template>
        </b-navbar-item>
      </template>
    </b-navbar>

    <section>
      <nuxt />
    </section>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: mapState({
    user: (state) => state.auth.user,
    loggedIn: (state) => state.auth.loggedIn,
  }),
  data() {
    return {
      links: [
        {
          title: 'Главная',
          to: '/',
        },
        {
          title: 'Личный кабинет',
          to: '/account',
        },
        {
          title: 'Склад',
          to: '/warehouse',
        },
        {
          title: 'Склад',
          to: '/schedule',
        },
        {
          title: 'Видео-поток',
          to: '/video',
        },
        {
          title: 'О нас',
          to: '/about',
        },
      ],
    }
  },
}
</script>
