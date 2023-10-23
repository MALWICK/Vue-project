<template>
    <section v-if="showWarn">
<div class="contaner" @click.stop>
    <div class="close" >
        <button @click="close">x</button>
    </div>
    <div class="inner-container">
        <h2>please fill in the form above</h2>
    </div>
</div>
    </section>
</template>

<script>

export default {
    name: 'WarnPopup',
    props: {
    showWarn: Boolean
  },
  methods: {
    close() {
        this.$emit('close');
    }
  }
   
}
</script>

<style scoped>
.contaner {
    width: 100%;
    height: 130px;
    border: 3px solid #525151;
    border-radius: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.close {
    height: 50px;
    width: 95%;
    display: flex;
    align-items: center;
    justify-content: right;
}

.close button {
    width: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 22px;
    font-weight: 700;
    border-radius: 50%;
    color: red;
    border: 2px solid lightgray;
    cursor: pointer;
}

.inner-container {
    height: 70px;
    width: 95%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}
</style>