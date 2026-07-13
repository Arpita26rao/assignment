<script lang="ts">
	let activeTab: "login" | "register" = "login";
</script>

<svelte:head>
	<title>Login - Bulk Email Sender</title>
</svelte:head>

<div class="page">
	<div class="card">
		<h1>Email Sender</h1>
		<p>Secure bulk email management</p>

		<div class="tabs">
			<button
				class:active={activeTab === "login"}
				onclick={() => (activeTab = "login")}
			>
				Sign In
			</button>

			<button
				class:active={activeTab === "register"}
				onclick={() => (activeTab = "register")}
			>
				Sign Up
			</button>
		</div>

		{#if activeTab === "login"}
			<h2>Login Form</h2>
		{:else}
			<h2>Register Form</h2>
		{/if}
	</div>
</div>

<style>
	.page {
		min-height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
		background: linear-gradient(135deg, #667eea, #764ba2);
		padding: 2rem;
	}

	.card {
		width: 100%;
		max-width: 450px;
		padding: 2rem;
		background: rgba(255, 255, 255, 0.95);
		border-radius: 20px;
		box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
		text-align: center;
	}

	.tabs {
		display: flex;
		gap: 1rem;
		margin: 2rem 0;
		justify-content: center;
	}

	button {
		padding: 10px 20px;
		border: none;
		border-radius: 10px;
		cursor: pointer;
		font-weight: 600;
	}

	.active {
		background: #667eea;
		color: white;
	}
</style>