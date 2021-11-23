<script setup lang="ts">
import { Icon } from '@iconify/vue'

const { t } = useI18n()

const props = defineProps({
  data: Object,
})

</script>
<template>
  <aside class="w-full sm:w-1/3 md:w-1/4 px-2">
    <div class="sticky top-0 p-4 w-full">
      <!-- navigation -->
      <ul class="flex flex-col overflow-hidden side">
        <li>
          <img class="avatar" src="../assets/images/imWladi.jpg" />
        </li>

        <li>
          <h1 class="side-header">
            {{ t('aside.contacts') }}
          </h1>
          <ul class="flex flex-col overflow-hidden side">
            <li v-for="( contact ) in data.contacts" :key="contact.label">
              <a :href="contact.value">
                <Icon class="side-link color-default" :icon="contact.icon" /> {{ contact.label }}
              </a>
            </li>
          </ul>
        </li>
        <li>
          <h1 class="side-header">
            {{ t('aside.technology') }}
          </h1>
          <ul class="flex block-inline flex-col overflow-hidden side">
            <li v-for="( skill ) in data.skills" :key="skill.label" :title="skill.label" class="inline skills-item">
              <Icon class="icon-skill" :icon="skill.icon" />
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </aside>
</template>
