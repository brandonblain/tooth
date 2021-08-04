<style scoped>
html, body{
	width:100%;
	height:100%;
	margin:0px;
	font-family: 'Work Sans', sans-serif;
}

body{
		background-color:blue;
	  background-size: cover;
		display: flex;
		flex-direction:column;
		justify-content:center;
	  align-items:center;
		color: #fff;
}

section{
	background-color: rgba(0, 0, 0, 0.72);
	width:25%;
	min-height:25%;
	display:flex;
	flex-direction:column;
	/*margin-left:auto;
	margin-right:auto;*/
}
form{
	display:flex;
	flex-direction:column;
	padding: 15px; 
}
h2{
	font-family: 'Archivo Black', sans-serif;
	color:#e0dada;
	margin-left:auto;
	margin-right:auto;
}

.info{
	width:100%;
	padding: 1em 5px;
	text-align:center;
	min-height:45px;
	display:flex;
	flex-direction:column;
	justify-content:center;
	align-items:center;
}

.info.error{
	border:1px solid #a90e0;
	background-color: #ff3c41;
	color:#a90e0;
}
.info p{
	margin:auto;
	padding:5px;
}
.info.good{
	border:1px solid #416d50;
	background-color: #47cf73;
	color:#416d50;
}
.imagelogin{
  background-size: 100% 100%;
  background-repeat:no-repeat;
  background:url(public/media/loginimage.jpg);
  background-size: cover;
}
input{
	height:35px;
	padding: 5px 5px;
	margin: 10px 0px;
	background-color:#e0dada;
	border:none;
}
button{
	height:40px;
	padding: 5px 5px;
	margin: 10px 0px;
	font-weight:bold;
	background-color:#be5256;
	border:none;
	color:#e0dada;
	cursor:pointer;
	font-size:16px;
}
button:hover{
	background-color:#711f1b;
}

.shake{
	animation-name: shake;
	animation-duration:1s;
	/*animation-fill-mode: both;*/
}

@media screen and (max-width: 780px) {
	section{
		width:90%;
	}
}
</style>




<template>
<div class="container">
	<div class="row">
	 <v-img :src="mymedia"></v-img>
    <div class="wrap">
        <div>
            <img id="fondo" style="width:100%;">
        </div>
        <form>
        <h2>Login Ortho Jáquez</h2>
        <div class="info" v-bind:class="good">
        <p v-show="login.login && login.password">{{ login.login}} / {{ login.password}}</p>
        </div>
        <input type="text" v-model="login.login" placeholder="Username" />
        <input type="password" v-model="login.password" placeholder="Password" />
        <button v-on:click="onSubmit">Log in</button>
        </form>
    </div>
	</div>
    </div>
</template>

<script>
    export default {
      data(){
          return{
              alert: {
                 message: "hello world"
             },
             login: {
                 login: "",
                 password: ""
             },
             shake: false,
             good: "",
             fake: {
                 login: "vincent",
                 password: "admin"
             },
			 mymedia:'public_path(media/loginimage.jpg)',
         }
         },
	computed: {
		isShake: function(){
			console.log(this.shake);
			if(this.shake == true){
				return 'shake'
			}
			return 'none'
		}
	},
	methods: {
		onSubmit: function(event) {
			event.preventDefault();
			this.shake = false
			setTimeout(function(){
				if (
				this.fake.login == this.login.login &&
				this.fake.password == this.login.password
			) {
				this.alert.message = "Hello Huston !";
			} else {
				this.shake = true;
				this.alert.message = "Huston, we got a problem !";
			}
			},3000)
			console.log(this.shake)
			
		}
	}
};

</script>
