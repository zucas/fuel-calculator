<template>
  <q-layout>
    <img src="http://cdn.airplane-pictures.net/images/uploaded-images/2012/11/9/248722.jpg" class="fit fullscreen responsive" alt="">
    <div slot="header" class="toolbar dark">
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
      <div class="row">
        <div>
          <Calculator></Calculator>
          <Terms @aceitou="aceitou"></Terms>
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
