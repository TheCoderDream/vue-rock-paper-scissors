<template>
  <div class="choices">
    <div>You</div>
    <div></div>
    <div>Computer</div>

    <div>
      <button class="rock" @click="$emit('chosed', 'rock')">
        <Icons type="rock"></Icons>
      </button>
      <button class="paper" @click="$emit('chosed', 'paper')">
        <Icons type="paper"></Icons>
      </button>
      <button class="scissors" @click="$emit('chosed', 'rock')">
        <Icons type="scissors"></Icons>
      </button>
    </div>

    <div class="vs">vs</div>

    <div>
      <button class="computer-choice">
        ?
      </button>
    </div>
  </div>
</template>

<script>
  import Icons from './Icons';
  export default {
    name: 'Choices',
    components: {
      Icons
    },
    data() {
      return {
        
      }
    }
  }
</script>