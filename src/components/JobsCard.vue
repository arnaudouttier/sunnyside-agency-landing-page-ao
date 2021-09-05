<template>
    <div  v-for="job in jobs" v-bind:key="job.id" :class="job.className"  >
        <div class="jobcard-content">
            <h3>{{job.jobTitle}}</h3>
            <p>{{job.text}}</p>
        </div>
    </div>
</template>

<script>
export default {
  name : 'JobsContent',
  data () {
      return {
          jobs : [
                { 
                    id:1, 
                    className : 'jobcard graphic',
                    jobTitle : 'Graphic design' , 
                    text: '  Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention..' 
                },
                {   id:2, 
                    className : 'jobcard photography',
                    jobTitle : 'Photography' , 
                    text: 'Increase your credibility by getting the most stunning, high-quality photos that improve your business image.'  
                }
          ]
      }
  }
}
</script>

<style lang="scss">
    @import "./src/scss/variables.scss";

    .jobcard{
        height: 480px;
        display: flex;
        align-items: end;
        justify-content: center;
        padding: 60px 30px;
    }
    .jobcard-content{
        h3{
            margin-bottom: 40px;
            font-size: 1.8rem;
        }
        p{
            line-height: 1.6rem;
            font-size: 1rem;
        }
    }
    .graphic, .photography{
        background-size: cover;
        background-repeat: no-repeat;
    }
    .graphic{
        color: $dark-desaturated-cyan ;
        background-image: url('../assets/images/mobile/image-graphic-design.jpg');
    }
    .photography{
        color: $dark-blue ;
        background-image: url('../assets/images/mobile/image-photography.jpg');
    }
    // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) {
         .jobcard{
             width: 50%;
         }
         .jobcard-content{
             max-width: 330px;
         }

        .graphic{
        background-image: url('../assets/images/desktop/image-graphic-design.jpg');
        }
        .photography{
        background-image: url('../assets/images/desktop/image-photography.jpg');
        }
     }

</style>
