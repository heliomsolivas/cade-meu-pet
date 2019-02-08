<template>
    <v-card color="grey lighten-2">
            <v-img :src="dog.img" height="170px"> </v-img>
            <v-card-title>
                <div>
                <h3>{{dog.name}}</h3>
                <p class="breed">{{dog.breed}}</p>
                </div>
            </v-card-title>
            <v-btn class="light" block @click="$emit('addToFavorites', dog)"><v-icon color="red">favorite</v-icon></v-btn>
    </v-card>
</template>

<script>
	export default {
	  props: {
	    dog: {
	      type: Object
	    }
	  }
	};
</script>

<style lang="scss" scoped>
.light{
  box-shadow:none !important;
}
.v-btn{
  height: 52px;
}
.v-card__title{
  background:#fff;
}
.v-card{
  margin-top: 0 !important;
  box-shadow: none !important;
  border-radius: 3px;
    background-color: #ffffff;
    box-shadow: 0px 5px 25px 0px rgba(46, 61, 73, 0.2) !important;
    transition: all 0.5s ease;
}
</style>
