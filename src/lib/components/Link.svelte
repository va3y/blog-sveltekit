<script>
	export let inNewTab = false;
	export let prefetch = false;
	export let href;
</script>

<a
	sveltekit:prefetch={prefetch ? true : false}
	target={inNewTab ? '_blank' : ''}
	rel={inNewTab ? 'noopener noreferrer' : ''}
	class="text-rose-600 dark:text-rose-700 hover:underline underline-offset-2 {$$restProps.class ||
		''}"
	{href}
>
	<slot />
</a>
