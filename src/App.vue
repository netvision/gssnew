<script setup>
import Menubar from 'primevue/menubar';
import logo from './assets/gss-logo.png'
const menuItems = [
        { label: 'Home', url: '/' },
        {
          label: 'About Us',
          items: [
            { label: 'Introduction', url: '/intro' },
            { label: 'Managing Committee', url: '/management' },
            { label: 'Admission Info', url: '/admissions' },
            { label: 'Courses Offered', url: '/courses' },
            { label: 'Other Info', url: '/info' }
          ],
        },
        { label: 'Principal & Staff', url: '/#/other' },
        { label: 'Facilities', url: '/facilities' },
        { label: 'Photo Gallery', url: '/gallery' },
        { label: 'Contact', url: '/contact' },
      ]

onMounted(() => {
  window.document.title = "Lets Work together"
});
</script>

<template>
  <div class="flex flex-col min-h-screen w-full bg-white"> <!-- Added a parent flex-col to stack header and main -->
    <header class="flex flex-col sm:flex-row items-end max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full pt-4">
      <img :src="logo" class="h-24 sm:h-44 p-2" />
      <div>
        <h2 class="merriweather-bold text-4xl sm:text-4xl text-orange-800 pl-0 sm:pl-8 font-bold">
          Ginnidevi Satyanarayan Sekhsaria
        </h2>
        <h2 class="lato-regular text-3xl sm:text-3xl mb-3 text-orange-800 pl-0 sm:pl-8 font-bold">
          GSS Girls' PG College, Chirawa
        </h2>
      </div>
    </header>
    <main class="w-full sm:w-auto flex-1"> <!-- Added flex-1 to main for proper stacking -->
      <Menubar :model="menuItems" class="max-w-7xl w-full mx-auto bg-red-100" />
      <RouterView></RouterView>
    </main>
  </div>
     
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Barlow:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Merriweather:ital,wght@0,300;0,400;0,700;0,900;1,300;1,400;1,700;1,900&family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');
.merriweather-bold {
  font-family: "Merriweather", system-ui;
  font-weight: 700;
  font-style: normal;
}
.barlow-light {
  font-family: "Barlow", sans-serif;
  font-weight: 300;
  font-style: normal;
}

.barlow-regular {
  font-family: "Barlow", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.lato-regular {
  font-family: "Lato", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.lato-bold {
  font-family: "Lato", sans-serif;
  font-weight: 700;
  font-style: normal;
}

.lato-black {
  font-family: "Lato", sans-serif;
  font-weight: 900;
  font-style: normal;
}

</style>
