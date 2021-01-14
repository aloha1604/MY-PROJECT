<template>
    <div class="hello">
        {{ counter }}
    </div>
</template>

<script>
export default {
    name: "HelloWorld",
    data() {
        return {
            counter: 0,
        };
    },
    beforeUpdate() {
        console.log("beforeUpdate", this.counter); // Logs the counter value every second, before the DOM updates.
    },
    updated() {
        console.log("Updated", this.counter); // Logs the counter value every second, before the DOM updates.
    },
    created() {
        console.log("createdbefoe", this.counter);
        setInterval(() => {
            this.counter++;
        }, 1000);
        console.log("createdafter", this.counter);
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
    font-weight: normal;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
</style>
