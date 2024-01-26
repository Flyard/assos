<template>
  <div class="navbar bg-primary" v-if="!isMobile()">
    <div class="flex-1 text-white">
      <router-link :to="{name: 'assos'}" class="btn btn-ghost text-2xl">
        <img src="../assets/Logo_AssoDex2.png" class="h-8 w-8">
        Assodex
      </router-link>
    </div>
    <div class="flex-none text-white">
      <ul class="menu menu-horizontal px-1 ">
        <li>
          <router-link :to="{name: 'assos'}" class="font-bold">Associations</router-link>
        </li>
        <li>
          <router-link :to="{name: 'actions'}" class="font-bold">Actions</router-link>
        </li>
        <li>
          <router-link :to="{name: 'carte'}" class="font-bold">Carte</router-link>
        </li>
      </ul>
    </div>
  </div>

  <div class="navbar bg-primary text-white" v-if="isMobile()">
    <div class="navbar-start">
      <router-link :to="{name: 'assos'}" class="btn btn-ghost text-2xl">
        <img src="../assets/Logo_AssoDex2.png" class="h-8 w-8">
        Assodex
      </router-link>
    </div>
    <div class="navbar-end">
      <div class="dropdown dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost btn-circle">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" color="white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7"/>
          </svg>
        </div>
        <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-[2] p-2 shadow bg-base-100 rounded-box w-52 text-black">
          <li>
            <router-link :to="{name: 'assos'}" class="font-bold">Associations</router-link>
          </li>
          <li>
            <router-link :to="{name: 'actions'}" class="font-bold">Actions</router-link>
          </li>
          <li>
            <router-link :to="{name: 'carte'}" class="font-bold">Carte</router-link>
          </li>
        </ul>
      </div>
    </div>

  </div>
</template>


<script setup lang="js">

function isMobile() {
  return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
      navigator.userAgent
  );
}

</script>