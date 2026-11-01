<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-h5 text-weight-bold"> Knjižnica </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink v-for="link in linksList" :key="link.label" v-bind="link" />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import EssentialLink from '@/components/EssentialLink.vue'

const linksList = [
  {
    label: 'Naslovnica',
    caption: 'Početna stranica',
    icon: 'home',
    link: '/#/',
  },
  {
    label: 'Popis knjiga',
    caption: 'Sve knjige u knjižnici',
    icon: 'menu_book',
    link: '/#/popis_knjiga',
  },
  {
    label: 'Pretraživanje',
    caption: 'Pronađi knjigu',
    icon: 'search',
    link: '/#/pretrazivanje',
  },
  {
    label: 'O nama',
    caption: 'Informacije o knjižnici',
    icon: 'info',
    link: '/#/o_nama',
  },
  {
    label: 'Lokacija',
    caption: 'Gdje se nalazimo',
    icon: 'location_on',
    link: '/#/lokacija',
  },
  {
    label: 'Prijava',
    caption: 'Prijavi se u sustav',
    icon: 'login',
    link: '/#/login',
  },
  {
    label: 'Registracija',
    caption: 'Izradi korisnički račun',
    icon: 'person_add',
    link: '/#/registracija',
  },
]

const leftDrawerOpen = ref(false)

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
