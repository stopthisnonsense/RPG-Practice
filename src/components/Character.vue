<template>
  <div class="character">
    <h2>Character: {{ name }}</h2>
    <h3>Level: {{ level }}</h3>
    <h3>HP: {{ currentHp }} / {{ maxHp }}</h3>
    <button @click="damage" class="button">Take Damage!</button>
    <button @click="heal" class="button">Heal Damage!</button>
  </div>
</template>

<script>
export default {
  data: function() {
    const player = new Character("Rico", 1, 100, 100);
    function Character(charName, charLevel, currentHp, maxHp) {
      this.charName = charName;
      this.charLevel = charLevel;
      this.currentHp = currentHp;
      this.maxHp = maxHp;
    }
    return {
      name: player.charName,
      level: player.charLevel,
      currentHp: player.currentHp,
      maxHp: player.maxHp
    };
  },
  methods: {
    damage() {
        this.currentHp = this.currentHp - Math.floor(Math.random() * 10);
      if (this.currentHp < 0) {
        this.currentHp = 0;
      }
    },
    heal() {
        this.currentHp = this.currentHp + Math.floor(Math.random() * 10);
      if (this.currentHp > this.maxHp) {
        this.currentHp = this.maxHp;
      }
    }
  }
};
</script>

<style scoped lang="scss"></style>
