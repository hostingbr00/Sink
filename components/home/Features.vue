<script setup>
import { Link, AreaChart, ServerOff, Paintbrush, Sparkles, Hourglass } from 'lucide-vue-next'

const features = ref([
  {
    title: 'Encurtamento de URL',
    description:
          'Comprima suas URLs ao seu comprimento mínimo.',
    icon: Link,
  },
  {
    title: 'Analytics',
    description:
          'Monitore a análise dos links e obtenha estatísticas perspicazes.',
    icon: AreaChart,
  },
  {
    title: 'Serverless',
    description:
          'Implante sem a necessidade de servidores tradicionais.',
    icon: ServerOff,
  },
  {
    title: 'Slug Personalizável',
    description:
          'Suporte para slugs personalizados.',
    icon: Paintbrush,
  },
  {
    title: 'Slug com IA',
    description:
          'Aproveite a IA para gerar slugs.',
    icon: Sparkles,
  },
  {
    title: 'Expiração de Link',
    description:
          'Defina datas de expiração para seus links.',
    icon: Hourglass,
  },
])
</script>

<template>
  <main class="pt-16 md:py-12">
    <div class="md:pb-12">
      <h2 class="text-4xl font-bold lg:text-5xl lg:tracking-tight">
        Funcionalidades
      </h2>
      <p class="my-8 text-lg md:mb-0 text-slate-600">
        Funcionalidade simples e suficiente
      </p>
    </div>

    <div class="grid gap-8 md:gap-16 sm:grid-cols-2 md:grid-cols-3">
      <div
        v-for="item in features"
        :key="item.title"
        class="flex items-start gap-4"
      >
        <div class="w-8 h-8 p-2 mt-1 bg-black rounded-full shrink-0">
          <component
            :is="item.icon"
            class="w-4 h-4 text-white"
          />
        </div>
        <div>
          <h3 class="text-lg font-semibold">
            {{ item.title }}
          </h3>
          <p class="mt-2 leading-relaxed text-slate-500">
            {{ item.description }}
          </p>
        </div>
      </div>
    </div>
  </main>
</template>
