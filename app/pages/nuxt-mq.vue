<template>
  <div class="nuxt-mq-example">
    <h1>nuxt-mq</h1>
    <p>range: {{ $mq }}</p>
    <div>
      <mq-layout mq="lg">
        <LargeComponent />
      </mq-layout>
      <mq-layout mq="md">
        <MediumComponent />
      </mq-layout>
      <mq-layout mq="sm">
        <SmallComponent />
      </mq-layout>
    </div>
  </div>
</template>

<script>
import LargeComponent from '../components/nuxt-mq/LargeComponent';
import MediumComponent from '../components/nuxt-mq/MediumComponent';
import SmallComponent from '../components/nuxt-mq/SmallComponent';

export default {
  components: {
    LargeComponent,
    MediumComponent,
    SmallComponent,
  },
};
</script>

<style scorped>
.nuxt-mq-example {
  margin: 5px;
}
</style>
