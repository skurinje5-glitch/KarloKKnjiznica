<template>
  <q-page padding>
   <div class="text-h4 q-mb-md">Prijava korisnika</div>

    <div class="text-subtitle1 q-mb-lg">
      Prijavite se svojim korisničkim podacima.
    </div>

    <div style="max-width: 400px">
      <q-input
        v-model="korisnickoIme"
        label="Korisničko ime"
        outlined
        class="q-mb-md"
      />

      <q-input
        v-model="lozinka"
        label="Lozinka"
        type="password"
        outlined
        class="q-mb-md"
      />

      <q-btn
        label="Potvrdi"
        color="primary"
        @click="potvrdi"
      />
    </div>
  </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const korisnickoIme = ref('')
    const lozinka = ref('')

    function potvrdi () {
      alert('Podaci za prijavu su uneseni.')
    }

    return {
      korisnickoIme,
      lozinka,
      potvrdi
    }
  }
}
</script>
