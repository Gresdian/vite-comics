<script>
export default {
    name: 'Appheader',
    data() {
        return {
            links:[
                'CHARACHTERS',
                'COMICS',
                'MOVIES',
                'TV',
                'GAMES',
                'COLLECTIBLES',
                'VIDEOS',
                'FANS',
                'NEWS',
                'SHOP'
                
            ]
        }
    },
            
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="navbar">
                <div class="logo">
                    <a href="/">
                        <img src="/img/dc-logo.png" alt="DC comics">
                    </a>
                </div>
                <div class="menu">
                    <ul>
                        <li  v-for="link, index in links" :key="index">
                            <a href="#" :class="index == 1 ? 'active' : ''">{{ link }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    @use '../styles/generals.scss' as *;
    @use '../styles/partials/variables' as *;


.navbar {
    display: flex;
    justify-content: space-between;
    padding: 20px 0;



     img {
        width: 80px;
        vertical-align: middle;

    }

    ul {
        list-style-type: none;
        margin: 0;
        display: flex;
        

        li{          
            display: inline-block;
            a{
                
                color: #000;
                padding: 0 10px;
                line-height: 80px;
                font-weight: 600;

                position: relative;
                
                &.active,
                &:hover{
                    color: $primary-color;
                    
                    &::after{
                        content:'';
                        position: absolute;
                        bottom: -51px;
                        left: 10px;
                        width: calc(100% - 20px);
                        height: 10px;
                        background-color: $primary_color;
                    }
                }


                
            }
        }
    }


}
</style>