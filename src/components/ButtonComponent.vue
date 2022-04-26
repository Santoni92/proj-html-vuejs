<template>
  <button>{{ message }}</button>
</template>

<script>
export default {
    name:'ButtonComponent',
    props:{
        message:String
    }
}
</script>

<style lang="scss" scoped>
button{
    background-color: #1fad96;
    color:white;
    font-size:25px;
    padding:10px;
    border-radius: 10px;
}

</style>