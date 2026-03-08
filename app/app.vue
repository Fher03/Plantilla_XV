<script setup lang="ts">
import { ref } from "vue";

const audioElement = ref<HTMLAudioElement | null>(null);

// Esta función se ejecuta CUANDO EL USUARIO HACE CLIC en el botón de la portada
const handleInitEffects = () => {
  if (audioElement.value) {
    // El navegador ya permite el audio porque esto proviene de un evento de clic
    audioElement.value.play().catch((error) => {
      console.error("Error al reproducir audio:", error);
    });
  }
};
</script>

<template>
  <SectionWelcomeCover @start="handleInitEffects" />

  <main
    class="bg-[url(/bg.jpg)] bg-repeat flex flex-col items-center min-h-screen"
  >
    <audio ref="audioElement" loop preload="auto">
      <source src="/music/kiss_me.mp3" type="audio/mpeg" />
      Tu navegador no soporta audio.
    </audio>

    <SectionPrincipal />
    <SectionGratitude />
    <SectionWhereAndWhen />
    <SectionDressCode />
    <SectionUploadPhotos />
    <SectionPolaroidPhotos />
    <SectionFinale />
    <SectionContactUs />
  </main>
</template>
