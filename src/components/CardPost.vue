<script>
export default {
    name: 'CardPost',
    props: {
        post: {
            type: Object,
            required: true
        }
    },
    methods: {
        handleLike() {
            this.$emit('like')
        }
    }
}
</script>
<template>
    <div class="cardPost">
        <div class="cardPost-img">
            <img :src="post.img" alt="">
        </div>
        <h3 class="cardPost-title">{{ post.title }}</h3>
        <p class="cardPost-description">{{ post.description }}</p>
        <div class="cardPost-like">
            <button @click="handleLike">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-balloon-heart-fill" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M8.49 10.92C19.412 3.382 11.28-2.387 8 .986 4.719-2.387-3.413 3.382 7.51 10.92l-.234.468a.25.25 0 1 0 .448.224l.04-.08c.009.17.024.315.051.45.068.344.208.622.448 1.102l.013.028c.212.422.182.85.05 1.246-.135.402-.366.751-.534 1.003a.25.25 0 0 0 .416.278l.004-.007c.166-.248.431-.646.588-1.115.16-.479.212-1.051-.076-1.629-.258-.515-.365-.732-.419-1.004a2.376 2.376 0 0 1-.037-.289l.008.017a.25.25 0 1 0 .448-.224l-.235-.468ZM6.726 1.269c-1.167-.61-2.8-.142-3.454 1.135-.237.463-.36 1.08-.202 1.85.055.27.467.197.527-.071.285-1.256 1.177-2.462 2.989-2.528.234-.008.348-.278.14-.386Z"/>
            </svg>
            Like
            </button>
            <p>{{ post.like }} {{ post.like <= 1 ? 'Like' : 'Likes'}} </p>
        </div>
    </div>
</template>

<style lang="scss">
.cardPost {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 500px;
    height: 700px;
    margin: 50px;
    padding: 20px;
    backdrop-filter: blur(10px);
    background-color: rgba(255, 255, 255, 1);
    border-radius: 26px;
    box-shadow: 35px 35px 68px 0px rgba(87, 87, 87, 0.5), inset -0px -0px 16px 0px rgba(87, 87, 87, 0.6), inset 0px 11px 28px 0px rgb(255, 255, 255);

    &-img{
        width: 100%;
        height: 50%;
        border-radius: 26px;
        
        img{
            width: 100%;
            height: 100%;
            border-radius: 26px;
        }
    }

    &-like{
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 50%;

        button{
            width: 100px;
            height: 30px;
            border: none;
            background-color: #F56040;
            color: #fff;
            font-size: 1.2rem;
            border-radius: 10px;
            transition: background-color 0.1s ease-in;

            &:hover{
                cursor: pointer;
                background-color: #FD1D1D;
            }
        }
    }
}
</style>