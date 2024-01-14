 <template>
  <div class="home">
    <home/>
    
  </div>
</template>

<script>
// @ is an alias to /src
import home from '@/components/home.vue'
import carusel from '@/components/Carusel.vue'

export default {
  name: 'homeView',
  components: {
    home,
    carusel,
  }
}
</script>
