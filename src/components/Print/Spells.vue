<template>
  <div class="spells">
    <h3 class="handle">Spells</h3>
    <dl>
      <template v-for="(spell, index) in spells">
        <div :key="index">
          <h5>
            <span class="spell">{{ spell.name }}</span>
            <span class="spell">{{ spell.roll }}+ to cast</span>
            <span class="spell"> Range {{ spell.range || "N/A" }} </span>
          </h5>
          <div>{{ spell.text }}</div>
        </div>
      </template>
    </dl>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "Spells",
  computed: mapGetters(["spells"]),
};
</script>

<style lang="scss">
.spells {
  font-size: 12px;

  .spell {
    margin-left: 20px;
    margin-top: 10px;
  }
}
</style>
