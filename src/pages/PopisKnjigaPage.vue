
<template>
  <q-page padding>
    <div class="text-h4 q-mb-md">Popis svih knjiga</div>
    <div class="text-subtitle1 q-mb-lg">
      Pregledajte dostupne knjige u našoj knjižnici.
    </div>

    <div class="q-pa-md">
      <q-table
        title="Popis knjiga"
        :rows="rows"
        :columns="columns"
        row-key="id"
      />
    </div>

  </q-page>
</template>

<script setup>
const columns = [
  {
    name: 'id',
    label: 'ID',
    field: 'id',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  },
  {
    name: 'naslov',
    label: 'Naslov',
    field: 'naslov',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  },
  {
    name: 'autor',
    label: 'Autor',
    field: 'autor',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  },
  {
    name: 'zanr',
    label: 'Žanr',
    field: 'zanr',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  },
  {
    name: 'godina',
    label: 'Godina izdanja',
    field: 'godina',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  },
  {
    name: 'izdavac',
    label: 'Izdavač',
    field: 'izdavac',
    align: 'left',
    sortable: true,
    style: {
      fontSize: '14px'
    },
    headerStyle: {
      fontSize: '18px'
    }
  }
]

const rows = [
  {
    id: 1,
    naslov: 'Mali princ',
    autor: 'Antoine de Saint-Exupéry',
    zanr: 'Fantastika',
    godina: 1943,
    izdavac: 'Mladost'
  },
  {
    id: 2,
    naslov: 'Zločin i kazna',
    autor: 'Fjodor Dostojevski',
    zanr: 'Roman',
    godina: 1866,
    izdavac: 'Školska knjiga'
  },
  {
    id: 3,
    naslov: 'Frankenstein',
    autor: 'Mary Shelley',
    zanr: 'Znanstvena fantastika',
    godina: 1818,
    izdavac: 'Lumen izdavaštvo'
  },
  {
    id: 4,
    naslov: 'Ponos i predrasude',
    autor: 'Jane Austen',
    zanr: 'Ljubavni roman',
    godina: 1813.,
    izdavac: 'Znanje'
  },
  {
    id: 5,
    naslov: 'Harry Potter i kamen mudraca',
    autor: 'J. K. Rowling',
    zanr: 'Fantastika',
    godina: 1997,
    izdavac: 'Bloomsbury'
  },
  {
    id: 6,
    naslov: 'Gospodar prstenova',
    autor: 'J. R. R. Tolkien',
    zanr: 'Fantastika',
    godina: 1954,
    izdavac: 'Allen & Unwin'
  }
]
</script>
