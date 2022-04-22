<template>
    <button @click="onClick()" :style="{background: color}" class="btn">{{text}}</button>
</template>

<script>

export default{
  name:'Button',
  props:{
      text:{
          type:String,
          default:'Add',
      },
      color:{
          type:String,
          default:'lightblue',
      }
  },
  methods:{
      onClick() {
        console.log('hi');
      }
  }
}
</script>
