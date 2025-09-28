<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Privacy by default",
			description: "We believe privacy isn't a feature—it's the foundation. Octra is designed to compute on encrypted data without ever exposing it."
		},
		{
			title: "Decentralization as a principle",
			description: "Trust comes from transparency, not central control. Octra runs on a peer-to-peer network with no central authority."
		},
		{
			title: "Applied cryptography, real impact",
			description: "We're advancing fully homomorphic encryption to solve real-world problems. By enabling computation on encrypted inputs, we make it possible to build AI systems that don't compromise privacy."
		},
		{
			title: "Open by design",
			description: "Octra Labs is a non-profit research association committed to open source development and peer-reviewed innovation."
		}
	];
</script>

<SecondaryHero
	generating
	title="Solving world hunger"
	subtitle="one step at a time"
	imageSrc="https://www.unc.mn/image-placeholder.svg"
/>

<!-- Story Section -->
<Story
	generating
	paragraphs={[
		"We started in 2018 with a simple goal: make helpful tech that people actually need. While many chase profits, we chose to do things differently.",
		"Beyond making good products, we care about doing the right thing, being kind to our planet, and making sure everyone can use what we build. That's our compass.",
		"From day one, we've asked ourselves: 'Does this actually help people?' This question gets us through tough calls and shapes who we are. We're playing the long game here.",
		"We think about how our work affects real people's lives. We build tech that brings people together, keeps your information safe, and treats everyone fairly. When we stick to these basics, good things happen."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- Team and investors sections removed as Octra Labs is a non-profit research association with no specific team members or investors mentioned in the company context -->

<!-- CTA Section -->
<CallToAction
	title="Be the first to build with next-gen privacy tech"
	subtitle="From AI to web3, the future is private"
	description="Start building with Octra's developer tools today and stay ahead of the curve. Power AI models with confidential data, or enable fully private logic on-chain—all without exposing sensitive information."
	imageSrc="/generated/image-a-candid-documentary-style-photograph-of.webp"
	callsToAction={[
		{
			href: "#",
			label: "Start building with Octra",
			variant: "primary"
		},
		{
			href: "#",
			label: "Contact our enterprise team",
			variant: "secondary"
		}
	]}
/>
