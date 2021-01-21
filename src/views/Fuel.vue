<template>
    <div>
        <div class="mb-4 tracking-widest text-sm font-light">
            FUEL CALCULATOR
        </div>
        <form>
            <div class="grid grid-cols-2 gap-x-2 items-center gap-y-4">
                <div class="text-xl col-span-1">
                    Lap time
                </div>
                <div class="grid grid-cols-4 gap-2 items-center">
                    <input type="number" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200" min="0" max="60" v-model="lapTimeMin">
                    min
                    <input type="number" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200" min="0" max="60" v-model="lapTimeSec">
                    sec
                </div>
                 <div class="text-xl col-span-1">
                    Stint Length
                </div>
                <div class="grid grid-cols-4 gap-2 items-center">
                    <input type="number" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200" v-model="stintLength">
                    min
                </div>
                 <div class="text-xl col-span-1">
                    Litres per Lap
                </div>
                <div class="grid grid-cols-4 gap-2 items-center">
                    <input type="number" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200" v-model="litres">
                    L
                </div>
            </div>
            <div class="grid grid-cols-2 gap-2 mt-4">
            </div>
            <div class="my-4 bg-blue-700 hover:bg-blue-800 text-center p-4 rounded-lg active:bg-black cursor-pointer select-none text-white font-semibold" @click="calculate()">
                Calculate
            </div>
        </form>
        <div class="grid grid-cols-2 gap-4">
            <div class="bg-gray-800 rounded-lg p-8">
                <div>
                    Risky Fuel
                </div>
                <div class="text-6xl">
                    {{fuel||0}}<span class="text-sm text-gray-500 ml-2">Litres</span>
                </div>
            </div>
            <div class="bg-gray-800 rounded-lg p-8">
                <div>
                    Safe Fuel
                </div>
                <div class="text-6xl">
                    {{fuel+litres*2}}<span class="text-sm text-gray-500 ml-2">Litres</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            lapTimeMin: '',
            lapTimeSec: '',
            stintLength: '',
            litres: '',
            laptime: '',
            fuel: '',
            laps: '',
        }
    },
    methods: {
        calculate() {
            this.laptime = parseInt(this.lapTimeMin*60)+parseInt(this.lapTimeSec);
            this.laps = (parseInt(this.stintLength)*60)/parseInt(this.laptime);
            this.fuel = Math.round(this.laps*(Number(this.litres)))
        }
    }
}
</script>