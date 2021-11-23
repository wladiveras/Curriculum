<script setup lang="ts">
const { t } = useI18n()

const props = defineProps({
  project: Object,
})
</script>

<template>
  <h1 class="side-header">
    {{ t('project.header') }}
  </h1>
  <table class="border-collapse w-full">
    <thead>
      <tr>
        <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden text-center lg:table-cell max-list">
          {{ t('project.header') }}
        </th>
        <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden text-center lg:table-cell">
          {{ t('project.type') }}
        </th>
        <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden text-center lg:table-cell">
          {{ t('project.description') }}
        </th>
        <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden text-center lg:table-cell max-list">
          {{ t('project.technologies') }}
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="( P ) in props.project" :key="P.title" class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0 max-list">
        <td class="w-full lg:w-auto p-3 text-gray-800 text-center textborder border-b block lg:table-cell relative lg:static">
          <span class="lg:hidden absolute top-0 left-0 bg-blue-400px-2 py-1 text-xs font-bold uppercase">  {{ t('project.header') }}</span>
          <b class="dark-color">
            <a :href="P.url" target="_BLANK">{{ P.title }}</a>
          </b>
        </td>
        <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
          <span class="lg:hidden absolute top-0 left-0 bg-blue-400 px-2 py-1 text-xs font-bold uppercase">  {{ t('project.type') }}</span>
          <span class="rounded bg-yellow-400 py-1 px-3 text-xs font-bold">{{ P.type }}</span>
        </td>
        <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
          <span class="lg:hidden absolute top-0 left-0 bg-blue-400px-2 py-1 text-xs font-bold uppercase ">{{ t('project.description') }}</span>
          <span class="dark-color">{{ P.description }}</span>
        </td>

        <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static max-list">
          <span class="lg:hidden absolute top-0 left-0 bg-blue-400px-2 py-1 text-xs font-bold uppercase">{{ t('project.technologies') }}</span>
          <i v-for="( V, K ) in P.technology" :key="K" class="dark-color">
            {{ V }},
          </i>
        </td>
      </tr>
    </tbody>
  </table>
</template>
<style scoped>
.dark .bg-white {
  background-color: #22272e;
}
.dark .dark-color {
  color: #fff;
}

.dark *, ::before, ::after {
 border-color: #444c56;

}

.dark .bg-gray-200 {
  background: #2d333b;
  color: #adbac7;
}
</style>
