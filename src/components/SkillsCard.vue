<template>
    <div :class="cardClass" >
        <div class="skill-card">
        <h3>{{title}}</h3>
        <p>{{text}}</p>
        <button :class="buttonClass" >{{skillsContentButton}}</button>
        </div>
    </div>
</template>

<script>
export default {
    name : 'SkillsContent',
    props: [ 'cardClass', 'title' , 'text' , 'buttonClass' ],
  data () {
      return {
          skillsContentButton : 'LEARN MORE ',
      }
  }
}
</script>

<style lang="scss" scoped>
    @import "./src/scss/variables.scss";

    .skills-content{
        padding: 70px 30px;
        
        h3, p{
            margin-bottom: 40px;
        }
        p{
            color: $dark-grayish-blue;
            line-height: 2rem;
        }
    }
    .btn{
        color: $very-dark-desaturated-blue;
        font-size: 1rem;
        font-family: $title-font;
        position: relative;

        &:after{
            content: " ";
            height: 10px;
            width: 130px;
            position: absolute;
            left: -7px;
            bottom: -3px;
            z-index: -1;
            border-radius: 5rem;
        }
    }
    .red{
        &:after{
            background-color: #ffd7d0;
        }
        &:hover{

            &:after{
                background-color: $soft-red;
            }
        }
    }
    .yellow{
        &:after{
            background-color: #fdf0b9;
        }
        &:hover{
            &:after{
                background-color: $yellow;
            }
        }
    }

    // Medium devices (tablets, 768px and up)
    @media (min-width: 992px) { 
        .skills-content{
            padding: 0;
            text-align: left;
            display: flex;
            justify-content: center;
            align-items: center;
            
        }
        .skill-card{
            max-width: 440px;
            max-height: 280px;
        }
    }
    

</style>
