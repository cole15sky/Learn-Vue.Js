<template>
    <div class="container">

        <div class="wrapper">

            <h1> Login</h1>

<div>
    <label for="username">Username:</label> 
<input type="text" placeholder="Enter your email" v-model="email"> 
<label for="password">Password:</label> 
<input type="password" placeholder="Enter the password" v-model="password">
      </div> <br>
      <button v-on:click="getData()" type="button">LogIn</button> 
      <h5> Don't have account? <u>SignUp</u></h5>
      
    </div>
   </div>
        
</template>


<script> 
export default{
    name: "Header",
    data(){
    return{
        email:'',
        password:''
    }

    },
    methods: {
        getData() {
            // Simple validation checks
            if (!this.email || !this.password) {
                alert("Both fields are required!");
                return;
            }
            
            // Basic email validation regex
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailRegex.test(this.email)) {
                alert("Please enter a valid email address.");
                return;
            }

            console.log("Values:", {
                username: this.email,
                password: this.password
            });
        }
    }
};

    


</script>




<style scoped>
h1{
    text-align: center;
    color: blue;
}
.container{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: blanchedalmond;
    height: 300px;
    width: 250px;
    border: 2px solid blue;
    border-radius: 8%;
    margin: auto; 
    position: relative;
}

.wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

u{
    color: blue;
}

input{
    margin-left: 15px;
    font-size: 15px;
}

label{
    margin-left: 25px;
    font-family: 'Times New Roman', Times, serif;
    font-size: 15px;
}

button{
    background-color: blue;
    color: white;
    border-radius: 20%;
}
</style>




