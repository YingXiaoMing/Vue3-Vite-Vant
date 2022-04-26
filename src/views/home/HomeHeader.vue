
<script lang="ts">

export default {
    name: 'HomeHeader'
}
</script>

<script setup lang="ts">







</script>

<template>
    <van-sticky>
        <van-nav-bar>
            <template #title>
                <div class="flex-center header_container">
                    <img class="header_img" src="/src/assets/home/header.png"/>
                    <span class="header_title">xx超市</span>
                    <img class="header_arrow" src="/src/assets/home/header_arrow.png">
                </div>
            </template>
        </van-nav-bar>
    </van-sticky>
</template>
<style lang="scss" scoped>

.header_img {
    width: 21px;
    height: 19px;
}
.header_title {
    margin: 0 5px;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    font-size: 16px;
}
.header_arrow {
    width: 10px;
}
</style>