<template>
  <div class="home">
    <HeaderJumbotron :data="info"/>
    <CountDownTimer :format="info.startTimeFormat" :date="info.startTime"/>
    <SubHeaderTickets :data="info"/>
    <AboutBlock/>
    <Scheduler/>
  </div>
</template>

<script>

  import { eventInfo } from '@/data/index';
  import HeaderJumbotron from './HeaderJumbotron.vue';
  import SubHeaderTickets from './SubHeaderBlock.vue';
  import Scheduler from './Scheduler.vue';
  import AboutBlock from './AboutBlock.vue';
  import CountDownTimer from './CountDownTimer.vue';

  export default {
    name: 'home',
    created() {
      this.info = eventInfo;
    },
    data() {
      return {
        info: {},
      };
    },
    components: {
      CountDownTimer,
      AboutBlock,
      Scheduler,
      HeaderJumbotron,
      SubHeaderTickets,
    },
  };
</script>

