<template>
  <button>{{ messageButton }}</button>
</template>

<script>
export default {
    name:'ButtonComponent',
    props:{
        messageButton:String
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
    &:hover{
        background-color: white;
        color:green;
    }
}

</style>