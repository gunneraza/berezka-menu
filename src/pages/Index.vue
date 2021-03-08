<template>
  <q-page>
    <logo class="q-mb-xl q-mt-lg" />
    <div class="row q-col-gutter-md">
      <div
        v-for="category in categories"
        :key="category.title"
        class="col-6"
      >
        <category :category="category" />
      </div>
    </div>
  </q-page>
</template>

<script>
  import { defineComponent, computed } from 'vue'
  import Category from "components/Category"
  import { useStore } from 'vuex'
  import Logo from 'components/Logo'

  export default defineComponent({
    name: 'PageIndex',
    components: {
      Logo,
      Category,
    },

    setup() {
      const store = useStore()
      const categories = computed(() => store.state.products.categories)

      return {
        categories,
      }
    },
  })
</script>

