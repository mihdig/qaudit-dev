<script lang="ts">
	import '../app.css';
	import { Moon, Sun, Menu, X } from 'lucide-svelte';

	let { children } = $props();

	let isDark = $state(true);
	let mobileMenuOpen = $state(false);
	let scrolled = $state(false);

	$effect(() => {
		if (typeof window !== 'undefined') {
			// Check system preference or stored preference
			const stored = localStorage.getItem('theme');
			if (stored) {
				isDark = stored === 'dark';
			} else {
				isDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
			}
			updateTheme();

			// Scroll listener
			const handleScroll = () => {
				scrolled = window.scrollY > 20;
			};
			window.addEventListener('scroll', handleScroll);
			return () => window.removeEventListener('scroll', handleScroll);
		}
	});

	function toggleTheme() {
		isDark = !isDark;
		updateTheme();
		localStorage.setItem('theme', isDark ? 'dark' : 'light');
	}

	function updateTheme() {
		if (isDark) {
			document.documentElement.classList.add('dark');
		} else {
			document.documentElement.classList.remove('dark');
		}
	}

	const navLinks = [
		{ href: '#features', label: 'Features' },
		{ href: '#pricing', label: 'Pricing' },
		{ href: '#faq', label: 'FAQ' },
		{ href: '/docs', label: 'Docs' }
	];
</script>

