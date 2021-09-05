<template>
   <div class="skills" >
        <img  
          :srcset="eggDesktopPhoto + ' 600w, '"
          :src="eggMobilePhoto"  
          alt="egg photo job">
       <SkillsCard 
          cardClass="skills-content transform"
          title='Transform your brand'  
          text='We are a full-service creative agency specializing in helping brands grow fast Engage your clients through compelling visuals that do most of the marketing for you'
          buttonClass="btn yellow" />
        <img  
          :srcset="glassDesktopPhoto + ' 600w, '"
          :src="glassmobilePhoto"  
          alt="glass photo job">
        <SkillsCard 
          cardClass="skills-content standOut"
          title='Stand out to the right audience'  
          text='Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places' 
          buttonClass="btn red" />
   </div>
</template>

<script>
import SkillsCard from './SkillsCard.vue'

export default {
  components: {
    SkillsCard,
  },
  data () {
      return {
        eggMobilePhoto : require('../assets/images/mobile/image-transform.jpg'),
        eggDesktopPhoto : require('../assets/images/desktop/image-transform.jpg'),
        glassmobilePhoto : require('../assets/images/mobile/image-stand-out.jpg'),
        glassDesktopPhoto : require('../assets/images/desktop/image-stand-out.jpg'),
      }
  }
}
</script>

<style lang="scss">
  .skills{
    text-align: center;
  }

    // Medium devices (tablets, 768px and up)
    @media (min-width: 992px) { 
      .skills{
        display: grid; 
        grid-template-columns: repeat(2, 1fr); 
        grid-template-rows: repeat(2, 1fr); 
        gap: 0px 0px; 
        grid-template-areas: 
          "trans transphoto"
          "standoutphoto standout"; 
      }
      .transform{grid-area: trans;}
      .transPhoto{grid-area: transphoto;}
      .standoutPhoto{grid-area: standoutphoto;}
      .standOut{grid-area: standout;}
    }
</style>
