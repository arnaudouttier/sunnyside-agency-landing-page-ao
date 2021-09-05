<template>
    <div class="jobs">
        <JobsCard />
    </div>
</template>

<script>
import JobsCard from './JobsCard.vue'

export default {
  components: {
    JobsCard,
  }
}
</script>

<style lang="scss">
  .jobs{
    text-align: center;
  }
   // Medium devices (tablets, 768px and up)
    @media (min-width: 768px) {
      .jobs{
        display: flex;
      }
     }
</style>
