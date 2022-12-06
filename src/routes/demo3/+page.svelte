<script lang="ts">
	import { Modal, modalStore, type ModalSettings } from '@skeletonlabs/skeleton';

	function triggerAlert(): void {
		const alert: ModalSettings = {
			type: 'alert',
			title: 'Example Alert',
			body: 'This is an example modal.',
			image: 'https://i.imgur.com/WOgTG96.gif'
		};
		modalStore.trigger(alert);
	}
</script>

<Modal />

<pre>queue: {JSON.stringify($modalStore, null, 2)}</pre>
<button on:click={triggerAlert} class="btn btn-ghost-accent">Open Modal</button>
