<template>
  <div class="bucket-list">
    <h1>
      {{ title }}
    </h1>

    <ul>
        <li v-for="item in data" :key="item.task">
        <BucketItem :item="item"/>
      </li>
    </ul>

    <h6>
        {{ footer }}
    </h6>
  </div>
</template>



<script>

  import BucketItem from './BucketItem.vue'
  export default {
    name: 'BucketList',
    components: {BucketItem},
    props: {
      title: String,
      footer : String,
      link : String,
      data : Array
    },

    methods: {
      loadData: function() {
        console.log("loading...")
      },
    },

    beforeMount(){
      this.loadData()
    },

    created() {
      var axios=require('axios');
      var self = this;
      var url='https://raw.githubusercontent.com/maifeeulasad/bucket-list/develop/bucket/bucket.json';
      axios.get(url)
              .then(function (response) {
                self.data = response.data;
              });
    }
  }
</script>