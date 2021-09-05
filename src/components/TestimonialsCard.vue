<template>
    <div v-for="job in jobs" v-bind:key="job.id" class="testimonials-card" >
        <img  :src="job.url" :alt="job.alt">
        <p>{{job.text}}</p>
        <h3>{{job.name}}</h3>
        <h4>{{job.jobName}}</h4>
    </div>
</template>

<script>
export default {
    name : 'TestimonialsContent',
  data () {
      return {
          jobs : [
                { 
                    id:1, 
                    url : require('../assets/images/image-emily.jpg')  , 
                    alt: 'Emily'  , 
                    name:'Emily R',
                    text: 'We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.',
                    jobName: 'Marketing Director'
                },
                { 
                    id:2, 
                    url : require('../assets/images/image-thomas.jpg')  , 
                    alt: 'Thomas' , 
                    name:'Thomas' ,
                    text:'Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.',
                    jobName: 'Chief Operating Officer'
                },
                { 
                    id:3, 
                    url : require('../assets/images/image-jennie.jpg')  , 
                    alt: 'Jennie' , 
                    name:'Jennie',
                    text: 'Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!',
                    jobName: 'Business Owner'
                },
          ]
      }
  },
  }
</script>

<style lang="scss" scoped>
    @import "./src/scss/variables.scss";
    
    .testimonials-card{

        img, p{
            margin-bottom: 40px;
            
        }
        p{
            color: $very-dark-grayish-blue;
            line-height: 1.7;
        }
        h3{
            margin-bottom: 12px;
            color: $very-dark-desaturated-blue;
            font-size: 1.3rem;
        }
        h4{
            font-family: $main-font;
            margin-bottom: 60px;
            color: $grayish-blue;
            font-size: 0.9rem;
        }
    }
    img {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        margin-bottom: 40px;
    }
    // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) { 
         .testimonials-card{
            margin-right: 20px;
            
             p{
                 height: 250px;
             }
         }
    }
     // Medium devices (tablets, 768px and up)
    @media (min-width: 992px) { 
         .testimonials-card{
             p{
                 height: auto;
             }
         }
    }
</style>
