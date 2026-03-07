<template>
  <div
    class="flex flex-col items-center h-fit w-screen xl:w-120 py-10 px-5 gap-8 overflow-x-hidden"
  >
    <NuxtImg
      v-for="(_, index) in 8"
      :key="index"
      v-motion
      :initial="{
        opacity: 0,
        /* Salen desde los laterales (Par: izquierda, Impar: derecha) */
        x: index % 2 === 0 ? -200 : 200,
        /* Rotación inicial sutil para el efecto de vuelo */
        rotate: index % 2 === 0 ? -15 : 15,
        scale: 0.9,
      }"
      :visible-once="{
        opacity: 1,
        x: 0,
        /* Quedan con una inclinación muy leve y elegante */
        rotate: index % 2 === 0 ? -2 : 2,
        scale: 1,
        transition: {
          type: 'spring',
          stiffness: 40 /* Movimiento más suave y menos rígido */,
          damping: 18 /* Controla el rebote para que sea fino */,
          mass: 1 /* Peso equilibrado */,
          delay: 150 /* Tiempo de espera para que el usuario empiece a ver la sección */,
        },
      }"
      :src="`/photos/polaroid_${index + 1}.png`"
      class="w-80 h-auto"
    />
  </div>
</template>
