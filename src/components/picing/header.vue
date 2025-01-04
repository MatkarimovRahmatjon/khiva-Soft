<template>
  <div class="container text-[#282938]">
    <div class="flex flex-col items-center justify-center">
      <div class="text-center max-w-[562px] w-full">
        <h1
          class="font-semibold mt-[128px] mb-[16px] text-[48px] leading-[64px]"
        >
          Our Pricing Plans
        </h1>
        <p class="opacity-[70%]">
          When you’re ready to go beyond prototyping in Figma, Webflow is ready
          to help you bring your designs to life — without coding them.
        </p>
      </div>
    </div>

    <div class="flex justify-between mb-32">
        <div class="my-16 relative" v-for="item in card">
          <img :src="item.ellipse" alt="" class="absolute">
        <div :class="`bg-[${item.bg}] text-[${item.textColor}]`" class="p-14 h-full rounded-xl w-full max-w-[406px]">
          <div class="flex items-center">
            <h1 class="font-semibold mr-2 text-[38px] leading-[56px]">
              {{ item.price }}
            </h1>
            <p class="text-[16px] leading-7" :class="`text-[${item.disigncolor}]`">{{ item.disign }}</p>
          </div>
          <h1 class="text-2xl leading-9 mt-5">{{ item.title }}</h1>
          <p class="opacity-[70%] font-medium text-[16px] leading-7 mt-2 w-72 max-h-[85px] h-full">
            {{ item.text }}
          </p>
          <div class="mt-9">
            <div class="flex mb-6">
              <img :src="item.img" alt="" class="min-w-[26px]" />
              <h1 class="ml-2 text-[16px] leading-7">
                {{ item.text1 }}
              </h1>
            </div>
            <div class="flex mb-6">
              <img :src="item.img" alt="" class="min-w-[26px]" />
              <h1 class="ml-2 text-[16px] leading-7">
                {{ item.text2 }}
              </h1>
            </div>
            <div class="flex mb-6">
              <img :src="item.img" alt="" class="min-w-[26px]" />
              <h1 class="ml-2 text-[16px] leading-7">
                {{ item.text3 }}
              </h1>
            </div>
            <div class="flex mb-6">
              <img :src="item.img" alt="" class="min-w-[26px]" />
              <h1 class="ml-2 text-[16px] leading-7">
                {{ item.text4 }}
              </h1>
            </div>
            <div class="flex">
              <img :src="item.img" alt="" class="min-w-[26px]" />

              <h1 class="ml-2 text-[16px] leading-7">
                {{ item.text5 }}
              </h1>
            </div>
          </div>

          <button
            :class="`bg-[${item.btn}] text-[${item.btnColor}]`"
            class="ml-[40px] px-[78px] py-4 rounded-[41px] mt-20" 
          >
            {{ item.button }}
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const card = ref([

    {
        disigncolor:'#2405F2',
        btnColor:'#F4F6FC',
        btn: '#282938',
        textColor: '#282938',
        price: '$299',
        disign: 'Per Design',
        title: 'Landing Page ',
        text: 'When you’re ready to go beyond prototyping in Figma, ',
        bg: '#F4F6FC',
        img: '/public/img/Pointer.png',
        button: 'Get started',
        text1: 'All limited links',
        text2: 'Own analytics platform',
        text3: 'Chat support',
        text4: 'Optimize hashtags',
        text5: 'Unlimited users',
    },
    {
        disigncolor:'#FCD980',
        btnColor:'#282938',
        btn: '#FCD980',
        textColor: '#FFFFFF',
        price: '$399',
        disign: 'Multi Design',
        title: 'Website Page',
        text: 'When you’re ready to go beyond prototyping in Figma, Webflow’s ready to help.',
        bg: '#1C1E53',
        img: '/public/img/Pointer.png',
        ellipse: '/public/img/Ellipse.png',
        button: 'Get started',
        text1: 'All limited linksv',
        text2: 'Own analytics platform',
        text3: 'Chat support',
        text4: 'Optimize hashtags',
        text5: 'Unlimited users',
    },
    {
        disigncolor:'#2405F2',
        btnColor:'#F4F6FC',
        btn: '#282938',
        textColor: '#282938',
        disign: 'Per Design',
        price: '$499 +',
        title: 'Complex Project',
        text: 'When you’re ready to go beyond prototyping in Figma,',
        bg: '#F4F6FC',
        img: '/public/img/Pointer.png',
        button: 'Contact US',
        text1: 'All limited linksv',
        text2: 'Own analytics platform',
        text3: 'Chat support',
        text4: 'Optimize hashtags',
        text5: 'Unlimited users',
        text6: 'Assist and Help',
    },

]
)
</script>

<style lang="scss" scoped></style>
