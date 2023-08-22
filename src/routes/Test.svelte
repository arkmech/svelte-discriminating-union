<script lang="ts">
	type $$Props = {
		name: string;
	} & (
		| { color?: 'red' }
		| {
				color: 'green';
				uniqueProp?: string;
		  }
	);
	export let name: $$Props['name'];
	export let color: $$Props['color'];
	export let uniqueProp: $$Props['uniqueProp'];
</script>

<div>{name}</div>
{#if color === 'red'}
	<div>Red</div>
{:else if color === 'green'}
	<div>Green</div>
	<div>{uniqueProp}</div>
{/if}
