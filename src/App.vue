<template>
<div class="container">
  <Header title="Task tracker"/>
</div>
</template>

<script>
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Header,
  },
data() {
  return{
    tasks: []
  }
},
created() {
  this.tasks=[
    {
      id:1,
      text:'Doctors Appointment',
      day:'March 1st',
      reminder:true
    },
    {
      id:2,
      text:'Restaurant Grill 168',
      day:'March 22th',
      reminder:true
    },
    {
      id:3,
      text:'Coffee Shop',
      day:'March 29th',
      reminder:false
    }
  ]
}
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bellota:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&display=swap');
* {
 box-sizing: border-box;
 margin:0;
 padding:0;
}

body {
  font-family: 'Bellota';
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid skyblue;
  padding: 30px;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: pink;
  color: #fff;
  border: none;
  padding: 10px 20px;
  box-shadow: 2px 2px 4px rgb(162, 188, 197);
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration:none;
  font-size: 15px;
  font-family: 'Bellota';
}
</style>
