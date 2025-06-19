<template>
  <section class="flex flex-col gap-2">
    <!-- access variables from within your script tags with {{  }} syntax-->
    <div class= "bg-beige h-20 w-full rounded-2xl grid place-items-center">
      {{ count }}
    </div>

    <div class="flex gap-2">
      <button 
        type="button"
        class="cursor-pointer rounded-md bg-zinc-500 text-white w-1/2 p-2"
        @click="increaseCount"
      >
        Increase Count
      </button>
  
      <button 
        class="cursor-pointer rounded-md bg-red-500 text-white w-1/2 p-2"
        type="button"
        @click="resetCount"
      >
        reset Count
      </button>
    </div>
  </section>
</template>

<!-- 
There are two options when using vue.
The modern way is to use <script setup> you will see this in the documentation called "Composition api"
The alternative is "Options api"
This will look something like
<script> // note we do not add "setup"
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increaseCount() {
      this.count = this.count + 1;
    },
    resetCount() {
      this.count = 0;
    }
  },
}
</script>

it is mostly preference which one you use however in my opinion "Composition api" looks more similar to regular
javascript code and may be easier to understand for you
-->
<script setup>
import {ref} from "vue";
// this creates a reactive variable
// whenever this changes, the template will re-render with the new count automatically
// https://vuejs.org/guide/essentials/reactivity-fundamentals.html#declaring-reactive-state-1
const count = ref(0);

function increaseCount() {
  count.value = count.value + 1
}

function resetCount() {
  count.value = 0;
}
</script>