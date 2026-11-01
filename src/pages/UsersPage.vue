<template>
  <q-page padding>
    <div class="q-pa-md row items-start q-gutter-md">
  <q-card class="my-card">
    <q-card-section>
      {{ lorem }}
    </q-card-section>
  </q-card>

  <q-card
    class="my-card text-white"
    style="background: radial-gradient(circle, #35a2ff 0%, #014a88 100%)"
  >
    <q-card-section>
      <div class="text-h6">Naš mijenjajući planet</div>
      <!--div class="text-subtitle2">by Borna Štreberčina</div-->
    </q-card-section>

    <q-card-section class="q-pt-none">
      {{ lorem }}
    </q-card-section>
  </q-card>

  <q-card dark bordered class="bg-grey-9 my-card">
    <q-card-section>
      <div class="text-h6">Borna Štreberčina</div>
      <div class="text-subtitle2">by Borna Štreberčina</div>
    </q-card-section>

    <q-separator dark inset />

    <q-card-section>
      {{ ana }}
    </q-card-section>
  </q-card>

  <q-card flat bordered class="my-card">
    <q-card-section>
      <div class="text-h6">Borna Štreberčina</div>
    </q-card-section>

    <q-card-section class="q-pt-none">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua.
    </q-card-section>

    <q-separator inset />

    <q-card-section>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua.
    </q-card-section>
  </q-card>
</div>
  </q-page>
</template>

<script setup>
const lorem =
  'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
const ana = "Ana je super"
</script>


<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
