<template>
    <div class="grid lg:grid-cols-2 h-screen bg-black-light background">
        <div class="w-[80%] p-10 bg-white-shades m-auto">
            <div>
                <p class="tracking-widest text-[#9E9E9E] mb-6">REQUEST A CALL BACK</p>
                <h5 class="font-light text-5xl mb-8">We offer high quality, professional Auto Repair Services</h5>
                <p class="text-[#9E9E9E]">We have been in the Auto Repair business since 1986, providing our customers
                    with complete auto
                    repair
                    services and maintenance.</p>
            </div>
            <div class="mt-8">
                <form ref="formRef" @submit.prevent="sendEmail">
                    <div>
                        <label class="text-12 text-accent hidden sm:block">Your name</label>
                        <input type="name" v-model="callBackInput.name"
                            class="text-xs md:text-sm text-black h-14 block w-full border border-accent-shades mt-2 rounded-lg focus:outline-none focus:border-l-4 focus:border-l-primary p-3 bg-white mb-[5px]"
                            required placeholder="Enter Your name" tabindex="-1" />
                    </div>
                    <div>
                        <label class="text-12 text-accent hidden sm:block">Your email</label>
                        <input type="email" v-model="callBackInput.email"
                            class="text-xs md:text-sm text-black h-14 block w-full border border-accent-shades mt-2 rounded-lg focus:outline-none focus:border-l-4 focus:border-l-primary p-3 bg-white mb-[5px]"
                            required placeholder="Enter Your Email" tabindex="-1" />
                    </div>
                    <div>
                        <label class="text-12 text-accent hidden sm:block">Your phone</label>
                        <input type="number" v-model="callBackInput.phoneNumber"
                            class="text-xs md:text-sm text-black h-14 block w-full border border-accent-shades mt-2 rounded-lg focus:outline-none focus:border-l-4 focus:border-l-primary p-3 bg-white mb-[5px]"
                            required placeholder="Enter Your Number" tabindex="-1" />
                    </div>
                    <button tabindex="-1" type="submit"
                        class="mt-7 w-full md:h-12 h-10 md:text-sm text-xs p-2 text-white rounded-md border-0 active:bg-black focus:bg-black hover:bg-gray-700 bg-black m-1 flex justify-center items-center"
                        style="color: white">
                        <span>Send</span>
                        <!-- <spinSpinner v-else /> -->
                    </button>
                </form>
            </div>
        </div>
        <div>
            <!-- <img src="/src/assets/callback.png" alt="reg" class="h-" /> -->
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref } from 'vue'
import emailjs from 'emailjs-com';

export default defineComponent({
    name: "CallbackComponent",
    setup() {
        const formRef = ref<HTMLFormElement | null>(null)
        const callBackInput = reactive({
            name: '',
            phoneNumber: '',
            email: '',
        })
        //     const sendEmail = () => {
        //    emailjs.send('service_yionyvi', 'template_q3n71uv', {
        //     to_email: "giwafauzziyyah@gmail.com",
        //     subject: "Some needs a call back",
        //     message: `call ${callBackInput.name} on ${callBackInput.phoneNumber} or email ${callBackInput.email}`
        //   }, 'YOUR_USER_ID')
        //   .then((response) => {
        //     console.log('Email sent:', response);
        //     // Handle success response
        //   }, (error) => {
        //     console.error('Error sending email:', error);
        //     // Handle error response
        //   });
        // };
        const sendEmail = () => {
            if (formRef.value) { // Ensure that formRef.value is not null
                emailjs
                    .sendForm('service_yionyvi', 'template_kog8op3', formRef.value, 'xGVQsYWVnkqgQ1-xM',)
                    .then(
                        (response) => {
                            console.log('form', formRef.value)
                            console.log('SUCCESS!', response);
                            callBackInput.name = '';
                            callBackInput.email = '';
                            callBackInput.phoneNumber = '';
                        },
                        (error) => {
                            console.log('FAILED...', error.text);
                        },
                    );
            } else {
                console.error('Form element not found!');
            }
        };
    return {
        callBackInput,
        sendEmail,
        formRef,
    }
}
})
</script>

<style scoped>
.background {
    background: url("/src/assets/callback.png");

    /* background-position: center; */
    background-repeat: no-repeat;
    background-size: cover;
    /* height: fit-content; */
    height: 100vh;
    width: 100vw;
    /* background-position: left; */
}
</style>