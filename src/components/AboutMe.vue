<script setup lang="ts">
import { Icon } from '@iconify/vue'
const { t } = useI18n()
const props = defineProps({
  data: Object,
})
</script>

<template>
  <p class="line-break" v-html="t('about.me')"></p>

  <span v-for="( skill ) in data.skills" :key="skill.label">
    <span v-if="skill.main" :title="skill.label">
      <Icon class="zoom icon-margin content-icon color-default" :icon="skill.icon" /> </span>
  </span>

  <p class="line-break" v-html="t('about.me2')"></p>

  <span v-for="( skill ) in data.skills" :key="skill.label">
    <span v-if="skill.learning" :title="skill.label">
      <Icon class="zoom icon-margin content-icon color-default" :icon="skill.icon" /> </span>
  </span>
</template>

<style scoped>
.icon-margin {
  margin: 3px 3px 3px 3px
}

</style>
