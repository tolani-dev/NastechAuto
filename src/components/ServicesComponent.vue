<template>
    <div class=" sm:container w-full h-full mx-auto px-5 mt-10 md:mt-10 py-12">
        <div class="grid grid-cols-2 h-full w-full">
            <div
                class="2xl:justify-self-center w-full hidden lg:grid lg:min-h-[300px] lg:max-w-[400px] xl:min-h-[400px] xl:max-w-[500px] pl-14">
                <img src="/src/assets/oil1.jpeg" alt="" class="object-fill h-full">
            </div>
            <div class="justify-self-center mt-5 sm:mt-0 items-center">
                <p class="text-sm tracking-widest text-[#9E9E9E]">5 STAR AUTO SERVICE</p>
                <h2 class="font-bold text-gray-900 md:text-5xl">
                    <i
                        class="text-2xl sm:text-5xl block py-2 text-black font-light animate__animated animate__fadeInRight">Your
                        one stop
                        solution for auto repairs.
                    </i>
                    <p
                        class="block sm:w-[500px] lg:w-[500px] 2xl:w-[650px] animate__animated animate__fadeInRight animate__delay-1s font-bold">
                        servicing all makes and models.</p>

                </h2>
                <div class="pt-6">
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Heating and
                            cooling system service</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Complete
                            muffler and exhaust service</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Oil
                            changes</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Tire
                            repairs</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Brake
                            work</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Transmission
                            repairs</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Suspension
                            services</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Power
                            windows and door locks</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Air
                            conditioning services</span></p>
                    <p class="flex gap-6 leading-8"><span class="tracking-widest text-[#9E9E9E]">-</span><span
                            class="tracking-widest text-[#9E9E9E]">Engine diagnostics</span></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: "ServiceComponent",
    setup() {


        return {}
    }
})
</script>

<style scoped></style>