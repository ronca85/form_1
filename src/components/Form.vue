
<template>
	<form v-on:submit.prevent="onSubmit" :class="['', validateEmail()]">
		<label>Email</label>
		<input type="email" v-model="user.email"/>
		<div class="buttonset">
			<button type="submit">Submit</button>
		</div>
	</form>
</template>

<script>
export default {
	data() {
		return {
			user : {
				email : "",
				reg: /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,24}))$/,
			}
		}
	},

	methods: {
		validateEmail: function() {
			return (this.user.email == "")? "" : (this.user.reg.test(this.user.email)) ? 'has-success' : 'has-error';
		},
		onSubmit() {
			console.log( "submit" );
			this.validateEmail;
		}
	},
}
</script>

<style>
	form {
		display: inline-flex;
		flex-direction: column;
		align-items: flex-start;
	}
	input {
		border: 2px solid #999;
		padding: 15px;
		margin-bottom: 15px;
	}
	.buttonset {
		display: flex;
		width: 100%;
		justify-content: flex-end;
	}
	button {
		margin: 0;
		border: none;
		background: #66b;
		color: #fff;
		padding: 15px;
	}
</style>

