  <template>
    <div>
      <h1>This is Home Page</h1>
      <form action="">
        <inputField :name="name" @update-name="updateName"/>
        <br><button>submit</button>
        <!-- 양방향 바인딩 -->
      </form>
      {{ name }}
    </div>
  </template>

  <script>
  import inputField from '@/components/inputField.vue';
  export default {
    components:{
      inputField
    },
    data () {
      return {
        name: ''
      }
    },
    methods :{
      updateName(name) {
        this.name = name;
      }
    }
  }
  </script>

  <style scoped>
  h1 {
    color:red;
  }
  </style>