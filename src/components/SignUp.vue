<template>
  <h1>Signup</h1>
  <form action="" @submit.prevent="submitbtn">
    <label for="">Email</label><br>
    <input type="email" v-model="email" required><br>
    <label for="">Password</label><br>
    <input type="password" v-model="password" required><br>
    <label for="">Roles</label>
    <select name="" id="" v-model="roles">
        <option value="Web developer">Web Developer</option>
        <option value="Web designer">Web Designer</option>
    </select>
    <div>
        <input type="checkbox" v-model="names">

        <label for="">Accpect Terms and Condition</label>
    </div>
   
    <div>
        <label for="">Skills</label>
        <input type="text" @keyup="addKey" v-model="skill">
    </div>
    <div v-for="skill in skills" :key="skill">
        <p>{{skill}}<span class="cus" @click="remove(skill)">&#10006;</span></p>
    </div>
  
    <input type="submit">
  </form>
  {{ email  }} <br>
  {{ password  }} <br>
  {{ roles }} <br>
  <!-- {{ appect }} <br>
  {{ names }} -->
</template>

<script>
// import func from '../../vue-temp/vue-editor-bridge';
export default {
    name:'SignUp',
    data(){
        return{
            email:"",
            password:"",
            roles:"",
            appect:false,
            names:[],
            skills:[],
            skill:"",
        }
    },
    methods:{
        addKey(event)
        {
            if(event.key === ",")
            {
               this.skills.push(this.skill);
               this.skill="";

            }
        },
        submitbtn()
        {
            console.log('submit')
        },
        remove(skill)
        {
            this.skills = this.skills.filter(function(s){
                return skill !== s
            })
        }
    }
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
    input,select{
        display: block;
        margin:15px 0  20px;
        border: none;
        border-bottom: 1px solid blanchedalmond;
        width: 80%;
        padding:10px 0 10px;
    }
    input[type="checkbox"]{
        position: relative;
        margin: 0 10px 0 0;
        display: inline-block;
    }
    .cus{
        cursor: pointer;
    }
</style>