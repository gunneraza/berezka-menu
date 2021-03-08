<template>
  <q-card class="category text-center">
    <q-card-section>
      <q-img
        :src="category.img"
        width="120px"
      />
      <div class="text-h5 q-mt-lg text-uppercase text-weight-bold">
        {{ category.title }}
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Category',
    props: {
      category: {
        type: Object,
        required: true,
      },
    },
  })
</script>

<style lang="scss">
  .category {
    width: 100%;
    box-shadow: 0 6px 10px rgb(0 0 0 / 6%);
    transition: 300ms ease;
    cursor: pointer;

    &:hover {
      box-shadow: 0 6px 18px rgb(0 0 0 / 16%);
    }
  }
</style>
