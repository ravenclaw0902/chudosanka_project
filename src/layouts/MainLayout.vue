<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-green-6">
      <div class="row no-wrap">
        <q-toolbar class="col-10">
          <q-btn
            flat
            dense
            round
            icon="menu"
            aria-label="Menu"
            @click="leftDrawerOpen = !leftDrawerOpen"
          />

          <q-toolbar-title class="flex row no-wrap">
            <div class="col-2 row no-wrap items-center">
              <a href="/">
                <img
                  src="/imgs/logo.svg"
                  style="margin: 12px; width: 100px; height: 100px"
                />
              </a>
              <div class="col-10 flex-center items-center text-center">
                <span class="text-center">Центр семейного здоровья</span><br />
                <span class="text-center">Чудосанка</span>
              </div>
            </div>
          </q-toolbar-title>
        </q-toolbar>
        <q-toolbar class="col-2">
          <q-space></q-space>
          <q-btn flat round dense icon="search" />
          <q-btn flat round dense icon="assignment_ind" />
        </q-toolbar>
      </div>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label header class="text-grey-8">
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <MainCarousel />
      <router-view />
    </q-page-container>

    <q-footer class="bg-green-8">
      <div class="row no-wrap">
        <a href="/" class="text-white">123</a>
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'
import MainCarousel from 'components/MainCarousel.vue'

export default {
  name: 'MainLayout',

  components: {
    EssentialLink,
    MainCarousel
  },

  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: [
        {
          title: 'Docs',
          caption: 'quasar.dev',
          icon: 'school',
          link: 'https://quasar.dev'
        },
        {
          title: 'Github',
          caption: 'github.com/quasarframework',
          icon: 'code',
          link: 'https://github.com/quasarframework'
        },
        {
          title: 'Discord Chat Channel',
          caption: 'chat.quasar.dev',
          icon: 'chat',
          link: 'https://chat.quasar.dev'
        },
        {
          title: 'Forum',
          caption: 'forum.quasar.dev',
          icon: 'record_voice_over',
          link: 'https://forum.quasar.dev'
        },
        {
          title: 'Twitter',
          caption: '@quasarframework',
          icon: 'rss_feed',
          link: 'https://twitter.quasar.dev'
        },
        {
          title: 'Facebook',
          caption: '@QuasarFramework',
          icon: 'public',
          link: 'https://facebook.quasar.dev'
        },
        {
          title: 'Quasar Awesome',
          caption: 'Community Quasar projects',
          icon: 'favorite',
          link: 'https://awesome.quasar.dev'
        }
      ]
    }
  }
}
</script>
