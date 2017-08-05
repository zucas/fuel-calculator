<template>
  <q-layout>
    <div slot="header" class="toolbar red">
      <q-toolbar-title :padding="0">
        Sim Fuel Calculator by Davi Zucas
      </q-toolbar-title>
    </div>

    <!--
      Replace following "div" with
      "<router-view class="layout-view">" component
      if using subRoutes
    -->
    <div class="layout-padding">
      <Terms @aceitou="aceitou"></Terms>
    </div>
  </q-layout>
</template>

<script>
import Terms from './Terms.vue'
export default {
  methods: {
    aceitou () {
      console.log('aceitou os termos')
    }
  },
  components: {
    Terms
  }
}
</script>
