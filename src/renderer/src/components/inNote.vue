<template>
  <button class="flex py-3 px-3.5 border-b w-full border-b-border hover:bg-hover duration-200">
    <img src="../assets/material_symbols/markdown.svg" alt="Markdown: " v-if="type === 'md'">
    <img src="../assets/material_symbols/notes.svg" alt="Plaintext: " v-else-if="type === 'txt'">
    <img src="../assets/material_symbols/contract.svg" alt="Scrap: " v-else-if="type === 'scrap'">
    <img src="../assets/material_symbols/image.svg" alt="Image: " v-else-if="type === 'png' || type === 'jpg' || type === 'jpeg' || type === 'webp' || type === 'gif'">
    <img src="../assets/material_symbols/check_box.svg" alt="Todo: " v-else-if="type === 'todo'">
    <img src="../assets/material_symbols/movie.svg" alt="Video: " v-else-if="type === 'mp4'">
    <img src="../assets/material_symbols/mic.svg" alt="Audio: " v-else-if="type === 'mp3' || type === 'wav'">
    <img src="../assets/material_symbols/unknown_document.svg" alt="Unkdown File: " v-else>
    <div>
      <div class="text-white ml-2.5 text-[1.035rem] text-left" v-if="name.startsWith('$untitled-')">
        New Note...
      </div>
      <div class="text-white ml-2.5 text-[1.035rem] text-left break-all" v-else>
        {{ name }}
      </div>
    </div>
  </button>
</template>

<script>
export default {
  props: [
      "type",
      "name",
      "info"
  ]
}
</script>