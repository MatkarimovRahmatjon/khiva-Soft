<template>
    <div class="container flex justify-between my-32">
        <div class="max-w-[400px]">
            <h1 class=" text-[48px] leading-[64px] text-[#282938]">Frequently asked questions</h1>
            <p class="text-[#2405F2] leading-8 text-[18px]">Contact us For More Info</p>
        </div>
        <div>
            <div v-for="item, index in card">
                <div class="my-8 flex justify-between max-w-[850px] w-full">
                    <div class="flex">
                        <span class="text-[24px] text-[#2405F2] leading-9 mr-[58px]">{{ item.num }}</span>
                        <div>
                            <h1 class="text-[#282938] text-[24px]">{{ item.title }}</h1>
                            <p v-if="item.hidden" class="mt-4 max-w-[604px] text-[18px] leading-8 text-[#282938]">
                                {{ item.text }}
                            </p>
                        </div>
                    </div>
                    <div @click="btn(index)">
                        <img src="../../../public/image/+.png" class="hover:rotate-45 duration-500 cursor-pointer"
                            alt="">
                    </div>
                </div>
                <img class="max-h-[1px] w-full" src="../../../public/image/qator.png" alt="">

            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";
const card = ref([
    {
        hidden: false,
        num: '01',
        title: 'How much time does it take ?',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    },
    {
        hidden: false,
        num: '02',
        title: 'What is your class naming convention ?',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    },
    {
        hidden: false,
        num: '03',
        title: 'How do we communicate ?',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    },
    {
        hidden: false,
        num: '04',
        title: 'I have a bigger project. Can you handle it ?',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    },
    {
        hidden: false,
        num: '05',
        title: 'What is your class naming convention ?',
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
    },
])

function btn(index) {
    card.value[index].hidden = !card.value[index].hidden;
}

</script>

<style scoped></style>