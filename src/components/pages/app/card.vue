<template>
    <div>
        <div class="card round text-center bg-white" style="height: 460px;">
            <div class="trans-img">
                <img :src="card.cardimg" class="card-img-top">
            </div>
            <div class="card-body my-3">
                <h5 class="card-title">
                    <img :src="card.iconimg" class="img-w"> 
                    {{ card.title }}
                    </h5>
                <p class="card-text text-muted">{{ card.text }}</p>
                <div class="d-flex justify-content-center">
                    <h6 class="bor"></h6>
                </div>
                <small class="text-muted">Available for</small>
                <div class="mt-3">
                    <div class="mt-3">
                        <img class="mb-1" :src="card.img1">
                        <img class="ms-1 mb-1" :src="card.img2"><br>
                        <img :src="card.img3">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'card',
    props: [
        'card', 'id', 'title', 'cardimg', 'iconimg', 'text', 'img1', 'img2', 'img3',
    ], 
    data(){
        return {
            
        }
    },
}
</script>
 
<style lang="scss">
.bor {
    width: 50%; 
    border-top: 1px solid lightgray; 
}
small {
    font-size: 12px;
}
    .round {
    border-radius: 13px;
    }
    .card {
        overflow: hidden;
    }
    .card:hover {
        border: 1px solid #2f65b0;
    }
    .card-img-top {
        transition: transform .6s; /* Animation */
    }
    .card-img-top:hover {
        transform: scale(1.1); /* (110% zoom - Note: if the zoom is too large, it will go outside of the viewport) */
    }
    .trans-img {
        overflow: hidden;
    }
    .img-w {
        width: 38px;
    }

</style> 