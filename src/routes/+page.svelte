<script lang="ts">
	import { page } from '$app/stores';
	import Schema from '$lib/schema.svelte';

	const schema = {
		'@type': 'BlogPosting',
		headline: 'some thing',
		name: 'yup',
		author: {
			'@type': 'Person',
			name: 'johnny appleseed',
			url: $page.url.origin,
			alternateName: 'name',
			identifier: '0123'
		},
		datePublished: new Date().toISOString(),
		dateModified: new Date().toISOString(),
		dateCreated: new Date().toISOString(),
		articleBody: 'some text here',
		description: 'short text',
		image: 'https://en.wikipedia.org/wiki/Image#/media/File:Image_created_with_a_mobile_phone.png',
		keywords: 'some, thing, here',
		timeRequired: '1' + 'M',
		identifier: '0231',
		url: $page.url.origin,
		publisher: {
			'@type': 'Organization',
			name: 'this fake org'
		}
	};
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<Schema {schema} />
