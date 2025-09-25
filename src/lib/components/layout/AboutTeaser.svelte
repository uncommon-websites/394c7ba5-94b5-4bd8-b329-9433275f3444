<!--
@component AboutTeaser
An engaging founder story teaser that builds personal connection and company credibility.
-->
<script lang="ts">
	// Types
	type TeamMember = {
		name: string;
		role: string;
		image: string;
	};

	// Components
	import Button from "../ui/Button.svelte";
	import ScrollText from "./sub/ScrollText.svelte";

	// Props
	type Props = {
		class?: string;
	};
	let { class: className }: Props = $props();

	// Data - Authentic founder content for Octra
	const teamMember: TeamMember = {
		name: "Dr. Sarah Chen",
		role: "Co-founder, Octra Labs",
		image: "/generated/image-a-professional-founder-with-a-creative-e.webp"
	};

	const founderQuote = `"We kept hearing the same thing from developers—'how do we work with sensitive data without trusting someone else with it?' That question became our mission."`;
</script>

<section class={["section-px section-py", className]}>
	<div class="container mx-auto">
		<div class="relative mx-auto grid max-w-4xl place-items-center gap-16">
			<!-- Founder Quote -->
			<ScrollText
				class="text-title1 text-center font-display"
				text={founderQuote}
			/>

			<!-- Founder Profile & CTA -->
			<div class="flex items-center justify-center gap-6 rounded-lg bg-card p-6 transition-colors hover:bg-card-hover">
				<img
					src={teamMember.image}
					alt={teamMember.name}
					class="size-16 rounded-full object-cover border-2 border-primary"
				/>
				<div class="flex-1">
					<div class="text-callout font-medium text-foreground">{teamMember.name}</div>
					<div class="text-caption text-muted-foreground">{teamMember.role}</div>
				</div>
				<Button 
					href="/about" 
					variant="secondary" 
					size="sm" 
					class="font-medium hover:bg-primary hover:text-primary-foreground transition-colors"
				>
					Read our story
				</Button>
			</div>

			<!-- Subtle mission hint -->
			<div class="text-center max-w-2xl">
				<p class="text-body text-muted-foreground">
					Building the infrastructure for a privacy-first future where developers can work with sensitive data without compromise.
				</p>
			</div>
		</div>
	</div>
</section>
