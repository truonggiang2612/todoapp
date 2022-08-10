<template>
   <div class="info">
            <h1 class="title">
                <pre>&lt;Product DIY&gt;</pre>
            </h1>
            <p class="description">See more about us. Click <strong>Open</strong> at the top</p>
    </div>
</template>

<script>
export default {
    name: 'ComponentContent'
    
}
</script>

<style>
.info .title,
.description {
    font-size: 25px;
    color: #fff;
}

.title pre {
    font-size: 40px;
}
</style>