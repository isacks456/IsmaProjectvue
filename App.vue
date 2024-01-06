
<template>
	<div>
		<img src="/Login.png" alt="" className="logo">
		<h1 className="name">Login</h1>
	</div>
	<div class="block1">
		<form action="" @submit.prevent="CheckInput">
			<div class="document">
				<div>
					<h1>Login</h1><input type="text" v-model="email" placeholder="Name" required minlength="4"><svg
						style="color: white" xmlns="http://www.w3.org/2000/svg" width="36" height="36" fill="currentColor"
						class="ico1" viewBox="0 0 16 16">
						<path
							d="M15 14s1 0 1-1-1-4-5-4-5 3-5 4 1 1 1 1h8zm-7.978-1A.261.261 0 0 1 7 12.996c.001-.264.167-1.03.76-1.72C8.312 10.629 9.282 10 11 10c1.717 0 2.687.63 3.24 1.276.593.69.758 1.457.76 1.72l-.008.002a.274.274 0 0 1-.014.002H7.022zM11 7a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm3-2a3 3 0 1 1-6 0 3 3 0 0 1 6 0zM6.936 9.28a5.88 5.88 0 0 0-1.23-.247A7.35 7.35 0 0 0 5 9c-4 0-5 3-5 4 0 .667.333 1 1 1h4.216A2.238 2.238 0 0 1 5 13c0-1.01.377-2.042 1.09-2.904.243-.294.526-.569.846-.816zM4.92 10A5.493 5.493 0 0 0 4 13H1c0-.26.164-1.03.76-1.724.545-.636 1.492-1.256 3.16-1.275zM1.5 5.5a3 3 0 1 1 6 0 3 3 0 0 1-6 0zm3-2a2 2 0 1 0 0 4 2 2 0 0 0 0-4z"
							fill="white"></path>
					</svg>
				</div><!--?xml version="1.0" encoding="UTF-8"?-->
				<div><input type="password" v-model="password" placeholder="password" required minlength="8"><svg class="ico2"
						style="color: white" xmlns="http://www.w3.org/2000/svg" width="45" height="45" fill="currentColor"
						viewBox="0 0 16 16">
						<path
							d="M0 8a4 4 0 0 1 7.465-2H14a.5.5 0 0 1 .354.146l1.5 1.5a.5.5 0 0 1 0 .708l-1.5 1.5a.5.5 0 0 1-.708 0L13 9.207l-.646.647a.5.5 0 0 1-.708 0L11 9.207l-.646.647a.5.5 0 0 1-.708 0L9 9.207l-.646.647A.5.5 0 0 1 8 10h-.535A4 4 0 0 1 0 8zm4-3a3 3 0 1 0 2.712 4.285A.5.5 0 0 1 7.163 9h.63l.853-.854a.5.5 0 0 1 .708 0l.646.647.646-.647a.5.5 0 0 1 .708 0l.646.647.646-.647a.5.5 0 0 1 .708 0l.646.647.793-.793-1-1h-6.63a.5.5 0 0 1-.451-.285A3 3 0 0 0 4 5z"
							fill="white"></path>
						<path d="M4 8a1 1 0 1 1-2 0 1 1 0 0 1 2 0z" fill="white"></path>
					</svg></div>
				<button type="submit">Login</button>
				<div this.localServer></div>
			</div>
		</form>
	</div>
</template>


<script>
export default {
	data() {
		return {
			email: '',
			password: '',
			localServer: ''
		};
	},
	methods: {
		CheckInput() {
			if (this.email.length >= 4 && this.password.length >= 8) {
				alert("Welcome" + " " + this.email),
					open("./assets/IconSupport.vue")
			} else {
				// You can add some logic for invalid input here
			}
		},
	},
};

</script>

<style scoped>
.block1 {
	border: 4px solid rgb(221, 208, 180);
	width: 268px;
	height: 268px;
	border-radius: 14px;
}

.document {
	position: relative;
	top: 58px;
	right: -44px;
}

.block1 input {
	margin: 4px;
	padding: 4px;
	border-radius: 4px;
	transition: all 1.1s ease;
	background: transparent;
	border: 1px solid silver;
	color: #ffff;
}

.block1 input:hover {
	cursor: pointer;
	border-color: yellow;
}

.block1 input:valid {
	border-color: aquamarine;
}

.block1 button {
	position: relative;
	right: -114px;
	padding: 4px;
	top: 14px;
	border-radius: 4px;
	background: transparent;
	border: 1px solid silver;
	color: rgb(160, 147, 147);
	transition: all 1.5s ease;

}

.block1 button:hover {
	cursor: pointer;
	border-color: yellow;
	transform: translateX(4px);
}

.block1 h1 {
	position: relative;
	font-size: 1.6rem;
	top: -14px;
	left: 44px;
	color: rgb(102, 95, 95);
	text-decoration: underline;
	transition: all 3.5s ease;
}

.block1 h1:hover {
	cursor: default;
}

.ico1 {
	position: relative;
	left: -211px;
	top: 14px;
	width: 28px;
}

.ico2 {
	position: relative;
	left: -214px;
	width: 35.4px;
	top: 16px;
}

.logo {
	position: relative;
	width: 158px;
	top: -98px;
	left: -568px;
}

.name {
	position: relative;
	width: 158px;
	top: -98px;
	left: -516px;
	color: #454141;
	font-size: 2.1rem;
	transition: all 3.5s ease;
}

.name:hover {
	cursor: default;
}
</style>
