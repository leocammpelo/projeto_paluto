<template>
  <el-row>
    <p>{{ coordinates.lat }} Latitude, {{ coordinates.lng }} Longitude</p>
    <GmapMap
      :center="{lat:-21.2522174, lng:-44.9936702}"
      :zoom="10"
      style="width:640px; height:360px">
    </GmapMap>
  </el-row>
</template>

<script>
  export default {
    data () {
      return {
          coordinates: {
              lat: 0,
              lng: 0
          }
      }
    },

    created() {
        this.$getLocation({})
            .then(coordinates => {
                this.coordinates = coordinates;
            })
          .catch(error => alert(error));
    },
    
  }
</script>