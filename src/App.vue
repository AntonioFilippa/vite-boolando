<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  data() {
    return {}
  },
  components: {
    AppHeader,
    AppMain,
  }
}
</script>
<template>
 
 <app-header></app-header>
 <app-main></app-main>

</template>

<style lang="scss" scoped>
@use 'src/scss/main.scss'
</style>