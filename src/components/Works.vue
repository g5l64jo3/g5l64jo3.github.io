<template>
  <a
    :href="info.url"
    class="group flex flex-col gap-6 rounded-md bg-white p-5 shadow-sm transition-shadow hover:shadow-lg sm:flex-row sm:items-start sm:gap-2"
    target="_blank"
    rel="noreferrer noopener"
  >
    <div class="w-80 flex-none flex items-end gap-2">
      <img
        :src="info.coverPc"
        class="max-h-32 max-w-60 rounded-md object-cover"
        :alt="`${info.name}_電腦版`"
      />
      <img
        v-if="info.coverM"
        :src="info.coverM"
        class="max-h-28 max-w-16 rounded-md object-cover"
        :alt="`${info.name}_手機版`"
      />
    </div>
    <div class="flex-1">
      <div class="mb-2 text-xl font-bold transition-colors group-hover:text-stone-500">
        {{ info.name }}
      </div>
      <ul class="list-disc pl-5 leading-7">
        <li v-for="item in info.list" :key="item">{{ item }}</li>
      </ul>
    </div>
  </a>
</template>

<script setup>
const props = defineProps({
  info: {
    type: Object,
    required: true,
  },
})
</script>
