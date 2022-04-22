<template>
  <header>
    <h1>{{title}}</h1>
    <Button text="Add task" color="pink"/>
  </header>
</template>

<script>
import Button from './Button'
export default{
    name: 'Header',
    props: {
        title: {
            type: String,
            default:'Hello world'
        }
    },
    components :{
        Button,
    }
}
</script>

<style scoped>
header{
    display:flex;
    justify-content: space-between;
    align-items: center;
    margin-block-end:20px;
}

</style>

