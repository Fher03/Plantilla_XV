<template>
  <div
    class="relative flex flex-col items-center min-h-screen w-screen xl:w-120 py-12 px-6 overflow-hidden bg-[#fffdfb]"
  >
    <div
      class="absolute top-0 left-0 w-80 h-80 bg-pink-100/50 rounded-full blur-3xl -translate-x-1/2 -translate-y-1/2"
    />
    <div
      class="absolute bottom-20 right-0 w-96 h-96 bg-yellow-100/40 rounded-full blur-3xl translate-x-1/3"
    />

    <div class="z-20 mb-6 flex flex-col items-center">
      <div class="text-[#d4a373] text-4xl mb-[-10px] opacity-70">❦</div>
      <div class="border-y border-[#d4a373]/30 py-2 px-6">
        <span class="font-great-vibes text-4xl text-[#cca47c]">Mis Quince</span>
      </div>
    </div>

    <div
      class="relative w-full max-w-md bg-white/60 backdrop-blur-md border border-pink-100 shadow-2xl rounded-3xl p-10 flex flex-col items-center z-10 overflow-hidden text-center"
    >
      <span
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 font-serif text-[14rem] font-bold text-pink-200/20 select-none z-0"
      >
        15
      </span>

      <div class="relative z-10 flex flex-col items-center gap-6">
        <h2 class="font-great-vibes text-5xl text-gray-800">Agradecimientos</h2>

        <p class="text-gray-600 font-serif italic text-lg leading-relaxed px-2">
          "De una manera muy especial, llena de alegría y gratitud por la vida
          que Dios me ha regalado."
        </p>

        <p class="font-serif italic text-xl text-[#d4a373] mt-2">
          Con la bendición de:
        </p>

        <div class="flex flex-col gap-4 w-full">
          <p
            class="text-2xl font-light tracking-[0.15em] text-gray-700 uppercase leading-tight"
          >
            Luz Elena <br />
            <span class="font-bold">Rodriguez Vázquez</span>
          </p>
          <div class="h-[1px] w-12 bg-yellow-200 mx-auto" />
          <p
            class="text-2xl font-light tracking-[0.15em] text-gray-700 uppercase leading-tight"
          >
            Jorge Ernesto <br />
            <span class="font-bold">Núñez de la Torre</span>
          </p>
        </div>

        <p
          class="mt-4 text-xs text-gray-400 font-light tracking-[0.2em] uppercase"
        >
          Celebrando la vida y la gratitud
        </p>
      </div>

      <NuxtImg
        class="absolute -bottom-10 -right-8 w-44 h-44 transform rotate-6 drop-shadow-sm"
        src="/flowers/flower_1.png"
        alt="Flores"
      />

      <NuxtImg
        class="absolute -top-12 -left-12 w-36 h-36 transform -rotate-45 opacity-60"
        src="/flowers/flower_1.png"
      />
    </div>

    <div class="mt-8 z-10 text-center">
      <div
        class="w-24 h-[1px] bg-gradient-to-r from-transparent via-[#d4a373] to-transparent mb-2 mx-auto"
      />
      <p class="font-great-vibes text-2xl text-[#cca47c]">XV Zoe</p>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap");

.font-great-vibes {
  font-family: "Great Vibes", cursive;
}
</style>
