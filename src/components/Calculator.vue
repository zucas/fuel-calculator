<template>

<div>
    <div class="card bg-white">
      <div class="toolbar">

  <q-toolbar-title :padding="1">
    Sim Fuel Calculator
  </q-toolbar-title>
</div>
        <div class="card-content">
            <form>
                <div class="list no-border">
                    <div class="list-label">Choose Aircraft Model</div>
                    <div class="item multiple-lines">
                        <i class="item-primary">airplanemode_active</i>
                        <div class="item-content">
                            <q-select class="full-width" type="list" v-model="select" :options="selectOptions"></q-select>
                        </div>
                    </div>
                </div>
                <div class="row text-center">
                  <div class="list no-border">
                      <div class="list-label">Choose TRIP time (DEP to DEST in Minutes)</div>
                      <div class="item multiple-lines">
                          <i class="item-primary">schedule</i>
                          <div class="item-content">
                            <q-knob
                            v-model="trip_time"
                            :min="min"
                            :max="max"
                            step="10"
                            ></q-knob>
                          </div>
                      </div>
                  </div>
                  <div class="auto">

                  </div>
                  <div class="list no-border">
                      <div class="list-label">Choose ALTN TRIP time (DEST to ALTN1 in Minutes)</div>
                      <div class="item multiple-lines">
                          <i class="item-primary">schedule</i>
                          <div class="item-content">
                            <q-knob
                            v-model="trip_altn"
                            :min="min"
                            :max="maxAlt"
                            step="10"
                            ></q-knob>
                          </div>
                      </div>
                  </div>
                </div>
            </form>
        </div>
        <div class="card-content">
          <div class="row">
            <div class="auto">

            </div>
            <div class="width-2of5">
                <div class="card text-center bg-green text-white">
                  <div class="card-content">
                    <h5> <i>local_gas_station</i> Total Fuel</h5>
                    <h3> {{ (((trip_time * 0.1) + trip_time) * consumo_por_min) + (trip_altn * consumo_por_min) + (30 * 36.6)  }} Kg </h3>
                  </div>
                </div>
            </div>
            <div class="auto">

            </div>
          </div>
        </div>
    </div>
</div>

</template>

<script>
export default {
  data () {
    return {
      consumo_por_min: 39,
      select: 'a320',
      trip_time: 60,
      trip_altn: 35,
      min: 10,
      maxAlt: 90,
      max: 361,
      selectOptions: [{
          label: 'Airbus A319',
          value: 'a319'
      }, {
          label: 'Airbus A320',
          value: 'a320'
      }, {
          label: 'Boeing B737-700',
          value: 'b737'
      }, {
          label: 'Boeing B737-800',
          value: 'b738'
      }]
    }
  }
}

</script>
