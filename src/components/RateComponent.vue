<template>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 parallax items-center p-12">
        <div class="flex flex-col items-center pb-5 md:mb-0">
            <p class="font-bold text-lg text-white">OVER</p>
            <p class="font-semibold tracking-[.2em] text-xl text-white">5000</p>
            <p><span class="font-extrabold text-xl text-white">HAPPY </span><span
                    class="italic text-lg tracking-widest text-white">CLIENTS</span></p>
        </div>
        <div class="flex flex-col items-center pb-5 sm:mb-0">
            <p class="font-bold text-lg text-white">OVER</p>
            <p class="font-semibold tracking-[.2em] text-xl text-white">10000</p>
            <p><span class="font-extrabold text-xl text-white">CARS </span><span
                    class="italic text-lg tracking-widest text-white">FIXED</span></p>
        </div>
        <div class="flex flex-col items-center pb-5 md:mb-0">
            <p class="font-bold text-lg text-white">OVER</p>
            <p class="font-semibold tracking-[.2em] text-xl text-white">250</p>
            <p><span class="font-extrabold text-xl text-white">MAKES/MODELS </span><span
                    class="italic text-lg tracking-widest text-white">SERVICED</span></p>
        </div>
        <div class="flex flex-col items-center pb-5 md:mb-0">
            <p class="font-bold text-lg text-white">OVER</p>
            <p class="font-semibold tracking-[.2em] text-xl text-white">500</p>
            <p><span class="font-extrabold text-xl text-white">SERVICE </span><span
                    class="italic text-lg tracking-widest text-white">AVAILABLE</span></p>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "RateComponent",
    setup() {


        return {}
    }
})
</script>

<style scoped>
.parallax {
    /* The image used */
    background-image: url("/src/assets/keys.png");

    /* Set a specific height */
    min-height: 250px;

    /* Create the parallax scrolling effect */
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

@media only screen and (max-device-width: 1366px) {
    .parallax {
        background-attachment: scroll;
    }
}
</style>