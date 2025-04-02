<!-- eslint-disable prettier/prettier -->

<script setup>
const props = defineProps({
  isHovered: {
    type: Boolean,
    required: true,
    default: false,
  },
  isClicked: {
    type: Boolean,
    required: true,
    default: false,
  },
});

const emit = defineEmits(["changeClickState", "changeHoverState"]);

const changeClickState = () => {
  emit("changeClickState");
};

const changeHoverState = () => {
  emit("changeHoverState");
};
</script>

<template>
  <div
    class="z-10 transition duration-500 bg-white w-48 aspect-[5/7] rounded-2xl absolute translate-x-1 rotate-1"
    :class="{
      'scale-105': isHovered,
      '-translate-x-[8rem] translate-y-[1rem] rotate-[-20deg]': isClicked,
    }"
    @click="changeClickState"
    @mouseover="changeHoverState"
    @mouseleave="changeHoverState"
  >
    <img
      src="../images/spa.png"
      alt="spa"
      class="rounded-[inherit] border-2 border-white"
    />
  </div>

  <!-- <div
    class="z-10 transition duration-500 bg-white w-48 aspect-[5/7] rounded-2xl absolute translate-x-1 rotate-1"
    :class="{
      'scale-105': isHovered,
      '-translate-x-[8rem] translate-y-[1rem] rotate-[-20deg]': isClicked,
    }"
    @click="changeClickState()"
    @mouseover="changeHoverState()"
    @mouseleave="changeHoverState()"
  >
    <img
      src="../images/spa.png"
      alt="spa"
      class="rounded-[inherit] border-2 border-white"
    />
  </div> -->
</template>

<style scoped></style>
