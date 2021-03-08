<template>
    <div>
        <h2>Character: {{ name }}</h2>
        <h3>Level: {{ level }}</h3>
        <h3>HP: {{ currentHp }} / {{ maxHp }}</h3>
        <button @click="damage" class="button">Take Damage!</button>
        <button @click="heal" class="button">Heal Damage!</button>
    </div>
</template>

<script>
// import Character from "@/components/Character.vue";
export default {
  components: {
    // Character
  },
  data: function() {
    const player = new Character("Goblin", 1, 100, 100);
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
};
</script>