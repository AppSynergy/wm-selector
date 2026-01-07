<template>
  <div class="army-rules">
    <h3 class="handle">Army Rules</h3>
    <div>{{ armyRules }}</div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "ArmyRules",
  computed: mapGetters(["armyRules"]),
};
</script>
