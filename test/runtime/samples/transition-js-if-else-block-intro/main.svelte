<script>
	export let yes;
	export let no;

	export let x;

	function foo(node, params) {
		return {
			duration: 400,
			tick: t => {
				node.foo = t;
			}
		};
	}
</script>

{#if x}
	<div bind:this={yes} in:foo>yes</div>
{:else}
	<div bind:this={no} in:foo>no</div>
{/if}