<template>
	<div id="test" class="test">
		<h3>{{title}}</h3>
		
		<label><strong>Title</strong></label> <input type="text" v-model="title" v-on:keyup="presskey">
		<br/><br/>
				
		<p><strong>User:</strong> {{fullName}}</p>
		
		<hr/>
		<br/>
		<label><strong>First Name</strong></label> <input type="text" v-model="user.fname">
		<br/><br/>
		<label><strong>Last Name</strong></label> <input type="text" v-model="user.lname">		
	</div>
</template>

<script>
	export default {
		name: 'test',
		props: {
			msg: {
				type: String,
				default: 'Default Message'
			}
		},
		data() {
			return {
				title: 'Vue Demo App 1',
				user: {
					fname: 'Anita',
					lname: 'Bathe'
				},
				showLastName: true,
				items: [
					{title:'Item One',},
					{title:'Item Two',},
					{title:'Item Fifteen',}
				]
			}
		},
		methods: {
			start: function() {
				var itemCount = this.items.length;
				alert(itemCount + ' items');
			},
			presskey: function(e) {
				var str = e.target.value;
				var patt = /^(\s)+$/;
				
				this.title = (str.length && !patt.test(str))?str: "Vue Demo App 1";
			}
		},
		computed: {
			fullName: function() {
				return this.user.fname + ' ' + this.user.lname;
			}
		}
	}
</script>

<style scoped>
	div {
		padding:1%;
	}
</style>