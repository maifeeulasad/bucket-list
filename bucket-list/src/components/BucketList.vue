<template>
  <div class="bucket-list">
    <h1>
      {{ title }}
    </h1>

    <ul>
      {{ data }}
    </ul>

    <h6>
        {{ footer }}
    </h6>
  </div>
</template>

<script>
  export default {
    name: 'BucketList',
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