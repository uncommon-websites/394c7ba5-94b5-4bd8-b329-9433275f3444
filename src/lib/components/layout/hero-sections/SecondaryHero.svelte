<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";

	let {
		title,
		subtitle,
		imageSrc = "https://www.unc.mn/image-placeholder.svg",
		...rest
	}: {
		title: string;
		subtitle: string;
		imageSrc: string;
		[key: string]: any;
	} = $props();
</script>

<header class={[
	'relative overflow-hidden',
	'border-b border-border',
	'bg-gradient-to-br from-secondary-50 via-white to-mint-50',
	'dark:from-gray-950 dark:via-gray-900 dark:to-gray-950'
]} {...rest}>
	<!-- Subtle pattern overlay -->
	<div class="absolute inset-0 opacity-50" style="background-image: url('data:image/svg+xml,%3Csvg width=%2260%22 height=%2260%22 viewBox=%220 0 60 60%22 xmlns=%22http://www.w3.org/2000/svg%22%3E%3Cg fill=%22none%22 fill-rule=%22evenodd%22%3E%3Cg fill=%22%23000000%22 fill-opacity=%220.02%22%3E%3Cpath d=%22M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z%22/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');"></div>

	<div class="relative container mx-auto section-px section-py">
		<div class="grid gap-16 gap-y-8 lg:gap-24">
			<!-- Enhanced header with gradient text -->
			<div class="text-center max-w-4xl mx-auto space-y-6">
				<h1 class={[
					'text-display font-[700]',
					'bg-gradient-to-r from-primary-600 via-primary-500 to-mint-500',
					'bg-clip-text text-transparent',
					'tracking-tight'
				]}>
					{title}
				</h1>
				<p class={[
					'text-title2 font-[500]',
					'text-muted-foreground',
					'max-w-2xl mx-auto',
					'leading-relaxed'
				]}>
					{subtitle}
				</p>
			</div>

			<!-- Enhanced image with frame styling -->
			<div class="relative max-w-5xl mx-auto">
				<!-- Window-style frame -->
				<div class={[
					'relative',
					'border border-border',
					'rounded-lg',
					'bg-card',
					'p-1',
					'transition-all duration-300',
					'hover:border-primary-300',
					'hover:shadow-lg hover:shadow-primary-500/10'
				]}>
					<div class="aspect-video overflow-hidden rounded-md bg-muted">
						<img
							class={[
								'h-full w-full object-cover',
								'transition-transform duration-500',
								'hover:scale-105'
							]}
							src={imageSrc}
							alt="Octra team collaborating in their workspace"
						/>
					</div>
				</div>

				<!-- Decorative elements -->
				<div class="absolute -top-2 -right-2 w-4 h-4 bg-mint-400 rounded-full opacity-80"></div>
				<div class="absolute -bottom-2 -left-2 w-3 h-3 bg-secondary-300 rounded-full opacity-60"></div>
			</div>
		</div>
	</div>
</header>
