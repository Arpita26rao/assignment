
<script lang="ts">
	let activeTab: "login" | "register" = "login";
</script>

<svelte:head>
	<title>Login - Bulk Email Sender</title>
</svelte:head>

<main>
	<h1>Email Sender</h1>
	<p>Secure bulk email management</p>

	<div>
		<button on:click={() => (activeTab = "login")}>
			Sign In
		</button>

		<button on:click={() => (activeTab = "register")}>
			Sign Up
		</button>
	</div>

	{#if activeTab === "login"}
		<h2>Login Form</h2>
	{:else}
		<h2>Register Form</h2>
	{/if}
</main>