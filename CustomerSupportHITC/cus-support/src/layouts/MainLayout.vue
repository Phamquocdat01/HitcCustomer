<template>
  <q-layout view="lHh Lpr fff" class="bg-grey-1">
    <q-header elevated class="bg-white text-indigo-14" height-hint="64">
      <q-toolbar class="GPL__toolbar" style="height: 64px">
        <div class="row no-wrap col-2">
          <q-img
            src="https://www.hitc.vn/wp-content/themes/htc/images/logo-color.png?time=1689085763"
          />
        </div>

        <div
          class="q-ml-lg q-gutter-lg text-h6 text-weight-bolder row example-row-all-breakpoints items-center no-wrap"
        >
          <a href="#" class="text-indigo-14"> Trang chủ </a>
          <a href="#" class="text-indigo-14"> Tiket </a>
          <a href="#" class="text-indigo-14"> FTTH </a>
          <a href="#" class="text-indigo-14"> Danh Mục </a>
          <a href="#" class="text-indigo-14"> CR </a>
          <a href="#" class="text-indigo-14"> CS </a>
          <a href="#" class="text-indigo-14"> Báo cáo </a>
        </div>
      </q-toolbar>
      <div
        class="q-ml-sm q-gutter-sm row example-row-all-breakpoints items-center no-wrap"
      >
        <q-btn round dense flat color="indigo-14" icon="help">
          <q-tooltip>Help</q-tooltip>
        </q-btn>
        <q-btn round dense flat color="indigo-14" icon="notifications">
          <!-- <q-badge color="red" text-color="white" floating> 2 </q-badge> -->
          <q-tooltip>Notifications</q-tooltip>
        </q-btn>
        <q-btn round dense flat color="indigo-14" icon="apps">
          <q-tooltip>Apps</q-tooltip>
        </q-btn>
        <q-btn round dense flat color="indigo-14" icon="person">
          <!-- <q-avatar size="26px">
            <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
          </q-avatar> -->
          <q-tooltip>Account</q-tooltip>
        </q-btn>
      </div>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>

<style>
a {
  color: #304ffe;
  text-decoration: none;
}
a:hover {
  opacity: 0.7;
}
/* HEADER */
header {
  background-color: #ffffff;
  height: 80px;
  display: flex;
  align-items: center;
  width: 100%;
  z-index: 9999;
  position: absolute;
  box-shadow: 0 1px 6px 0 rgba(32, 33, 36, 0.28);
}
q-toolbar.screen--md .row .col-3 {
  width: 15%;
}
</style>

<!-- <template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar class="bg-primary text-white rounded-borders">
        <img
          src="https://www.hitc.vn/wp-content/themes/htc/images/logo-color.png?time=1689085763"
          style="width: 200px; height: 64px"
        />
        <q-space />
        <div class="q-gutter-md">
          <q-btn round icon="help_outline" color="primary" class="q-mr-xs" />
          <q-btn round icon="notifications" class="q-mr-xs" />
          <q-btn round icon="apps" class="q-mr-xs" />
          <q-btn round class="q-mr-xs" color="primary" icon="person" />
        </div>
       
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template> -->

<!-- <script>
// import { defineComponent, ref } from 'vue'
// import EssentialLink from 'components/EssentialLink.vue'

// const linksList = [
//   {
//     title: 'Docs',
//     caption: 'quasar.dev',
//     icon: 'school',
//     link: 'https://quasar.dev'
//   },
//   {
//     title: 'Github',
//     caption: 'github.com/quasarframework',
//     icon: 'code',
//     link: 'https://github.com/quasarframework'
//   },
//   {
//     title: 'Discord Chat Channel',
//     caption: 'chat.quasar.dev',
//     icon: 'chat',
//     link: 'https://chat.quasar.dev'
//   },
//   {
//     title: 'Forum',
//     caption: 'forum.quasar.dev',
//     icon: 'record_voice_over',
//     link: 'https://forum.quasar.dev'
//   },
//   {
//     title: 'Twitter',
//     caption: '@quasarframework',
//     icon: 'rss_feed',
//     link: 'https://twitter.quasar.dev'
//   },
//   {
//     title: 'Facebook',
//     caption: '@QuasarFramework',
//     icon: 'public',
//     link: 'https://facebook.quasar.dev'
//   },
//   {
//     title: 'Quasar Awesome',
//     caption: 'Community Quasar projects',
//     icon: 'favorite',
//     link: 'https://awesome.quasar.dev'
//   }
// ]

// export default defineComponent({
//   name: 'MainLayout',

//   components: {
//     EssentialLink
//   },

//   setup () {
//     const leftDrawerOpen = ref(false)

//     return {
//       essentialLinks: linksList,
//       leftDrawerOpen,
//       toggleLeftDrawer () {
//         leftDrawerOpen.value = !leftDrawerOpen.value
//       }
//     }
//   }
// })
</script> -->