<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                  <slot></slot>
            </div>
        </div>
      
    </div>
</template>
<script>
export default {
   
}
</script>
<style scoped>
.panel-body{
    font-family: 'Arizonia',cursive;
    font-size: 24px;
    color:pink;
    background-color: black;


}
.quote{
    cursor: pointer;
 }
.quote:hover{
    background-color: gray;
}
</style>