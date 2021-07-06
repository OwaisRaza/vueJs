<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <a-row :gutter="24">
      <a-col v-for="item in items" v-bind:key="item.id" class="gutter-row" :xs="{ span: 24 }" :md="{ span: 8 }">
        <div class="gutter-box">
           <a-card>
            <img
              slot="cover"
              alt="example"
              width="100%"
              :src="item.img"
            />
            <a-card-meta :title="item.title">
              <template slot="description">
                {{item.description}}
              </template>
            </a-card-meta>
          </a-card> 
        </div>
      </a-col>
    </a-row>

  </div>
</template>

<script>
import Vue from "vue";

export default {
  name: 'HelloWorld', 
  props: {
    msg: String
  },
  data() {
    return {
 items: [{
      id: 1,
      title: 'abc',
      description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro, facilis!',
      img: 'https://images.pexels.com/photos/458886/pexels-photo-458886.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
    },
    {
      id: 2,
      title: 'xyz',
      description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro, facilis!',
      img: 'https://images.pexels.com/photos/1083822/pexels-photo-1083822.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
    },
    {
      id: 3,
      title: 'cye',
      description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro, facilis!',
      img: 'https://images.pexels.com/photos/992734/pexels-photo-992734.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
    }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

</style>
