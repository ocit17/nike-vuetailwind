<script setup>
import Nav from './components/Nav.vue';
import { 
  Hero,
  PopularProducts,
  SuperQuality,
  Services,
  SpecialOffer,
  CustomerReviews,
  Subscribe,
  Footer
} from './sections'
</script>

<template>
  <main>
    <Nav/>
    <section class="xl:padding-l wide:padding-r padding-b">
      <Hero/>
    </section>
    <section class="padding">
      <PopularProducts/>
    </section>
    <section class="padding">
      <SuperQuality/>
    </section>
    <section class="padding-x py-10">
      <Services/>
    </section>
    <section class="padding bg-pale-blue">
      <SpecialOffer/>
    </section>
    <section class="padding">
      <CustomerReviews/>
    </section>
    <section class="padding-x sm:py-32 pt-16 w-full">
      <Subscribe/>
    </section>
    <section class="padding-x bg-black padding-t pb-8">
      <Footer/>
    </section>
  </main>
</template>
