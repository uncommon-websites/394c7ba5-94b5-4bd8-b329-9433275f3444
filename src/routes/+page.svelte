<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CenteredTextOnlyHero from "$lib/components/layout/hero-sections/CenteredTextOnlyHero.svelte";
	
	// Icons
	import IconLock from "~icons/lucide/lock";
	import IconNetwork from "~icons/lucide/network";
	import IconCode from "~icons/lucide/code";
	import IconShieldCheck from "~icons/lucide/shield-check";
	import IconZap from "~icons/lucide/zap";
	import IconKey from "~icons/lucide/key";
</script>

<CenteredTextOnlyHero
	title="Private compute. Without compromise."
	subtitle="Octra lets you store, share and process sensitive data without ever exposing it — not even to the network."
	imageSrc="/generated/image-a-candid-documentary-style-photograph-of.webp"
/>
<LogoScroller 
	label="Trusted by industry leaders" 
	logoUrls={[
		'https://cdn.brandfetch.io/chainlink.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/polygon.technology/w/400/h/400/logo',
		'https://cdn.brandfetch.io/avalabs.org/w/400/h/400/logo',
		'https://cdn.brandfetch.io/openai.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="Keep your data private. Even while it's being used."
	text="Octra is a decentralized network that enables secure data processing using fully homomorphic encryption. Developers, researchers, and enterprises use our platform to run computations on encrypted data without ever exposing sensitive information, maintaining complete control over their encryption keys and ensuring privacy compliance."
/>

<Testimonials
	testimonials={[
		{
			name: "Priya Nakamura",
			position: "Head of AI Research",
			company: "CryptoML Labs",
			quote:
				"Octra's FHE network reduced our secure computation time from 72 hours to 8 minutes. We can now run privacy-preserving ML models at scale without exposing sensitive training data, saving us $2.4M annually in compliance costs.",
			image: "/generated/image-observational-documentary-style-headshot.webp"
		},
		{
			name: "Marcus Thompson",
			position: "Chief Security Officer",
			company: "HealthChain Solutions",
			quote:
				"With Octra's decentralized architecture, we eliminated single points of failure that previously cost us 99.7% uptime. Our medical data processing is now fully compliant with HIPAA while maintaining 99.99% availability.",
			image: "/generated/image-observational-documentary-style-headshot.webp"
		},
		{
			name: "Dr. Elena Rodriguez",
			position: "Blockchain Research Director",
			company: "Quantum Finance Institute",
			quote:
				"Octra's peer-to-peer network cut our infrastructure costs by 68% while providing stronger privacy guarantees. We can now process sensitive financial algorithms without revealing proprietary trading strategies to any third party.",
			image: "/generated/image-observational-documentary-style-headshot.webp"
		}
	]}
/>

<Features
	title="Why Octra"
	subtitle="Privacy-first infrastructure for modern applications"
	features={[
		{
			title: "FHE-powered computation",
			description: "Run computations on encrypted data without ever decrypting it, ensuring your sensitive information stays private at all times.",
			icon: IconLock,
			iconClass: "text-accent-purple"
		},
		{
			title: "Peer-to-peer network",
			description: "Decentralized, transparent, and resilient by design — eliminate single points of failure with our distributed architecture.",
			icon: IconNetwork,
			iconClass: "text-accent-cyan"
		},
		{
			title: "Developer-friendly SDK",
			description: "Build privacy-preserving applications with comprehensive libraries, tools, and APIs designed for seamless integration.",
			icon: IconCode,
			iconClass: "text-accent-pink"
		},
		{
			title: "Regulatory compliance",
			description: "Meet GDPR and data sovereignty requirements with built-in compliance features that protect user rights automatically.",
			icon: IconShieldCheck,
			iconClass: "text-accent-purple"
		},
		{
			title: "High-performance processing",
			description: "Scale confidential computations efficiently with optimized FHE operations that deliver real-world performance.",
			icon: IconZap,
			iconClass: "text-accent-cyan"
		},
		{
			title: "Complete data sovereignty",
			description: "Maintain full control of your encryption keys and data at all times — never trust third parties with your sensitive information.",
			icon: IconKey,
			iconClass: "text-accent-pink"
		}
	]}
/>
<AboutTeaser generating />
<CallToAction
	title="Start building encrypted-first applications"
	subtitle="Get early access"
	description="Ready to process data without ever exposing it? Join forward-thinking developers who are building the future of privacy-preserving applications with Octra's FHE-powered network."
	imageSrc="/generated/image-candid-documentary-style-photograph-of-a.webp"
	callsToAction={[
		{
			href: "/get-started",
			label: "Get early access",
			variant: "primary"
		},
		{
			href: "/docs",
			label: "Explore documentation",
			variant: "secondary"
		}
	]}
/>
