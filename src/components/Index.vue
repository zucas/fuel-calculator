<template>
  <q-layout>
    <img src="https://c1.staticflickr.com/1/206/478962457_72b41c1678_b.jpg" class="fit fullscreen responsive" alt="">
    <div slot="header" class="toolbar dark">
      <q-toolbar-title :padding="0">
        Sim Fuel Calculator by Davi Zucas - v0.1a
      </q-toolbar-title>
    </div>

    <!--
      Replace following "div" with
      "<router-view class="layout-view">" component
      if using subRoutes
    -->
    <div class="layout-view">
      <div class="layout-padding">
        <div>
          <Terms @aceitou="aceitou"></Terms>
          <br>
          <br>
          <Calculator></Calculator>
        </div>
      </div>
    </div>
  </q-layout>
</template>

<script>
import Terms from './Terms.vue'
import Calculator from './Calculator.vue'
export default {
  methods: {
    aceitou () {
      console.log('aceitou os termos')
    }
  },
  components: {
    Terms,
    Calculator
  }
}
</script>
