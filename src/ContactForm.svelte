<script>
	import contacts from "./store/contacts";

	// binding values
	let name = "";
	let surname = "";
	let mail = "";

	// submit contact
	const submitContact = () => {
		contacts.addContact({ name, surname, mail });
		// reset values
		name = surname = mail = "";
	}
</script>

<div id="contactForm">
	<input type="text" 	bind:value={name} placeholder="Insert name" />
	<input type="text" 	bind:value={surname} placeholder="Insert surname" />
	<input type="email" bind:value={mail} placeholder="Insert mail" />
	<input type="submit" on:click={submitContact} value="Add" />
	<input type="submit" on:click={contacts.reset} value="Reset" />
</div>