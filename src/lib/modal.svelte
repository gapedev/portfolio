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
  <button autofocus on:click={close}></button>
  <slot name="header"></slot>
	<slot></slot>
  
 
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
		position: absolute;
    right: 0;
    top: 6.25rem;
    width: 29.0625rem;
		padding: 2.8125rem;
    max-width: 32em;
    max-height: calc(100vh - 4em);
    overflow: auto;
    padding: 1em;
    border-radius: 0.2em;
    background: white;
		-webkit-animation: scale-up-hor-right 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: scale-up-hor-right 0.4s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	}
	button {
    font-size: 1rem;
    width: 1.875rem;
    background: none;
    color: #0052CC;
    cursor: pointer;
    border: none;
    justify-content: right;
    position: absolute;
    right: 1.875rem;
	}

	button:hover {
		-webkit-animation: rotate-center 0.6s ease-in-out both;
	        animation: rotate-center 0.6s ease-in-out both;
	}

@-webkit-keyframes scale-up-hor-right {
  0% {
    -webkit-transform: scaleX(0.4);
            transform: scaleX(0.4);
    -webkit-transform-origin: 100% 100%;
            transform-origin: 100% 100%;
  }
  100% {
    -webkit-transform: scaleX(1);
            transform: scaleX(1);
    -webkit-transform-origin: 100% 100%;
            transform-origin: 100% 100%;
  }
}
@keyframes scale-up-hor-right {
  0% {
    -webkit-transform: scaleX(0.4);
            transform: scaleX(0.4);
    -webkit-transform-origin: 100% 100%;
            transform-origin: 100% 100%;
  }
  100% {
    -webkit-transform: scaleX(1);
            transform: scaleX(1);
    -webkit-transform-origin: 100% 100%;
            transform-origin: 100% 100%;
  }
}
@-webkit-keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
            transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
  }
}
@keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
            transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
  }
}


</style>