<template>
  <div :class="{'dark': darkMode }">
    <div class="bg-white dark:bg-dim-900">
   
      <div class="min-h-full">

        <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">
          <!-- Sitder bar -->
            <div class="hidden md:block xs:col-span-1 xl:col-span-2">
              <div class="sticky top-0">
                <SidebarLeft/>
              </div>
            </div>

          <!-- Main Content -->
            <main class="bg-red-700 col-span-12 md:col-span-8 xl:col-span-6">
              <h1>Hi</h1>
            </main>

          <!-- Right bar -->
            <div class="hidden bg-red-300 md:block md:col-span-3 xl:col-span-4">
              <div class="sticky top-0">
                <h1>Right Sidebar</h1>
              </div>
            </div>
        </div>

      </div>
    
    </div>
  </div>
</template>


<script setup>
  const darkMode = ref(false);
</script>
