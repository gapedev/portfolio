<script>
	import { createEventDispatcher, onDestroy } from 'svelte';

	const dispatch = createEventDispatcher();
	const close = () => dispatch('close');

	let modal;

	const handle_keydown = e => {
		if (e.key === 'Escape') {
			close();
			return;
		}
	};

	const previously_focused = typeof document !== 'undefined' && document.activeElement;

	if (previously_focused) {
		onDestroy(() => {
			previously_focused.focus();
		});
	}
</script>

<svelte:window on:keydown={handle_keydown}/>

<div class="modal-background" on:click={close}></div>

<div class="modal" role="dialog" aria-modal="true" bind:this={modal}>
	<slot name="header"></slot>
	<slot></slot>

	<!-- svelte-ignore a11y-autofocus -->
	<button autofocus on:click={close}>x</button>
</div>

<style>
	.modal-background {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0,0,0,0.3);
	}

	.modal {
		display: flex;
		justify-content: space-around;
		position: absolute;
    right: 0;
    top: 100px;
    width: 29.0625rem;
		padding: 2.8125rem;
    max-width: 32em;
    max-height: calc(100vh - 4em);
    overflow: auto;
    padding: 1em;
    border-radius: 0.2em;
    background: white;
	}

	button {
		font-size: 16px;
    height: 45px;
    width: 45px;
    background-color: orange;
    color: #fff;
    border-radius: 50%;
    transition: all 0.3s linear 0s;
		cursor: pointer;
		border: none;
	}
</style>