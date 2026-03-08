<template>
  <div
    class="relative flex flex-col items-center min-h-screen w-screen xl:w-120 py-12 px-6 overflow-hidden bg-[#fffdfb]"
  >
    <div
      v-motion
      :initial="{ opacity: 0, scale: 0.8 }"
      :visible="{ opacity: 0.5, scale: 1, transition: { duration: 2000 } }"
      class="absolute top-0 left-0 w-80 h-80 bg-pink-100/50 rounded-full blur-3xl -translate-x-1/2 -translate-y-1/2"
    />

    <div
      v-motion-slide-visible-once-top
      class="z-20 mb-6 flex flex-col items-center"
    >
      <div class="text-accent text-4xl -mb-2.5 opacity-70">❦</div>
      <div class="border-y border-accent/30 py-2 px-6">
        <span class="font-great-vibes text-4xl text-accent">Mis Quince</span>
      </div>
    </div>

    <div
      v-motion-slide-visible-once-bottom
      :delay="200"
      class="relative w-full max-w-md bg-white/60 backdrop-blur-md border border-pink-100 shadow-2xl rounded-3xl p-10 flex flex-col items-center z-10 overflow-hidden text-center"
    >
      <span
        v-motion
        :initial="{ opacity: 0, scale: 0.3 }"
        :visible-once="{
          opacity: 0.2,
          scale: 1,
          transition: { type: 'spring', stiffness: 50, delay: 500 },
        }"
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 font-serif text-[14rem] font-bold text-pink-200 select-none z-0"
      >
        15
      </span>

      <div class="relative z-10 flex flex-col items-center gap-6">
        <p
          v-motion-fade-visible-once
          :delay="600"
          class="text-gray-600 font-serif italic text-lg leading-relaxed px-2"
        >
          Hay momentos inolvidables que se atesoran para siempre por eso será
          muy especial si disfrutas a mi lado y junto a
        </p>
        <p
          v-motion-fade-visible-once
          :delay="700"
          class="text-gray-600 italic text-4xl font-great-vibes leading-relaxed px-2"
        >
          Mis Padres
        </p>

        <div class="flex flex-col gap-4 w-full mt-4">
          <div v-motion-fade-visible-once :delay="800">
            <p
              class="text-2xl font-light tracking-[0.15em] text-gray-700 uppercase leading-tight"
            >
              Luz Elena <br />
              Rodriguez Vázquez
            </p>
          </div>

          <div
            v-motion-fade-visible-once
            :delay="1000"
            class="h-px w-12 bg-yellow-200 mx-auto"
          />

          <div v-motion-fade-visible-once :delay="1200">
            <p
              class="text-2xl font-light tracking-[0.15em] text-gray-700 uppercase leading-tight"
            >
              Jorge Ernesto <br />
              Núñez de la Torre
            </p>
          </div>
        </div>
      </div>

      <NuxtImg
        v-motion
        :initial="{ opacity: 0, rotate: -45, scale: 0.5 }"
        :visible-once="{
          opacity: 1,
          rotate: 6,
          scale: 1,
          transition: { delay: 1400, type: 'spring' },
        }"
        class="absolute -bottom-10 -right-8 w-44 h-44 drop-shadow-sm"
        src="/flowers/flower_1.png"
      />
    </div>
    <div
      v-motion
      :initial="{ opacity: 0 }"
      :enter="{ opacity: 1, transition: { delay: 1500 } }"
      class="mt-8 z-10 text-center"
    >
      <div
        class="w-24 h-px bg-linear-to-r from-transparent via-accent to-transparent mb-2 mx-auto"
      />
      <p class="font-great-vibes text-2xl text-accent">XV Zoé</p>
    </div>
  </div>
</template>
