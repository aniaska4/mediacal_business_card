  
<template>
  <div>
    <Nav />
    <Information />
    <Actuality />
    <Team />
    <Location />
    <Contact />
  </div>
</template>
<script>
import Nav from './partials/Nav'
import Information from './partials/Information'
import Actuality from './partials/Actuality'
import Team from './partials/Team'
import Location from './partials/Location'
import Contact from './partials/Contact'
export default {
  components: {
    Nav,
    Information,
    Actuality,
    Team,
    Location,
    Contact
  }
}
</script>
