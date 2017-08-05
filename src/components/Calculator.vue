<template>

<div>
    <div class="card bg-white">
        <div class="card-title">
            <h5 class="light-paragraph">Fuel Calculator</h5>
        </div>
        <div class="card-content">
            <form>
                <div class="list">
                    <div class="list-label">Choose Aircraft Model</div>
                    <div class="item multiple-lines">
                        <i class="item-primary">airplanemode_active</i>
                        <div class="item-content">
                            <q-select class="full-width" type="list" v-model="select" :options="selectOptions"></q-select>
                        </div>
                    </div>
                </div>
                <div class="list">
                    <div class="list-label">Choose TRIP time (DEP to DEST in Minutes)</div>
                    <div class="item multiple-lines">
                        <i class="item-primary">schedule</i>
                        <div class="item-content">
                          <q-knob
                          v-model="trip_time"
                          :min="min"
                          :max="max"
                          ></q-knob>
                        </div>
                    </div>
                </div>
            </form>
        </div>
    </div>
</div>

</template>

<script>
import moment from 'moment'
export default {
    data() {
        return {
            select: 'a320',
            trip_time: 60,
            max: 360,
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
