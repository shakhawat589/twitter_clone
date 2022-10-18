<template>
  <nuxt-link to="#" class="flex items-center gap-3 p-3 min-w hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white rounded-full" :class="defaultTransition">
    <div class="h-6 w-6 text-dark" >
      <slot name="icon"></slot>
    </div>
    <div class="text-xl hidden xl:block" :class="textActive">
      <slot name="name"></slot>
    </div>
  </nuxt-link>
</template>

<script setup>

  const {defaultTransition} = useTailwindConfig();

  const props = defineProps({
    active: {
      type: Boolean,
      default: false
    }
  });

  const textActive = computed(() => props.active ? 'font-semibold' : 'font-normal');

</script>