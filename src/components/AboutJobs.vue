<script setup lang="ts">
const props = defineProps({
  job: Object,
})
</script>
<template>
  <h1 class="side-header">
    Professional experience
  </h1>
  <div class="p-4 md:p-10">
    <div class="md:flex">
      <div class="text-left">
        <div class="relative mt-5 text-left">
          <!-- something -->
          <div v-for="( V, K ) in props.job" :key="K" class="flex items-center relative">
            <div class="hidden md:block w-20">
              <div class="font-bold italic">
                {{ V.year.start }} <span v-if="V.year.end"> - {{ V.year.end }}</span>
              </div>
              <div class="md:flex space-x-1 text-xs">
                <div>{{ V.month.start }}</div>
                <div>-</div>
                <div>{{ V.month.end }}</div>
              </div>
            </div>

            <div class="border-r-2 border-black absolute h-full left-1 md:left-20 top-2 z-10">
              <i class="fas fa-circle -top-1 -ml-2 absolute"></i>
            </div>

            <div class="ml-10">
              <div class="font-bold">
                {{ V.title }}
              </div>
              <div class="italic md:mb-4">
                {{ V.company }}
              </div>
              <div class="mb-4 mt-2 md:hidden">
                <div class="font-bold">
                  {{ V.year.start }} <span v-if="V.year.end"> - {{ V.year.end }}</span>
                </div>
                <div class="text-xs">
                  <div>{{ V.month.start }}</div>
                  <div>-</div>
                  <div>{{ V.month.end }}</div>
                </div>
              </div>
              <div class="mb-10">
                {{ V.description }}
              </div>
            </div>
          </div>
          <!-- something -->
        </div>
      </div>
    </div>
  </div>
</template>
