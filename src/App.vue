<script setup lang="ts">
import { ref } from 'vue';
import Job from './types/Job'
import OrderTerm from './types/OrderTerm'

const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])

const order = ref<OrderTerm>('title')

const handleClick = (term: OrderTerm) => {
  order.value = term
}
</script>

<template>
  <div class="app grid justify-center content-center">
    <div class="flex bg-white w-[730px] h-[280px] overflow-hidden rounded-[10px] drop-shadow-[0_40px_40px_rgba(201,213,225,0.5)]">
      <div class="bg-cover flex-none bg-[url('/drawers.jpg')] bg-black w-[285px]">
      </div>
      <div class="pt-[32px] px-[40px]">
        <p class="text-[20px] font-bold text-[#48556A]">
          Shift the overall look and feel by adding these wonderful touches to furniture in your home  
        </p>
        <p class="mt-[14px] leading-1 text-[#6E8098] text-[13px]">
          Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I’ve got some simple tips to help you make any room feel complete.
        </p>
        <div class="flex mt-[20px] justify-between">
          <div class="flex text-[13px]">
            <img src="/avatar-michelle.jpg" class="rounded-full mr-[16px] w-[40px] h-[40px]" alt="Avatar Michelle">
            <div>
              <span class="font-bold">Michelle Appleton</span><br>
              28 June 2020
            </div>
          </div>
          <div>
            <div class="grid justify-center rounded-full content-center w-[32px] h-[32px] bg-[#ECF2F8]" >
              <img src="/icon-share.svg" class="w-[15px] h-[13px]" alt="Share Icon">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
body, html, #app, .app {
  background-color: #ECF2F8;
  height: 100%;
  font-family: 'Manrope', sans-serif;
}
</style>
