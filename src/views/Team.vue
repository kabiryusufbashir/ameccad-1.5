<template>
  <div class="px-4 md:px-24 py-24">
    <div class="md:grid grid-cols-3 gap-4 my-8 bg-white items-center">
        <User path="sufi.jpg" name="Engr. Tijjani Aminu Ibrahim" rank="Managing Director"/>
        <User path="awwal.jpg" name="Engr. Auwal Abubakar Uthman" rank="Director Engineering/Center Manager"/>
        <User path="samir.jpg" name="Engr. Samir Bashir" rank="Director Training"/>
        <User path="khalil.jpg" name="Engr. Ibrahim Khalil Umar" rank="Director Research &amp; Development"/>
        <User path="abba.jpg" name="Engr. Abba Ibrahim" rank="Director Planning"/>
    </div>
  </div>  
</template>

<script>
import User from '../components/User'
export default {
  name: 'Team',
  components: {
      User
  }
}
</script>
