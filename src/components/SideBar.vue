<script setup>
import {defineEmits} from 'vue';

const emits = defineEmits(['selectOption'])

const selectOption = (isColor) => {
  emits("selectOption", isColor)
}
</script>

<template>
  <VNavigationDrawer
    expand-on-hover
    rail
  >
    <VList>
      <VListItem
          prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
          title="Sandra Adams"
          subtitle="sandra_a88@gmailcom"
      ></VListItem>
    </VList>
    <VDivider/>
    <VList density="compact" nav>
      <VListItem
      prepend-icon="mdi-image"
      title="Color Galery"
      value="color"
      @click="selectOption(true)">
      </VListItem>
      <VListItem
          prepend-icon="mdi-dialpad"
          title="Grayspace Galery"
          value="color"
          @click="selectOption(false)"
      >
      </VListItem>

    </VList>
  </VNavigationDrawer>
</template>