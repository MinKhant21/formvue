<template>
  <h1>Signup</h1>
  <form action="">
    <label for="">Email</label><br>
    <input type="email" required><br>
    <label for="">Password</label><br>
    <input type="password" required><br>
    <label for="">Work</label><br>
    <input type="text"><br>
    <!-- <input type="checkbox">Accpect -->
    <input type="submit">
  </form>
</template>

<script>
export default {
    name:'SignUp'
}
</script>

<style scoped>
    form{
        max-width: 490px;
        background-color: white;
        margin:30px auto;
        text-align: left;
        padding: 30px 0 0 40px;
    }
    label{
        padding:30px 0 15px;
        text-transform: uppercase;
        color: gray;
        font-size: 0.6em;
    }
    input{
        margin:15px 0  20px;
        border: none;
        border-bottom: 1px solid blanchedalmond;
        width: 80%;
        padding:10px 0 10px;
    }
</style>