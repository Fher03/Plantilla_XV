<script setup lang="ts">
import { ref } from "vue";

const emit = defineEmits(["start"]);

const isVisible = ref(true);
const isFading = ref(false);

const handleStart = () => {
  isFading.value = true;
  emit("start");
  setTimeout(() => {
    isVisible.value = false;
  }, 200);
};
</script>

<template>
  <Teleport to="body">
    <Transition name="paper-fade">
      <div
        v-if="isVisible"
        class="fixed inset-0 z-100 flex items-center justify-center bg-[#1a1a1a]/90 backdrop-blur-sm p-4"
        :class="{ 'pointer-events-none': isFading }"
      >
        <div class="relative w-full max-w-xl transform -rotate-1">
          <div
            class="relative aspect-5/4 bg-[#f2e8cf] shadow-2xl overflow-hidden flex flex-col items-center justify-center p-10 text-center"
            style="
              clip-path: polygon(
                2% 2%,
                97% 4%,
                100% 30%,
                98% 70%,
                100% 96%,
                50% 98%,
                1% 95%,
                0% 50%,
                3% 15%
              );
              border: 1px solid #d4c3a1;
            "
          >
            <div
              class="absolute inset-0 opacity-60 bg-[url('https://www.transparenttextures.com/patterns/aged-paper.png')] pointer-events-none"
            />

            <div
              class="absolute inset-0 shadow-[inner_0_0_50px_rgba(93,64,55,0.2)] pointer-events-none"
            />

            <div
              class="relative z-10 flex flex-col items-center h-full justify-between py-4"
            >
              <h1
                class="font-pinyon-script text-5xl md:text-6xl text-[#5d4037] leading-none mt-4"
              >
                Invitación Zoé
              </h1>

              <div class="relative mt-auto">
                <p class="font-pinyon-script text-[#8d6e63] text-2xl mb-2">
                  Toca para
                </p>

                <button
                  class="group relative w-24 h-24 transition-transform duration-300 hover:scale-110 active:scale-95 flex items-center justify-center"
                  @click="handleStart"
                >
                  <div
                    class="absolute inset-0 rounded-full bg-black/30 blur-md translate-y-2 translate-x-1"
                  />

                  <div
                    class="absolute inset-0 bg-[#a51d1d] rounded-full border-4 border-[#8b0000] shadow-[inner_0_0_15px_rgba(0,0,0,0.5)] transform group-hover:rotate-[-5deg] transition-transform"
                    style="
                      clip-path: polygon(
                        50% 0%,
                        85% 10%,
                        100% 40%,
                        95% 75%,
                        70% 95%,
                        50% 100%,
                        20% 95%,
                        5% 75%,
                        0% 40%,
                        15% 10%
                      );
                    "
                  />

                  <span
                    class="relative z-10 font-pinyon-script text-white text-3xl font-bold drop-shadow-[0_2px_2px_rgba(0,0,0,0.8)]"
                  >
                    Abrir
                  </span>

                  <div
                    class="absolute top-3 left-6 w-5 h-5 bg-white/20 rounded-full blur-sm pointer-events-none"
                  />
                </button>
              </div>
            </div>
          </div>

          <div
            class="absolute -top-2 -left-2 w-8 h-8 border-t-4 border-l-4 border-[#d4c3a1] rounded-tl-sm pointer-events-none"
          />
          <div
            class="absolute -bottom-2 -right-2 w-8 h-8 border-b-4 border-r-4 border-[#d4c3a1] rounded-br-sm pointer-events-none"
          />
        </div>

        <div
          class="absolute bottom-6 z-10 font-great-vibes text-4xl text-[#f2e8cf]/70 tracking-widest"
        >
          2026
        </div>
      </div>
    </Transition>
  </Teleport>
</template>

<style scoped>
/* Transición de salida: desvanecimiento suave */
.paper-fade-leave-active {
  transition:
    opacity 0.8s ease-in-out,
    transform 0.8s ease-in-out;
}
.paper-fade-leave-to {
  opacity: 0;
  transform: scale(0.9) translateY(20px);
}
</style>
