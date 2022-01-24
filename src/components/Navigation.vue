<template>
<div>
<nav>
    <div>
        <h2><span class="vue">Vue</span>Swiper</h2>
    </div>
       <div>
        <h2><a href="https://github.com/ismail9k/vue3-carousel" alt="Github"><img src="https://pngimg.com/uploads/github/github_PNG83.png" alt=""/></a></h2>
        </div>
</nav>
</div>
</template>
<script>
export default {
    name:"Navigation",
}
</script>
<style scoped>
nav {
    display:flex;
    justify-content:space-between;
    padding:1em;
    background:rgb(223, 223, 223);
    align-items:center;
    width:100%;
    height:10vh;
}
.vue {
    color:green;
    margin-right:4px;
}
img {
    width:30px;
    height:30px;
}
</style>