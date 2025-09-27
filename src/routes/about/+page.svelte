<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Privacy first",
			description: "Your data remains encrypted and under your control at all times, with FHE ensuring computation happens without exposing sensitive information."
		},
		{
			title: "Decentralized by design",
			description: "Building peer-to-peer infrastructure that eliminates single points of failure and puts control back in the hands of users."
		},
		{
			title: "Developer empowerment",
			description: "Providing the tools and libraries that make it simple to build privacy-preserving applications without compromising on functionality."
		}
	];
</script>

<SecondaryHero
	title="Privacy at the core"
	subtitle="Data stays yours. Always."
	imageSrc="/generated/image-a-diverse-group-of-people-collaborating-.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Octra Labs began as a non-profit research initiative, driven by a fundamental belief that privacy shouldn't be a privilege. We saw the growing centralization of data and knew there had to be a better way.",
		"Our breakthrough came through fully homomorphic encryption - the ability to perform computations on encrypted data without ever decrypting it. This isn't just academic research; it's the foundation for truly private, decentralized applications.",
		"As a collective of researchers and developers, we're not building for profit margins or investor returns. We're building because the future of digital privacy depends on decentralized, peer-to-peer networks that put users in control.",
		"Every protocol we develop, every tool we release, serves one purpose: enabling developers to build applications where privacy is built-in, not bolted-on. This is how we create a more secure digital world for everyone."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Research team."
	subtitle="Advancing fully homomorphic encryption."
	stakeholders={[
		{
			name: "Dr. Elena Rodriguez",
			position: "Lead Cryptographer",
			bio: "PhD in Applied Cryptography, specializing in fully homomorphic encryption protocols and privacy-preserving computation.",
			image: "/generated/image-candid-headshot-of-a-tech-researcher-in-.webp"
		},
		{
			name: "Marcus Chen",
			position: "Blockchain Architect",
			bio: "Former core developer at Ethereum Foundation, focused on decentralized infrastructure and consensus mechanisms.",
			image: "/generated/image-observational-headshot-of-a-cryptography.webp"
		},
		{
			name: "Dr. Kai Nakamura",
			position: "Research Director",
			bio: "Published researcher in privacy-preserving AI and secure multi-party computation with 15+ years in cryptographic systems.",
			image: "/generated/image-documentary-style-headshot-of-a-blockcha.webp"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Ready to build with privacy?"
	subtitle="Start developing on Octra today"
	description="Join the developers and enterprises already building the next generation of privacy-preserving applications with our FHE infrastructure and developer tools."
	imageSrc="/generated/image-candid-documentary-style-photo-of-a-prof.webp"
/>
