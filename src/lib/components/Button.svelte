<script lang="ts">
	import type { HTMLButtonAttributes } from 'svelte/elements';
	import { twJoin, twMerge } from 'tailwind-merge';

	type $$Props = HTMLButtonAttributes & {
		className?: string;
		href?: string;
		variant?: 'default' | 'primary';
		onClick?: () => void;
	};

	export let className: $$Props['className'] = '';
	export let href: $$Props['href'] = '';
	export let variant: $$Props['variant'] = 'default';
	export let onClick: $$Props['onClick'] = undefined;

	$: _class = twMerge(
		'font-medium flex items-center justify-center',
		'shadow-sm rounded-lg border !leading-none',
		'px-4 py-3.5 text-base',
		'bg-white border-neutral-300/70 hover:bg-neutral-50',
		variant === 'primary' &&
			twJoin(
				'bg-blue-500 border-blue-500 text-white hover:bg-blue-600/90 hover:border-blue-600/90'
			),
		className
	);
</script>

{#if href}
	<a {href} class={_class} {...$$restProps}>
		<slot />
	</a>
{:else}
	<button class={_class} on:click={onClick} {...$$restProps}>
		<slot />
	</button>
{/if}
