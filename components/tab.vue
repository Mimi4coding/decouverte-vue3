<script>
import DemoGrid from './Grid.vue'

export default {
  components: {
    DemoGrid
  },
  data: () => ({
    searchQuery: '',
    gridColumns: ['CoreUI'],
    gridData: [
      {  CoreUI: 'Dashboard'},
      {  CoreUI: '---THEME' },
      {  CoreUI: 'Colors' },
      {  CoreUI: 'Typgraphy'},
      {  CoreUI: '---COMPONENTS'},
      {  CoreUI: 'Base' },
      {  CoreUI: 'Buttons' },
      {  CoreUI: 'Charts' },
      {  CoreUI: 'Forms' },
      {  CoreUI: 'Icons' },
      {  CoreUI: 'Notifications' },
      {  CoreUI: 'Widgets (new)' },
      {  CoreUI: '---EXTRAS' },
      {  CoreUI: 'Pages' },
      {  CoreUI: 'Docs' },
      {  CoreUI: 'Try CoreUIPRO' },
    ]
  })
}
</script>

<template>
  <form id="search">
    Search <input name="query" v-model="searchQuery">
  </form>
  <DemoGrid
    :data="gridData"
    :columns="gridColumns"
    :filter-key="searchQuery">
  </DemoGrid>
</template>