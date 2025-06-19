<template>
  <main class="flex">
    <div class="relative">
      <div class="absolute top-8 left-8 bg-zinc-600 rounded-lg">
        <div class="text-xl font-bold p-4">
          <div class="ml-auto bg-amber-600 rounded-lg h-8 w-8">
            <div class="flex">
              <div class="text-white mx-auto">
                {{ count }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <button @click="count++" class = "mx-auto hover:cursor-pointer bg-amber-300">

      This is a button    </button>
  </main>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>