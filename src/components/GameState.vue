<template>
  <div :class="['game-state', state]" @click="$emit('clicked')">
    <div>
      <div class="game-state-content">
        <Icons :type="userChoice"></Icons>
        <span>{{statemessages[state]}}</span>
        <Icons :type="userChoice"></Icons>
      </div>
    </div>
  </div>
</template>

<script>
  import Icons from './Icons';
  export default {
    name: "GameState",
    components: {
      Icons
    },
    props: ['state', 'userChoice', 'computerChoice'],
    data() {
      return {
        statemessages: {
          win: 'Congrats! You won!',
          lose: 'Sorry! You lost!',
          draw: 'You draw!'
        }
      }
    }
  }
</script>