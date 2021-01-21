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
                    <input type="text" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200">
                    min
                    <input type="text" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200">
                    sec
                </div>
                 <div class="text-xl col-span-1">
                    Stint Length
                </div>
                <div class="grid grid-cols-4 gap-2 items-center">
                    <input type="text" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200">
                    min
                </div>
                 <div class="text-xl col-span-1">
                    Litres per Lap
                </div>
                <div class="grid grid-cols-4 gap-2 items-center">
                    <input type="text" class="dark:bg-gray-800 rounded p-1 text-center bg-gray-200">
                    L
                </div>
            </div>
            <div class="grid grid-cols-2 gap-2 mt-4">
                <div class="bg-gray-800 rounded-md text-center p-3">
                    Full Formation Lap
                </div>
                <div class="bg-gray-800 rounded-md text-center p-3">
                    Simple Formation Lap
                </div>
            </div>
            <div class="my-4 bg-gray-700 text-center p-4 rounded-lg hover:bg-gray-800 active:bg-black cursor-pointer select-none">
                Calculate
            </div>
        </form>
    
    </div>
</template>