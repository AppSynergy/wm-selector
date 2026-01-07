<template>
  <VueDraggable class="print-items" handle=".handle" v-model="printItems">
    <Stats :used="true" />
    <ArmyRules />
    <SpecialRules :used="true" />
    <MagicItems :used="true" />
    <Spells :used="true" />
    <URL />
  </VueDraggable>
</template>

<script>
import VueDraggable from "vuedraggable";

import ArmyRules from "@/components/Print/ArmyRules";
import MagicItems from "@/components/Print/MagicItems";
import SpecialRules from "@/components/Print/SpecialRules";
import Spells from "@/components/Print/Spells";
import Stats from "@/components/Print/Stats";
import URL from "@/components/Print/URL";
import store from "@/store";

export default {
  name: "PrintItems",
  components: {
    ArmyRules,
    MagicItems,
    SpecialRules,
    Spells,
    Stats,
    URL,
    VueDraggable,
  },
  computed: {
    printItems: {
      get: () => store.getters.printItems,
    },
  },
};
</script>

<style lang="scss"></style>
