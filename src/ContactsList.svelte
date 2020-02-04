<script>
	import contacts from "./store/contacts";
</script>

<div id="contactsList">
	{ #each $contacts as contact }
		<p>{contact.name} {contact.surname}</p>
		<p>{contact.mail}</p>
		<hr />
	{ /each }
</div>