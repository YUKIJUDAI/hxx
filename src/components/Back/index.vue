<template>
    <div>
        <div class="icon" @click="back">
            <van-icon name="arrow-left" class="arrow" />
        </div>
        <div class="icon2" @click="home">
            <van-icon name="home-o" class="home" />
        </div>
    </div>
</template>

<script>
export default {
    name: 'Back',
    methods: {
        back() {
            this.$emit('backEvt');
        },
        home() {
            this.$router.push({ name: 'Home' });
        }
    }
}
</script>

<style lang="scss" scoped>
.icon {
    position: fixed;
    top: 1.3%;
    left: 2%;
    z-index: 15;
    width: 35px;
    height: 35px;
    line-height: 35px;
    border-radius: 50%;
    text-align: center;
    background: rgba(0, 0, 0, 0.5);
    .arrow {
        color: #fff;
        margin-top: 10px;
        margin-left: -2px;
    }
}
.icon2 {
    position: fixed;
    top: 1.3%;
    right: 2%;
    z-index: 15;
    width: 35px;
    height: 35px;
    line-height: 35px;
    border-radius: 50%;
    text-align: center;
    background: rgba(0, 0, 0, 0.5);
    .home {
        color: #fff;
        margin-top: 10px;
        margin-right: -2px;
    }
}
</style>