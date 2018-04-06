<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User Name: {{ myName }} - {{ switchName() }}</p>
        <p>User Age: {{ userAge }}</p>
        <button @click="resetName">Reset name</button>
        <button @click="resetFn()">Reset name</button>
    </div>
</template>

<script>
  export default {
    //props: ['myName'],
    props: {
      //myName: [String, Array]
      myName: {
        type: String,
        // required: true,
        default: 'DEFAULT'
      },
      resetFn: Function,
      userAge: Number
    },
    methods: {
      switchName() {
        console.log('switchName mathod');
        return this.myName.split("").reverse("").join("~");
      },
      resetName() {
        // this.myName = 'Reset';
        // this.$emit('nameWasReset', this.myName);
        this.$emit('nameWasReset', 'Max');
      },
      created() {

      }
    }
  }
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
