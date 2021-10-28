<template>
  <div class="page--top-app-bar">
    <ui-top-app-bar
      title="Мерама"
      content-selector="#content-main"
      type="fixed"
    >

      <template #toolbar="{ toolbarItemClass }">
          <ui-icon-button
          icon="file_download"
          :class="toolbarItemClass"
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

    <div id="content-main">
      <!-- <p v-for="i in 36" :key="i">Content {{ i }}</p> -->
    </div>

  </div>
</template>