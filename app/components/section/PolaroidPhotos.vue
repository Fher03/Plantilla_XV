<template>
  <div class="flex flex-col items-center h-fit w-screen xl:w-100 py-10 px-5">
    <NuxtImg
      v-for="(_, index) in new Array(8)"
      :key="index"
      :src="`/photos/polaroid_${index + 1}.png`"
    />
  </div>
</template>
