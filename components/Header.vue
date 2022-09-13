<template lang="">
    <header class="flex items-center  justify-between py-7 lg:px-desktop mx-auto sticky top-0">
        <NuxtLink to="/">
          <h1 class="font-bold text-2xl">PRO.<span class="text-red-600">Agency</span></h1>
        </NuxtLink>
        <ul class="lg:flex hidden items-center space-x-14">
          <li class="group" v-for = "(link, i) in links" :key="`navLink${i}`">
            <NuxtLink>
              {{link}}
            </NuxtLink>
          </li>
        </ul>
    </header>
</template>

<script setup>
    const links = ["Home", "About", "Pricing", "Blog", "Contact Us"]
    const activeLink = useState('activeLink', () => 'Home')
</script>