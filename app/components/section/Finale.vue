<template>
  <div class="relative h-130 flex items-center justify-center">
    <h3
      class="relative font-great-vibes text-5xl leading-14 max-w-xs text-center"
    >
      Gracias por acompañarme en mi día especial
    </h3>
    <NuxtImg
      v-motion
      :initial="{ opacity: 0, rotate: -45, scale: 0.5 }"
      :visible-once="{
        opacity: 1,
        rotate: 6,
        scale: 1,
        transition: { delay: 1400, type: 'spring' },
      }"
      src="/flowers/flower_1.png"
      class="absolute top-0 -left-20 w-1/2"
    />
    <NuxtImg
      v-motion-fade-visible-once
      :delay="500"
      src="/flowers/flower_2.png"
      class="absolute -bottom-5 -right-15 w-4/5"
    />
  </div>
</template>
