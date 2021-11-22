<template>
  <div>
    <div class="container py-10 mx-auto border-b-2">
      <nuxt-link to="/admin">
        <button class="focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-white bg-indigo-600 cursor-pointer px-3 py-2.5 font-normal text-xs leading-3 shadow-md rounded">
          Voltar
        </button>
      </nuxt-link>
    </div>
    <div class="container py-5 mx-auto border-b-2">
      <form @submit.prevent="onSave">
        <div class="flex flex-col  my-5">
            <label for="title" class="text-gray-800 dark:text-gray-100 text-sm font-bold leading-tight tracking-normal mb-2">Titulo</label>
            <input v-model="editPost.author" autocomplete="off" class="text-gray-600 dark:text-gray-400 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 dark:focus:border-indigo-700 dark:border-gray-700 dark:bg-gray-800 bg-white font-normal w-64 h-10 flex items-center pl-3 text-sm border-gray-300 rounded border shadow" />
        </div>
        <div class="flex flex-col  my-5">
            <label for="title" class="text-gray-800 dark:text-gray-100 text-sm font-bold leading-tight tracking-normal mb-2">Titulo</label>
            <input v-model="editPost.title" autocomplete="off" class="text-gray-600 dark:text-gray-400 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 dark:focus:border-indigo-700 dark:border-gray-700 dark:bg-gray-800 bg-white font-normal w-64 h-10 flex items-center pl-3 text-sm border-gray-300 rounded border shadow" />
        </div>
        <div class="flex flex-col  my-5">
            <label for="description" class="text-gray-800 dark:text-gray-100 text-sm font-bold leading-tight tracking-normal mb-2">Descrição</label>
            <textarea v-model="editPost.description"   class="text-gray-600 dark:text-gray-400 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 dark:focus:border-indigo-700 dark:border-gray-700 dark:bg-gray-800 bg-white font-normal w-64 h-10 flex items-center pl-3 text-sm border-gray-300 rounded border shadow" name="dexcription"  cols="30" rows="50"></textarea>
        </div>
        <div class="flex flex-col  my-5">
            <button
            type="submit"
            class=" w-1/4 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-white bg-indigo-600 cursor-pointer px-3 py-2.5 font-normal text-xs leading-3 shadow-md rounded">
          salvar
        </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        editPost: {
          author: "",
          title: "",
          description: "",
        }
      }
    },
    methods: {
      onSave() {
        console.log('salvo')
      },
      onCancel() {

      }
    },
  }
</script>

<style lang="scss" scoped>

</style>
