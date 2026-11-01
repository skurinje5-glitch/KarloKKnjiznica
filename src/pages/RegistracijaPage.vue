<template>
  <q-page padding>
  <div class="text-h4 q-mb-md">Registracija korisnika</div>

    <div class="text-subtitle1 q-mb-lg">
      Kreirajte svoj korisnički račun.
    </div>

    <div style="max-width: 400px">
      <q-input
        v-model="ime"
        label="Ime"
        outlined
        class="q-mb-md"
      />

      <q-input
        v-model="prezime"
        label="Prezime"
        outlined
        class="q-mb-md"
      />

      <q-input
        v-model="korisnickoIme"
        label="Korisničko ime"
        outlined
        class="q-mb-md"
      />

      <q-input
        v-model="email"
        label="E-mail"
        type="email"
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

      <q-input
        v-model="telefon"
        label="Telefon"
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
    const ime = ref('')
    const prezime = ref('')
    const korisnickoIme = ref('')
    const email = ref('')
    const lozinka = ref('')
    const telefon = ref('')

    function potvrdi () {
      alert('Registracija je unesena.')
    }

    return {
      ime,
      prezime,
      korisnickoIme,
      email,
      lozinka,
      telefon,
      potvrdi
    }
  }
}
</script>
