

<script lang="ts">
  import { browser } from '$app/environment';
  import { onMount } from 'svelte';
import '../app.postcss';
	import { AppShell, AppBar} from '@skeletonlabs/skeleton';
	import { autoModeWatcher } from '@skeletonlabs/skeleton';
	// import { LightSwitch } from '@skeletonlabs/skeleton';

	onMount(() => {
		autoModeWatcher.toString()
		autoModeWatcher();
	})
	
</script>

<!-- <svelte:head>{@html `<script type="module">
    ${autoModeWatcher.toString()}
    autoModeWatcher();
  </script>`}</svelte:head> -->
<!-- <svelte:head>
	{@html `<\u{73}cript nonce="%sveltekit.nonce%">${autoModeWatcher.toString()}
    autoModeWatcher();</script>`}
</svelte:head> -->


<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<strong class="text-xl uppercase">Skeleton</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
			
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://discord.gg/EXqV7W8MtY"
					target="_blank"
					rel="noreferrer"
				>
					Discord
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://twitter.com/SkeletonUI"
					target="_blank"
					rel="noreferrer"
				>
					Twitter
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/skeletonlabs/skeleton"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
