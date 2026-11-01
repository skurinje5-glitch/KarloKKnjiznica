<template>
  <q-page padding>
  <div class="text-h4 q-mb-md">Pretraživanje knjiga</div>

    <div class="text-subtitle1 q-mb-lg">
      Pronađite knjigu prema njezinu naslovu ili autoru.
    </div>

    <q-input
      v-model="trazeniPojam"
      label="Unesite naziv knjige ili autora"
      outlined
      class="q-mb-md"
    />

    <div class="q-mb-md">
      <q-checkbox v-model="poNaslovu" label="Pretražuj po naslovu" />
      <q-checkbox v-model="poAutoru" label="Pretražuj po autoru" />
    </div>

    <q-btn
      label="Traži"
      color="primary"
      @click="traziKnjigu"
      class="q-mb-lg"
    />

    <q-table
      title="Rezultati pretraživanja"
      :rows="rezultati"
      :columns="columns"
      row-key="id"
    />
  </q-page>
</template>

<script>
import { ref } from 'vue'

const columns = [
  {
    name: 'id',
    label: 'ID',
    field: 'id',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'naslov',
    label: 'Naslov',
    field: 'naslov',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'autor',
    label: 'Autor',
    field: 'autor',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'zanr',
    label: 'Žanr',
    field: 'zanr',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  }
]

const knjige = [
  { id: 1, naslov: 'Mali princ', autor: 'Antoine de Saint-Exupéry', zanr: 'Fantastika' },
  { id: 2, naslov: 'Zločin i kazna', autor: 'Fjodor Dostojevski', zanr: 'Roman' },
  { id: 3, naslov: 'Frankestein', autor: 'Mary Shelley', zanr: 'Znanstvena fantastika' },
  { id: 4, naslov: 'Ponos i predrasude', autor: 'Jane Austen', zanr: 'Ljubavni roman' },
  { id: 5, naslov: 'Gospodar prstenova', autor: 'J. R. R. Tolkien', zanr: 'Fantastika' }
]

export default {
  setup () {
    const trazeniPojam = ref('')
    const poNaslovu = ref(true)
    const poAutoru = ref(false)
    const rezultati = ref([])

    function traziKnjigu () {
      const pojam = trazeniPojam.value.toLowerCase()

      rezultati.value = knjige.filter(knjiga => {
        return (
          (poNaslovu.value && knjiga.naslov.toLowerCase().includes(pojam)) ||
          (poAutoru.value && knjiga.autor.toLowerCase().includes(pojam))
        )
      })
    }

    return {
      columns,
      trazeniPojam,
      poNaslovu,
      poAutoru,
      rezultati,
      traziKnjigu
    }
  }
}
</script>