<div class="min-h-screen flex flex-col">
	<!-- Header -->
	<header
		class="fixed top-0 left-0 right-0 z-50 transition-all duration-300"
		class:glass={scrolled}
		class:bg-transparent={!scrolled}
	>
		<nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="flex items-center justify-between h-16 lg:h-20">
				<!-- Logo -->
				<a href="/" class="flex items-center gap-2 group">
					<div class="w-9 h-9 rounded-xl bg-gradient-to-br from-[rgb(var(--color-primary-500))] to-[rgb(var(--color-accent-500))] flex items-center justify-center">
						<span class="text-white font-bold text-lg">Q</span>
					</div>
					<span class="text-xl font-bold text-[rgb(var(--color-text))] group-hover:text-gradient transition-all">
						QAudit
					</span>
				</a>

				<!-- Desktop Navigation -->
				<div class="hidden md:flex items-center gap-8">
					{#each navLinks as link}
						<a
							href={link.href}
							class="text-[rgb(var(--color-text-secondary))] hover:text-[rgb(var(--color-text))] transition-colors font-medium"
						>
							{link.label}
						</a>
					{/each}
				</div>

				<!-- Right side -->
				<div class="flex items-center gap-3">
					<!-- Theme Toggle -->
					<button
						onclick={toggleTheme}
						class="p-2 rounded-lg hover:bg-[rgb(var(--color-bg-tertiary))] transition-colors"
						aria-label="Toggle theme"
					>
						{#if isDark}
							<Sun class="w-5 h-5 text-[rgb(var(--color-text-secondary))]" />
						{:else}
							<Moon class="w-5 h-5 text-[rgb(var(--color-text-secondary))]" />
						{/if}
					</button>

					<!-- Login (desktop) -->
					<a
						href="/login"
						class="hidden md:block text-[rgb(var(--color-text-secondary))] hover:text-[rgb(var(--color-text))] transition-colors font-medium"
					>
						Log in
					</a>

					<!-- CTA Button -->
					<a
						href="#hero"
						class="hidden sm:flex items-center gap-2 px-5 py-2.5 rounded-full font-semibold text-white transition-all hover:scale-105 hover:shadow-lg"
						style="background: var(--gradient-cta);"
					>
						Start Free
					</a>

					<!-- Mobile menu button -->
					<button
						onclick={() => mobileMenuOpen = !mobileMenuOpen}
						class="md:hidden p-2 rounded-lg hover:bg-[rgb(var(--color-bg-tertiary))] transition-colors"
						aria-label="Toggle menu"
					>
						{#if mobileMenuOpen}
							<X class="w-6 h-6 text-[rgb(var(--color-text))]" />
						{:else}
							<Menu class="w-6 h-6 text-[rgb(var(--color-text))]" />
						{/if}
					</button>
				</div>
			</div>

			<!-- Mobile Navigation -->
			{#if mobileMenuOpen}
				<div class="md:hidden py-4 border-t border-[rgb(var(--color-border))]">
					<div class="flex flex-col gap-3">
						{#each navLinks as link}
							<a
								href={link.href}
								onclick={() => mobileMenuOpen = false}
								class="px-4 py-2 text-[rgb(var(--color-text-secondary))] hover:text-[rgb(var(--color-text))] hover:bg-[rgb(var(--color-bg-tertiary))] rounded-lg transition-colors font-medium"
							>
								{link.label}
							</a>
						{/each}
						<a
							href="/login"
							class="px-4 py-2 text-[rgb(var(--color-text-secondary))] hover:text-[rgb(var(--color-text))] hover:bg-[rgb(var(--color-bg-tertiary))] rounded-lg transition-colors font-medium"
						>
							Log in
						</a>
						<a
							href="#hero"
							class="mx-4 mt-2 text-center px-5 py-2.5 rounded-full font-semibold text-white"
							style="background: var(--gradient-cta);"
						>
							Start Free
						</a>
					</div>
				</div>
			{/if}
		</nav>
	</header>

	<!-- Main Content -->
	<main class="flex-1">
		{@render children()}
	</main>

	<!-- Footer -->
	<footer class="border-t border-[rgb(var(--color-border))] bg-[rgb(var(--color-bg-secondary))]">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 lg:py-16">
			<div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-8">
				<!-- Brand -->
				<div class="col-span-2 lg:col-span-1">
					<a href="/" class="flex items-center gap-2 mb-4">
						<div class="w-8 h-8 rounded-lg bg-gradient-to-br from-[rgb(var(--color-primary-500))] to-[rgb(var(--color-accent-500))] flex items-center justify-center">
							<span class="text-white font-bold">Q</span>
						</div>
						<span class="text-lg font-bold text-[rgb(var(--color-text))]">QAudit</span>
					</a>
					<p class="text-sm text-[rgb(var(--color-text-muted))] mb-4">
						AI-Powered Accessibility & Security Audits
					</p>
					<p class="text-xs text-[rgb(var(--color-text-muted))]">
						Made in Moldova
					</p>
				</div>

				<!-- Product -->
				<div>
					<h4 class="font-semibold text-[rgb(var(--color-text))] mb-4">Product</h4>
					<ul class="space-y-2">
						<li><a href="#features" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Features</a></li>
						<li><a href="#pricing" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Pricing</a></li>
						<li><a href="/api" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">API</a></li>
						<li><a href="/changelog" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Changelog</a></li>
					</ul>
				</div>

				<!-- Resources -->
				<div>
					<h4 class="font-semibold text-[rgb(var(--color-text))] mb-4">Resources</h4>
					<ul class="space-y-2">
						<li><a href="/docs" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Documentation</a></li>
						<li><a href="/blog" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Blog</a></li>
						<li><a href="/guides" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Guides</a></li>
						<li><a href="/support" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Support</a></li>
					</ul>
				</div>

				<!-- Legal -->
				<div>
					<h4 class="font-semibold text-[rgb(var(--color-text))] mb-4">Legal</h4>
					<ul class="space-y-2">
						<li><a href="/privacy" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Privacy</a></li>
						<li><a href="/terms" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Terms</a></li>
						<li><a href="/accessibility" class="text-sm text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors">Accessibility</a></li>
					</ul>
				</div>
			</div>

			<div class="mt-12 pt-8 border-t border-[rgb(var(--color-border))] flex flex-col sm:flex-row justify-between items-center gap-4">
				<p class="text-sm text-[rgb(var(--color-text-muted))]">
					© 2024 QAudit. All rights reserved.
				</p>
				<div class="flex items-center gap-4">
					<a href="https://twitter.com/qaudit" class="text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors" aria-label="Twitter">
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
					</a>
					<a href="https://github.com/qaudit" class="text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors" aria-label="GitHub">
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
					</a>
					<a href="https://linkedin.com/company/qaudit" class="text-[rgb(var(--color-text-muted))] hover:text-[rgb(var(--color-text))] transition-colors" aria-label="LinkedIn">
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
					</a>
				</div>
			</div>
		</div>
	</footer>
</div>
