<template>
  <section class="home mt-5">
    <div class="container">
      <h3 class="text-center">{{ title }}</h3>
      <div class="row justify-content-center mt-5">
        <div class="col-12 col-md-12 col-lg-6">
          <p class="text-center">
            HalalBros adalah sebuah Web Aplikasi muslim yang menyediakan
            bermacam-macam fitur seperti Doa Harian, Kisah 25 Nabi, Bacaan
            Sholat, Al-Quran, dll
          </p>
        </div>
      </div>
      <div class="row justify-content-center mt-3">
        <div class="col-12 col-md-12 col-lg-6 text-center">
          <router-link
            class="btn btn-outline-secondary btn-block shadow-none"
            v-for="(list, i) in listApi"
            :key="i"
            :to="{ path: list.path }"
          >
            {{ list.title }}
          </router-link>
        </div>
      </div>
    </div>
  </section>
  <About class="abt" />
</template>

<script>
/* eslint-disable */
import About from "./About";
export default {
  data: () => ({
    title: "👌 HalalBros",
    listApi: [
      { path: "/asmaul", title: "Asmaul Husna" },
      { path: "/doa-harian", title: "Doa Doa Harian" },
      { path: "/kisah-nabi", title: "Kisah 25 Nabi" },
      { path: "/niat-sholat", title: "Niat Sholat" },
      { path: "/bacaan-sholat", title: "Bacaan Sholat" },
      { path: "/alquran", title: "Al Quran Lengkap" },
    ],
  }),
  components: {
    About,
  },
};
</script>

<style lang="scss">
.abt {
  margin-top: 80px;
  margin-bottom: 100px;
}
</style>
