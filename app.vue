<template>
  <div class="flex justify-center h-screen items-start bg-gray-100 pt-20">
    <div class="border p-8 w-96 bg-white flex flex-col gap-8">
      <h1 class="text-xl font-medium">Criador de Cartões de Natal Virtual</h1>
      <div class="border aspect-square banner-here relative" v-html="svg"></div>
      <form class="flex flex-col gap-4">
        <input type="text" v-model="form.name" class="px-4 py-1 border w-full" placeholder="Digite o nome" />
        <input type="text" v-model="form.greeting" class="px-4 py-1 border w-full" placeholder="Digite a saudação" />
        <input type="file" accept=".png, .jpg, .jpeg" @change="handleFileChange" class="px-4 py-1 border w-full" />
        <small class="text-gray-400">Só são aceitas imagens menores que 100kb, nos formatos png, jpeg ou jpg.</small>
        <button class="bg-indigo-500 text-white px-4 py-2" @click.prevent="downloadSvgAsJpeg(svg)">Baixar</button>
      </form>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>
