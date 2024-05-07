<template>
    <div class="">
        <div class="flex flex-col justify-center items-center m-10">
            <h4 class="place-item"><span class="font-black text-5xl">Our</span><span class="italic text-5xl">
                    service</span></h4>
            <p class="tracking-wide text-[#9E9E9E] text-lg md:w-[30%] md:mt-0 mt-3 text-center">Integrity and value are critical pieces
                to the best
                automotive business practices</p>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 ">
            <div class="">
                <img src="/src/assets/oil1.jpeg" alt="bg" class="h-[40%] w-full" />
                <div class="w-[80%] mx-auto">
                    <h5 class="text-[#9E9E9E] font-extrabold text-xl my-4">SEMI-SYNTHETIC OIL CHANGE</h5>
                    <p class="italics mb-2 text-[#9E9E9E]">from $40</p>
                    <p>
                        Oil Change is comprehensive preventive maintenance to check, change, inspect, flush, fill and
                        clean essential systems and components of your vehicle..</p>
                </div>
            </div>
            <div class="bg-white-shades ">
                <img src="/src/assets/safety3.jpeg" alt="bg" class="h-[40%] w-full" />
                <div class="w-[80%] mx-auto">
                    <h5 class="text-[#9E9E9E] font-extrabold text-xl my-4">SAFETY STANDARDS CERTIFICATES</h5>
                    <p class="italics mb-2 text-[#9E9E9E]">from $40</p>
                    <p>
                        Buying or selling a vehicle? Have Lakeport Auto Service inspect your vehicle before you do
                        either. Our comprehensive inspection will give you piece of mind before making any expensive
                        decisions..</p>
                </div>
            </div>
            <div class="">
                <img src="/src/assets/diag2.jpeg" alt="bg" class="h-[40%] w-full" />
                <div class="w-[80%] mx-auto">
                    <h5 class="text-[#9E9E9E] font-extrabold text-xl my-4">COMPUTER DIOGNOSTICS</h5>
                    <p class="italics mb-2 text-[#9E9E9E]">from $40</p>
                    <p>
                        If your “check engine light” is on your car’s computer is telling you something is wrong. When
                        you see this the best thing is to bring in your car to Lakeport Auto Service so we can have a
                        look at what is going on..</p>
                </div>
            </div>
            <div class="bg-white-shades ">
                <img src="/src/assets/ac.jpeg" alt="bg" class="h-[40%] w-full" />
                <div class="w-[80%] mx-auto">
                    <h5 class="text-[#9E9E9E] font-extrabold text-xl my-4">A/C INSPECTION</h5>
                    <p class="italics mb-2 text-[#9E9E9E]">from $30</p>
                    <p>
                        Is your car A/C making you sweat? Bring it into Lakeport Auto Service for a complete inspection
                        of your cars air conditioning system. We'll help you keep cool for this summers road trip or
                        daily commute..</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "OurServiceComponent",
    setup() {


        return {}
    }
})
</script>

<style scoped></style>