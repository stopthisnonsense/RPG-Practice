<template>
  <div class="character">
        <h2>Character</h2>
        <h3>{{ name }}</h3>
        <h4>Level: {{level}}</h4>
        <h3>HP: {{currentHp}} / {{maxHp}}</h3>
  </div>
</template>

<script>
    export default {
        data: function() {
            const player = new Character( "Rico", 1, 100, 100)
            function Character( charName, charLevel, currentHp, maxHp) {
                    this.charName = charName
                    this.charLevel = charLevel
                    this.currentHp = currentHp
                    this.maxHp = maxHp
            }
            return {
                name: player.charName,
                level: player.charLevel,
                currentHp: player.currentHp,
                maxHp: player.maxHp,
            }
        },
        methods: {
        }

    };
</script>

<style scoped lang="scss">

</style>