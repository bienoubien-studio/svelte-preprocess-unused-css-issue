<script lang="ts">
	import { Label as LabelPrimitive } from 'bits-ui';

	let {
		ref = $bindable(null),
		class: className,
		...restProps
	}: LabelPrimitive.RootProps = $props();
</script>

<LabelPrimitive.Root bind:ref class="cms-label {className}" {...restProps} />

<style lang="postcss">
	:global(.cms-label) {
		display: inline-block;
		font-size: var(--cms-text-sm);
	}
	:global(.cms-label ~ :disabled) {
		opacity: 0.7;
		cursor: not-allowed;
	}
</style>
