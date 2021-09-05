<template>
    <div class="navigation-button">
        <a v-on:click="navVisible = !navVisible" href="#">
            <svg width="24" height="18" xmlns="http://www.w3.org/2000/svg">
                <path d="M24 16v2H0v-2h24zm0-8v2H0V8h24zm0-8v2H0V0h24z" fill="#FFF" fill-rule="evenodd"/>
            </svg>
        </a>
    </div>
    <nav class="navigation" >
        <ul> 
            <li>
                <a href="">About</a>
            </li>
            <li>
                <a href="">Services</a>
            </li>
            <li>
                <a href="">Projects</a>
            </li>
            <li>
                <a href="">CONTACT</a>
            </li>
        </ul>
    </nav>
    <nav class="navigation-mobile" :class="{active:navVisible}" >
        <ul> 
            <li>
                <a href="">About</a>
            </li>
            <li>
                <a href="">Services</a>
            </li>
            <li>
                <a href="">Projects</a>
            </li>
            <li>
                <a href="">CONTACT</a>
            </li>
        </ul>
    </nav>
</template>

<script>
    export default {
        data () {
            return{
                navVisible: false,
            };
        },
               
    }
</script>

<style lang="scss">
    @import "./src/scss/variables.scss";

    .navigation, .navigation-mobile{
        display: none;
    }

    .navigation-mobile{
         position: absolute;
        top: 110px;
        text-align: center;
        left: 15px;
        right: 15px;
        background-color: $white;
        padding: 30px 0;

        li{
            padding: 20px;

            &:last-child{
                width: 100px;
                margin: auto;
                background-color: $yellow;
                border-radius: 50%;
                border-radius: 9999px;
                
                    a  {
                        color: $very-dark-desaturated-blue;
                    }
                }
            }
            a{
                color: $dark-grayish-blue;
            }
        }
    .active{
        display: block;
    }
    
    
    
    // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) { 
       
        .navigation{
            display: block;

            ul{
                display: flex;
            }
            li{
                height: 60px;
                width: 130px;
                display: flex;
                justify-content: center;
                align-items: center;
            
                &:last-child{
                    background-color: $white;
                    border-radius: 50%;
                    border-radius: 9999px;
                    transition: background-color 0.4s ease ;
                    
                    &:hover{
                        background-color: #6eceff;

                        a{
                            color: $white;
                        }
                    
                    }
                    a  {
                        color: $very-dark-desaturated-blue;
                    }
                }
                a{
                    color: $white;
                }
            }
        }

         .navigation-mobile, .navigation-button{
            display: none;
        }
    }
</style>
