<!-- <template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script> -->

  <template>
    <div>
      <h1>This is Home Page</h1>
      <Hyeon />
    </div>
  </template>

  <script>

  import Hyeon from '@/components/Hyeon.vue';

  export default {
    components : {
      Hyeon
    },

    data () {
      return {
        name:"hyeon's code"
      }
    }
  }
  </script>

  <style scoped>
  h1 {
    color:red;
  }
  </style>