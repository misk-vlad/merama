<template>
  <ui-top-app-bar
    title="Мерама"
    content-selector=""
    type="1"
  >

    <template #toolbar="{ toolbarItemClass }">
        <ui-icon-button
        icon="file_download"
        :class="toolbarItemClass"
        @click="onclick"
        ></ui-icon-button>
        <ui-icon-button 
        icon="print"
        :class="toolbarItemClass"
        ></ui-icon-button>
        <ui-icon-button
        icon="bookmark"
        :class="toolbarItemClass"
        ></ui-icon-button>
    </template>

    <template #nav-icon>
      <ui-icon size="48">storm</ui-icon>
    </template>

  </ui-top-app-bar>
</template>

<script>
export default {
  methods: {
    onclick() {
      alert("hello")
    }
  }
}
</script>