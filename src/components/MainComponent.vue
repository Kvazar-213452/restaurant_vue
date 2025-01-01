<template>
    <div class="goods">
        <div class="goods_item">
            <img v-if="goods[0]" class="img_goods" :src="goods[0]" alt="img">
            <br>
            <p class="name_goods">{{ goods[1] }}</p>
            <p class="inc_goods">{{ goods[2] }}</p>
            <br>
            <p class="cost_goods">{{ goods[3] }}</p>
            <p class="info_goods">{{ goods[4] }}</p>
            <br>
            <button class="btn_goods">Order</button>
        </div>
    </div>
</template>
  
<script>
export default {
    props: {
        goods: {
        type: Array,
        required: true
        }
    }
}
</script>
