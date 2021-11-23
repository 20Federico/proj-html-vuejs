<template>
  <div class="container">
    <div class="row row-cols-4">
      <div class="col text-center" v-for="data, i in dataTable" :key="i">
        <p class="data_stat">{{data.stat}}</p>
        <p class="data_title">{{data.title.toUpperCase()}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainDataTable",
  data() {
    return {
      dataTable: [
        {
          title: 'finished sessions',
          stat: '1.926'
        },
        {
          title: 'satisfaction rate',
          stat: '100%'
        },
        {
          title: 'enrolled learners',
          stat: '3092+'
        },
        {
          title: 'online instructors',
          stat: '200'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";

  .container {
    padding: $padding_l 20px;
  }
  .col {
    border-right: 1px dashed $text_brand_primary;
    &:first-of-type {
      border-left: 1px dashed $text_brand_primary;
    }
  }
  .data_stat {
    font-size: $font_size_h2;
    color: $text_brand_primary;
    font-weight: bold;
  }
  .data_title {
    color: $text_titles;
    font-weight: bold;
  }
</style>