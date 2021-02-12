<template>
  <section>
    <section class="section is-welcome-bg">
      <section class="container is-widescreen">
        <section class="is-moved is-backgrounded">
          <h1 class="is-welcome">
            ООО “Современные технологии&nbsp;автоматизации”
          </h1>
          <p class="is-welcome-medium mt-32">
            Автоматизированное складское помещение без использования
            человеческих ресурсов уже на вашем производстве
          </p>
          <p class="is-welcome-small mt-16">
            На данном сайте представлено пример того, как можно автоматизировать
            ваш склад и сэкономить на этом ваши деньги
          </p>
        </section>
        <section class="is-moved my-6">
          <p class="is-flex is-align-items-center">
            <img src="~assets/play-button.svg" alt="Play button" />
            <a href="https://youtu.be/MeowMeowMeow" class="ml-4">
              Посмотреть видео о разработке
            </a>
          </p>
        </section>
      </section>
    </section>
    <section class="hero is-black">
      <div class="hero-body columns has-text-centered">
        <div class="column is-one-fourth is-offset-one-fourth">
          <h2 class="is-fact-number">150</h2>
          <p class="is-fact-description">положительных отзывов</p>
        </div>
        <div class="column is-one-fourth">
          <h2 class="is-fact-number">150+</h2>
          <p class="is-fact-description">законченных проектов</p>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  auth: false,
  name: 'Index',
}
</script>

<style scoped lang="scss">
@import 'assets/style/colors';

.is-welcome-bg {
  background: url('~assets/welcome_bg.png') no-repeat;
  background-size: cover;
}
.is-welcome {
  font-size: 90px;
  font-weight: 700;
  color: black;
  line-height: 112.5px;
}
.is-welcome-medium {
  font-size: 30px;
  line-height: 37.5px;
  color: black;
  font-weight: 400;
}
.is-welcome-small {
  font-size: 20px;
  line-height: 25.5px;
  color: black;
  font-weight: 400;
}
.is-fact-description {
  font-weight: 400;
  font-size: 35px;
  line-height: 41px;
  color: white;
}
.is-fact-number {
  font-weight: 700;
  font-size: 50px;
  line-height: 58.59px;
  color: $primary;
}

.is-moved {
  margin-left: -60px;
  position: relative;
}
.is-backgrounded {
  border: 20px solid $primary;
  background: rgba(white, 0.5);
  padding: 110px 60px;
}
</style>
