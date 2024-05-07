<template>
  <header v-if="route.meta" class="w-full bg-white fixed mb-20 top-0 z-30 left-0 right-0 lg:shadow-xl rounded-b">

    <div
      class="hidden justify-between p-5 items-center lg:container md:max-w-[100%] lg:max-w-[85%] mx-auto md:flex h-[12vh]">
      <div class="w-[80px] md:w-[120px] lg:w-[200px]">
        <a href="/"><img src="/src/assets/logo4.png" alt="logo logo" class="object-fill"></a>
      </div>
      <div>
        <div class="flex items-center sm:gap-5 lg:gap-10">
          <a href="/">
            <div
              class="capitdivze font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary">
              Home
            </div>
          </a>

          <div
            class="capitalize font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary">
            <a href="/#ourservice"> services</a>
          </div>
          <div
            class="capitalize font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary">
            <a href="/#review"> about us</a>
          </div>

          <div
            class="capitalize font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary">
            <a href="/#callback">contact</a>
          </div>

          <!-- <div
              class="capitalize font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary"
            >
              <a
                href="http://medium.com/@logong"
                target="_blank"
                rel="noopener"
                >press & media
              </a>
            </div> -->
          <!-- <div
            class="capitalize font-semibold text-primary text-sm md:text-base cursor-pointer border-b border-transparent hover:border-b-4 hover:border-secondary">
            <a href="">press</a>
          </div> -->
        </div>
      </div>

      <div
        class="bg-primary text-white font-semibold text-sm px-5 py-2 rounded-full capitalize cursor-pointer hover:bg-indigo">
        <a href="#qr">Book an appointment</a>
      </div>
    </div>
    <!--  -->

    <!-- Mobile view -->
    <div v-if="drawerModal == true" id="navDrawer"
      class="w-[50%] h-screen md:hidden flex flex-col bg-black absolute top-0 rounded-b pt-5 pb-10 shadow" :class="drawerModal
    ? 'animate__animated animate__slideInLeft'
    : 'animate__animated animate__slideOutLeft'
    ">
      <div class="mb-3">
        <button @click="closeNav" id="closeNav"
          class="ml-5 bg-primary text-white py-2 px-4 hover:bg-indigo rounded-full cursor-pointer">
          x
        </button>
      </div>

      <div class="flex justify-between p-4 h-full">
        <div class="space-y-7">
          <div class="capitalize font-semibold text-primary text-sm cursor-pointer border-b border-transparent">
            <a href="/#home" @click="closeNav()"> home</a>
          </div>

          <div class="capitalize font-semibold text-primary text-sm cursor-pointer border-b border-transparent">
            <a href="/#review" @click="closeNav()">about us</a>
          </div>

          <div class="capitalize font-semibold text-primary text-sm cursor-pointer border-b border-transparent">
            <a @click="closeNav()" href="/#ourservice">services</a>
          </div>
          <div @click="closeNav()"
            class="capitalize font-semibold text-primary text-sm cursor-pointer border-b border-transparent">
            <a href="#callback">contact us </a>
          </div>
          <!-- <div @click="closeNav()"
            class="capitalize font-semibold text-primary text-sm cursor-pointer border-b border-transparent">
            <a href="" target="_blank" rel="noreferrer noopener">press
            </a>
          </div> -->
          <button @click="closeNav()"
            class="bg-primary mt-5 flex justify-center items-center mx-auto text-white font-semibold text-sm px-5 py-2 rounded-full capitalize cursor-pointer hover:bg-indigo">
            <a href="#qr">Book an appointment</a>
          </button>
        </div>
      </div>
    </div>

    <div @click="openNav" id="openNav" class="pt-5 pl-5 md:hidden cursor-pointer">
      <img src="/src/assets/icons/menu.svg" alt="">
    </div>
  </header>
  <router-view />
  <footer>
    <div class="bg-black-light">
      <div class="grid md:grid-cols-2 lg:grid-cols-4 m-auto w-[80%] p-14">
        <div>
          <img src="/src/assets/logo4.png" alt="logo" class="w-[70px]" />
          <p class="text-[#9E9E9E]">1508 trce abor ......</p>
          <p><span class="font-bold text-[#9E9E9E]">email:</span><span class="text-[#9E9E9E]">nasauto@gmail.com</span>
          </p>
          <p><span class="text-[#9E9E9E]">phone:</span><span class="text-[#9E9E9E]">08080815307</span></p>
        </div>
        <div>
          <p class="text-white font-extrabold mb-5">SHOP HOUR</p>
          <p><span class="font-bold text-[#9E9E9E]">monday-friday:</span><span class="text-[#9E9E9E]">8:30 AM - 5:30
              PM</span></p>
          <p><span class="text-[#9E9E9E]">Saturday:</span><span class="text-[#9E9E9E]">Please call</span></p>
          <p><span class="text-[#9E9E9E]">Sunday:</span><span class="text-[#9E9E9E]">Closed</span></p>
        </div>
        <div>
          <p class="text-white font-extrabold mb-5">RECENT POST</p>
          <p class="text-[#9E9E9E]">random text</p>
          <!-- <p><span class="font-bold text-[#9E9E9E]">email:</span><span class="text-[#9E9E9E]">nasauto@gmail.com</span>
          </p>
          <p><span class="text-[#9E9E9E]">phone:</span><span class="text-[#9E9E9E]">08080815307</span></p> -->
        </div>
        <div>
          <img src="/src/assets/logo4.png" alt="logo" class="w-[70px]" />
          <p class="text-[#9E9E9E]">1508 trce abor ......</p>
          <p><span class="font-bold text-[#9E9E9E]">email:</span><span class="text-[#9E9E9E]">nasauto@gmail.com</span>
          </p>
          <p><span class="text-[#9E9E9E]">phone:</span><span class="text-[#9E9E9E]">08080815307</span></p>
        </div>
      </div>
    </div>
    <div class="bg-black-shades grid grid-cols-2 p-4">
      <div>
        <p class="tracking-wide font-extralight">©2024 nasauto. All right reserved</p>
      </div>
      <div class="flex justify-end gap-2">
        <img src="/src/assets/instagram.png" alt="" class="w-4 h-4" />
        <img src="/src/assets/facebook.png" alt="" class="w-4 h-4" />
        <img src="/src/assets/google.png" alt="" class="w-4 h-4" />
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { RouterLink, RouterView, useRoute } from 'vue-router'
import { computed, defineComponent, ref } from 'vue'

export default defineComponent({
  name: "navbarComponent",
  components: {},
  setup() {
    const route = useRoute();
    const active = computed(() => route.path);
    const drawerModal = ref(false);

    const openNav = () => {
      console.log("hello");
      drawerModal.value = true;
    }
    const closeNav = () => {
      drawerModal.value = false
    }
    return {
      active,
      drawerModal,
      closeNav,
      openNav,
      route,
    }
  }
})

</script>
<style scoped></style>
