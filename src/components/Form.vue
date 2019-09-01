
<template>
	<form>
		<label for="first_name">First Name</label>
		<input name="first_name" type="text" placeholder="Enter first name">

		<div class="buttonset">
			<button>Submit</button>
		</div>
	</form>
</template>

<script>
export default {

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

