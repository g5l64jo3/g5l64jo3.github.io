<template>
  <div class="mx-auto max-w-screen-md px-4 py-20 text-stone-700">
    <div class="flex items-center gap-4 sm:gap-12">
      <img src="/img/avatar.jpg" class="w-1/3 sm:w-1/4" />
      <div class="grid gap-1">
        <div class="mb-2 flex items-end gap-3 sm:mb-3">
          <h1 class="text-3xl tracking-widest">黃懿瑢</h1>
          <span class="text-xl">Lea Huang</span>
        </div>
        <div class="group flex items-center gap-2">
          <PhoneIcon class="w-5 fill-lime-700 group-hover:fill-lime-800" />
          <a
            href="tel:0975425783"
            class="whitespace-nowrap text-lg text-lime-700 group-hover:text-lime-800"
          >
            0975-425-783
          </a>
        </div>
        <div class="group flex items-center gap-2">
          <EmailIcon class="w-5 fill-lime-700 group-hover:fill-lime-800" />
          <a
            href="mailto:g5l64jo3@gmail.com"
            class="text-lg text-lime-700 group-hover:text-lime-800"
          >
            g5l64jo3@gmail.com
          </a>
        </div>
      </div>
    </div>
    <ul class="mt-14 grid gap-8">
      <li class="flex flex-col gap-4 sm:flex-row">
        <h4 class="w-20 whitespace-nowrap font-bold sm:text-right">工作經歷</h4>
        <ul class="w-full">
          <li>
            <span class="text-sm text-gray-400">Aug 2020 - 現在</span>
            <p class="rounded-md bg-stone-100 px-4 py-3">
              擔任雄獅資訊 TGDS 團隊前端工程師，主要負責同業網前、後端開發，<br />
              也支援後端的供應商 api 串接、站內查詢 elk 維護、chrome extension 開發
            </p>
          </li>
          <li class="mt-3">
            <span class="text-sm text-gray-400">Aug 2015 - Jul 2020</span>
            <p class="rounded-md bg-stone-100 px-4 py-3">
              擔任運動筆記前端工程師，負責前端切版、edm、部分介面規劃、活動網站等<br />
              閒暇之餘自由接案、精進能力，同時也接觸不同的人事物增進溝通技巧
            </p>
          </li>
        </ul>
      </li>
      <li class="flex flex-col gap-4 sm:flex-row">
        <h4 class="w-20 font-bold sm:text-right">學歷</h4>
        <div class="w-full">
          <span class="text-sm text-gray-400">Sep 2011 - Jun 2015</span>
          <p class="rounded-md bg-stone-100 px-4 py-3">
            畢業於國立臺灣科技大學資訊工程系
          </p>
        </div>
      </li>
      <li class="flex flex-col gap-4 sm:flex-row">
        <h4 class="w-20 font-bold sm:text-right">技能</h4>
        <ul class="w-full rounded-md bg-stone-100 px-4 py-3">
          <li>前端：html, css, sass, javascript, jquery, vue2/3</li>
          <li>後端：php, mysql, git, laravel, elk, docker</li>
          <li>其他：ga, gtm</li>
        </ul>
      </li>
    </ul>
  </div>
  <div class="bg-stone-100">
    <div class="mx-auto grid max-w-screen-md gap-5 px-4 py-20 text-stone-700">
      <h2 class="mb-2 text-center text-2xl font-bold tracking-widest">專案開發</h2>
      <Works v-for="work in works" :key="work.name" :info="work" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import PhoneIcon from './assets/phone.svg'
import EmailIcon from './assets/email.svg'
import Works from './components/Works.vue'

const avatar = ref('/img/avatar.jpg')

const works = ref([
  {
    name: 'chrome extension',
    url: 'https://admin.roartrips.com/login',
    coverPc: '/img/extension_pc.jpg',
    coverM: '',
    list: ['維護訂房網站，使用 vue3 + quasar', '開發抓圖小工具簡化操作'],
  },
  {
    name: 'TGDS 同業網',
    url: 'https://tmp.ticketgds.com',
    coverPc: '/img/tgds_pc.jpg',
    coverM: '/img/tgds_m.jpg',
    list: ['網站、功能開發', '採用：vue3 前端框架 + Laravel api'],
  },
  {
    name: '運動筆記',
    url: 'https://running.biji.co',
    coverPc: '/img/running_pc.jpg',
    coverM: '/img/running_m.jpg',
    list: [
      '網頁切版',
      'dfp 串接',
      '無限加載文章，利用history api變更網址',
      '利用fabric.js製作圖片拼貼功能',
    ],
  },
  {
    name: '遊山茶訪',
    url: 'https://www.yoshantea.com',
    coverPc: '/img/tea_pc.jpg',
    coverM: '/img/tea_m.jpg',
    list: [
      '網頁切版',
      '後台可編輯產品、文章、活動，與資料庫串接',
      '發送email',
      'ga、search console設定',
    ],
  },
  {
    name: 'tokuyo 按摩椅',
    url: 'https://www.tokuyo.com.tw',
    coverPc: '/img/tokuyo_pc.jpg',
    coverM: '',
    list: ['網站維護，首次接觸MVC架構，Zend與smarty撰寫', 'nccc串接'],
  },
  {
    name: 'TOYOTA 認證中古車',
    url: 'https://www.toyotacpo.com.tw',
    coverPc: '/img/toyota_pc.jpg',
    coverM: '/img/toyota_m.jpg',
    list: ['RWD 網頁切版'],
  },
])
</script>
