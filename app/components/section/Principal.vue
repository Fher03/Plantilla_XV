<template>
  <div
    class="relative bg-[url(/photos/principal.jpg)] bg-center bg-cover bg-no-repeat w-full h-screen md:bg-contain"
  >
    <div class="absolute z-1 bg-black/30 bg-center w-full h-full" />
    <div
      class="flex z-2 relative flex-col items-center justify-between h-full py-10"
    >
      <div>
        <h1 class="text-7xl text-center text-primary font-pinyon-script">
          Zoé Valentina
        </h1>
        <h2 class="text-3xl text-center text-primary font-great-vibes">
          Mis XV
        </h2>
      </div>

      <CountDown />
    </div>
  </div>
</template>
