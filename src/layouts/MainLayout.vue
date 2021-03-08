<template>
  <q-layout>

    <q-page-container>
      <div class="container q-mx-auto">
        <router-view/>
      </div>
    </q-page-container>

  </q-layout>
</template>

<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'MainLayout',
  })
</script>

<style lang="scss">
  .container {
    max-width: 540px;
    padding: 14px;
  }
</style>
