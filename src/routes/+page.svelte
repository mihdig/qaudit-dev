<script lang="ts">
	import { Shield, Zap, Eye, FileText, Palette, Bot, Check, ArrowRight, Play, ChevronDown } from 'lucide-svelte';

	let url = $state('');
	let isScanning = $state(false);

	function handleScan() {
		if (!url) return;
		isScanning = true;
		// TODO: Implement actual scan
		setTimeout(() => {
			isScanning = false;
			// Navigate to results
		}, 2000);
	}

	const features = [
		{
			icon: Shield,
			title: 'WCAG 2.2 AA',
			description: '70+ accessibility rules covering all WCAG criteria. EAA 2025 compliant.',
			color: 'var(--color-primary-500)'
		},
		{
			icon: Eye,
			title: 'Security Audit',
			description: 'OWASP Top 10 checks. CSRF, XSS, mixed content detection.',
			color: 'var(--color-accent-500)'
		},
		{
			icon: Zap,
			title: 'Lightning Fast',
			description: 'Full scan in under 1 second. No waiting, instant results.',
			color: 'var(--color-warning)'
		},
		{
			icon: Palette,
			title: 'Tiered Contrast',
			description: 'Unique dual-screenshot method. Catches gradients others miss.',
			color: 'var(--color-pink-500)'
		},
		{
			icon: Bot,
			title: 'Vision AI',
			description: 'Auto-generate alt text. AI-powered fix suggestions.',
			color: 'var(--color-cyan-500)'
		},
		{
			icon: FileText,
			title: '5 Report Formats',
			description: 'Executive, Developer, QA reports. JSON, HTML, Markdown.',
			color: 'var(--color-info)'
		}
	];

	const pricingPlans = [
		{
			name: 'Free',
			price: '$0',
			period: 'forever',
			description: 'Perfect for trying out QAudit',
			features: [
				'5 scans per month',
				'Basic report',
				'1 domain',
				'Email support'
			],
			cta: 'Start Free',
			popular: false
		},
		{
			name: 'Starter',
			price: '$49',
			period: '/month',
			description: 'For small teams and projects',
			features: [
				'100 scans per month',
				'Full reports (all formats)',
				'3 domains',
				'API access',
				'Priority support'
			],
			cta: 'Start Trial',
			popular: false
		},
		{
			name: 'Pro',
			price: '$149',
			period: '/month',
			description: 'For growing businesses',
			features: [
				'500 scans per month',
				'Vision AI features',
				'10 domains',
				'Scheduled monitoring',
				'Slack/Jira integration',
				'Dedicated support'
			],
			cta: 'Start Trial',
			popular: true
		},
		{
			name: 'Business',
			price: '$399',
			period: '/month',
			description: 'For agencies and enterprises',
			features: [
				'2000 scans per month',
				'White-label reports',
				'Unlimited domains',
				'Custom integrations',
				'SLA guarantee',
				'Account manager'
			],
			cta: 'Contact Sales',
			popular: false
		}
	];

	const faqs = [
		{
			question: 'What is EAA 2025?',
			answer: 'The European Accessibility Act (EAA) came into force on June 28, 2025. It requires businesses serving EU customers to make their websites and apps accessible. Non-compliance can result in fines up to €100,000.'
		},
		{
			question: 'How accurate is the scanner?',
			answer: 'QAudit uses 70+ W3C ACT-validated rules with a false positive rate under 5%. Our unique Tiered Contrast Scanner catches issues that other tools miss, especially on gradient backgrounds.'
		},
		{
			question: 'Can I integrate with my CI/CD pipeline?',
			answer: 'Yes! QAudit provides a REST API, GitHub Action, and CLI tool for seamless integration into your development workflow. Fail builds automatically when accessibility issues are detected.'
		},
		{
			question: 'Do you support mobile app testing?',
			answer: 'Mobile app accessibility testing is coming in Q1 2025. Currently, QAudit focuses on web accessibility but can test mobile-responsive websites across different viewport sizes.'
		},
		{
			question: 'How is QAudit different from axe or WAVE?',
			answer: 'QAudit combines accessibility and security scanning in one platform. Our Tiered Contrast Scanner uses a unique dual-screenshot method to detect contrast issues on complex backgrounds. Plus, Vision AI provides intelligent fix suggestions.'
		}
	];

	let openFaq = $state<number | null>(null);
</script>

<svelte:head>
	<title>QAudit - AI-Powered Accessibility & Security Audits</title>
</svelte:head>

<!-- Hero Section -->
<section id="hero" class="relative min-h-screen flex items-center justify-center pt-20 overflow-hidden">
	<!-- Background gradient -->
	<div class="absolute inset-0 hero-gradient-overlay"></div>
	<div class="absolute top-0 left-1/2 -translate-x-1/2 w-[800px] h-[600px] hero-glow blur-3xl rounded-full opacity-50"></div>

	<div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-32">
		<div class="text-center max-w-4xl mx-auto">
			<!-- Badge -->
			<div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-[rgb(var(--color-surface-elevated))] border border-[rgb(var(--color-border))] mb-8 animate-fade-in">
				<span class="w-2 h-2 rounded-full bg-[rgb(var(--color-primary-500))] animate-pulse"></span>
				<span class="text-sm font-medium text-[rgb(var(--color-text-secondary))]">EAA 2025 Compliant Scanner</span>
			</div>

			<!-- Headline -->
			<h1 class="mb-6 animate-slide-up">
				<span class="text-[rgb(var(--color-text))]">AI-Powered </span>
				<span class="text-gradient">Accessibility</span>
				<br />
				<span class="text-[rgb(var(--color-text))]">& Security Audits</span>
			</h1>

			<!-- Subheadline -->
			<p class="text-xl lg:text-2xl text-[rgb(var(--color-text-secondary))] mb-10 max-w-2xl mx-auto animate-slide-up delay-100">
				Comply with EAA 2025 and WCAG 2.2 in minutes.
				<br class="hidden sm:block" />
				Scan any website. Get actionable fixes.
			</p>

			<!-- URL Input -->
			<div class="max-w-2xl mx-auto mb-8 animate-slide-up delay-200">
				<div class="flex flex-col sm:flex-row gap-3 p-2 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))] shadow-xl">
					<input
						type="url"
						bind:value={url}
						placeholder="Enter your website URL..."
						class="flex-1 px-5 py-4 bg-transparent text-[rgb(var(--color-text))] placeholder:text-[rgb(var(--color-text-muted))] focus:outline-none text-lg"
					/>
					<button
						onclick={handleScan}
						disabled={isScanning || !url}
						class="px-8 py-4 rounded-xl font-semibold text-white transition-all hover:scale-105 hover:shadow-lg disabled:opacity-50 disabled:cursor-not-allowed disabled:hover:scale-100 flex items-center justify-center gap-2"
						style="background: var(--gradient-cta);"
					>
						{#if isScanning}
							<div class="w-5 h-5 border-2 border-white/30 border-t-white rounded-full animate-spin"></div>
							Scanning...
						{:else}
							<Play class="w-5 h-5" />
							Scan Free
						{/if}
					</button>
				</div>
			</div>

			<!-- Trust badges -->
			<div class="flex flex-wrap justify-center gap-6 text-sm text-[rgb(var(--color-text-muted))] animate-slide-up delay-300">
				<div class="flex items-center gap-2">
					<Check class="w-4 h-4 text-[rgb(var(--color-primary-500))]" />
					No credit card required
				</div>
				<div class="flex items-center gap-2">
					<Check class="w-4 h-4 text-[rgb(var(--color-primary-500))]" />
					5 free scans
				</div>
				<div class="flex items-center gap-2">
					<Check class="w-4 h-4 text-[rgb(var(--color-primary-500))]" />
					Instant results
				</div>
			</div>
		</div>

		<!-- Demo Preview -->
		<div class="mt-16 lg:mt-24 max-w-5xl mx-auto animate-scale-in delay-400">
			<div class="relative rounded-2xl overflow-hidden border border-[rgb(var(--color-border))] shadow-2xl bg-[rgb(var(--color-surface))]">
				<!-- Browser chrome -->
				<div class="flex items-center gap-2 px-4 py-3 bg-[rgb(var(--color-bg-tertiary))] border-b border-[rgb(var(--color-border))]">
					<div class="flex gap-2">
						<div class="w-3 h-3 rounded-full bg-[rgb(var(--color-error))]"></div>
						<div class="w-3 h-3 rounded-full bg-[rgb(var(--color-warning))]"></div>
						<div class="w-3 h-3 rounded-full bg-[rgb(var(--color-success))]"></div>
					</div>
					<div class="flex-1 mx-4">
						<div class="px-4 py-1.5 rounded-lg bg-[rgb(var(--color-bg-secondary))] text-sm text-[rgb(var(--color-text-muted))] text-center">
							qaudit.dev/scan/example.com
						</div>
					</div>
				</div>
				<!-- Content placeholder -->
				<div class="p-8 lg:p-12">
					<div class="grid lg:grid-cols-3 gap-8">
						<!-- Score -->
						<div class="text-center">
							<div class="relative w-32 h-32 mx-auto mb-4">
								<svg class="w-full h-full -rotate-90" viewBox="0 0 100 100">
									<circle
										cx="50" cy="50" r="45"
										fill="none"
										stroke="rgb(var(--color-border))"
										stroke-width="8"
									/>
									<circle
										cx="50" cy="50" r="45"
										fill="none"
										stroke="rgb(var(--color-primary-500))"
										stroke-width="8"
										stroke-linecap="round"
										stroke-dasharray="283"
										stroke-dashoffset="28"
										class="transition-all duration-1000"
									/>
								</svg>
								<div class="absolute inset-0 flex items-center justify-center">
									<span class="text-4xl font-bold text-[rgb(var(--color-text))]">94</span>
								</div>
							</div>
							<p class="text-lg font-semibold text-[rgb(var(--color-primary-500))]">Excellent</p>
							<p class="text-sm text-[rgb(var(--color-text-muted))]">Accessibility Score</p>
						</div>
						<!-- Stats -->
						<div class="lg:col-span-2 grid grid-cols-2 gap-4">
							<div class="p-4 rounded-xl bg-[rgb(var(--color-bg-tertiary))]">
								<p class="text-3xl font-bold text-[rgb(var(--color-text))]">2</p>
								<p class="text-sm text-[rgb(var(--color-text-muted))]">Violations</p>
							</div>
							<div class="p-4 rounded-xl bg-[rgb(var(--color-bg-tertiary))]">
								<p class="text-3xl font-bold text-[rgb(var(--color-text))]">47</p>
								<p class="text-sm text-[rgb(var(--color-text-muted))]">Elements Checked</p>
							</div>
							<div class="p-4 rounded-xl bg-[rgb(var(--color-bg-tertiary))]">
								<p class="text-3xl font-bold text-[rgb(var(--color-text))]">0.8s</p>
								<p class="text-sm text-[rgb(var(--color-text-muted))]">Scan Time</p>
							</div>
							<div class="p-4 rounded-xl bg-[rgb(var(--color-bg-tertiary))]">
								<p class="text-3xl font-bold text-[rgb(var(--color-primary-500))]">Pass</p>
								<p class="text-sm text-[rgb(var(--color-text-muted))]">EAA Status</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Problem Section -->
<section class="py-20 lg:py-32 bg-[rgb(var(--color-bg-secondary))]">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<p class="text-sm font-semibold text-[rgb(var(--color-error))] uppercase tracking-wide mb-4">The Problem</p>
			<h2 class="text-[rgb(var(--color-text))] mb-4">
				EAA 2025 is here.<br />Non-compliance costs up to <span class="text-[rgb(var(--color-error))]">€100,000</span>
			</h2>
		</div>

		<div class="grid md:grid-cols-3 gap-8">
			<div class="p-8 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))]">
				<div class="text-4xl mb-4">💸</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-2">Manual Audits Cost $5K-50K</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">Traditional accessibility consultants charge thousands for a single audit. Most businesses can't afford regular testing.</p>
			</div>
			<div class="p-8 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))]">
				<div class="text-4xl mb-4">⚖️</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-2">Legal Risks Increasing Daily</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">EAA enforcement began June 2025. Companies face fines, lawsuits, and reputational damage from non-compliance.</p>
			</div>
			<div class="p-8 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))]">
				<div class="text-4xl mb-4">🚫</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-2">15% of Users Excluded</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">Over 1 billion people worldwide have disabilities. Inaccessible websites lose customers and market share.</p>
			</div>
		</div>
	</div>
</section>

<!-- Features Section -->
<section id="features" class="py-20 lg:py-32">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<p class="text-sm font-semibold text-[rgb(var(--color-primary-500))] uppercase tracking-wide mb-4">Features</p>
			<h2 class="text-[rgb(var(--color-text))] mb-4">One platform. Complete compliance.</h2>
			<p class="text-xl text-[rgb(var(--color-text-secondary))] max-w-2xl mx-auto">
				Everything you need to ensure your website is accessible and secure.
			</p>
		</div>

		<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each features as feature, i}
				<div class="group p-8 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))] hover:border-[rgb(var(--color-border-hover))] transition-all hover:shadow-xl hover:-translate-y-1">
					<div
						class="w-12 h-12 rounded-xl flex items-center justify-center mb-6"
						style="background: rgb({feature.color} / 0.15);"
					>
						<svelte:component this={feature.icon} class="w-6 h-6" style="color: rgb({feature.color});" />
					</div>
					<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-3">{feature.title}</h3>
					<p class="text-[rgb(var(--color-text-secondary))]">{feature.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- How it Works -->
<section class="py-20 lg:py-32 bg-[rgb(var(--color-bg-secondary))]">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<p class="text-sm font-semibold text-[rgb(var(--color-accent-500))] uppercase tracking-wide mb-4">How it Works</p>
			<h2 class="text-[rgb(var(--color-text))]">Three steps to compliance</h2>
		</div>

		<div class="grid md:grid-cols-3 gap-8 lg:gap-12">
			<div class="text-center">
				<div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-[rgb(var(--color-accent-500))] to-[rgb(var(--color-pink-500))] flex items-center justify-center text-white text-2xl font-bold mx-auto mb-6">1</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-3">Enter Your URL</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">Paste any website URL into the scanner. No installation or setup required.</p>
			</div>
			<div class="text-center">
				<div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-[rgb(var(--color-pink-500))] to-[rgb(var(--color-primary-500))] flex items-center justify-center text-white text-2xl font-bold mx-auto mb-6">2</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-3">AI Scans in Seconds</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">Our engine runs 70+ checks including contrast, focus, ARIA, and security in under 1 second.</p>
			</div>
			<div class="text-center">
				<div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-[rgb(var(--color-primary-500))] to-[rgb(var(--color-cyan-500))] flex items-center justify-center text-white text-2xl font-bold mx-auto mb-6">3</div>
				<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-3">Get Actionable Report</h3>
				<p class="text-[rgb(var(--color-text-secondary))]">Download detailed reports with exact issues, code fixes, and compliance status.</p>
			</div>
		</div>
	</div>
</section>

<!-- Pricing Section -->
<section id="pricing" class="py-20 lg:py-32">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<p class="text-sm font-semibold text-[rgb(var(--color-primary-500))] uppercase tracking-wide mb-4">Pricing</p>
			<h2 class="text-[rgb(var(--color-text))] mb-4">Simple, transparent pricing</h2>
			<p class="text-xl text-[rgb(var(--color-text-secondary))]">Start free. Upgrade when you need more.</p>
		</div>

		<div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
			{#each pricingPlans as plan}
				<div class="relative p-8 rounded-2xl border transition-all hover:shadow-xl {plan.popular ? 'pricing-popular' : 'pricing-default'}">
					{#if plan.popular}
						<div class="absolute -top-3 left-1/2 -translate-x-1/2 px-3 py-1 rounded-full text-xs font-semibold text-white" style="background: var(--gradient-cta);">
							Most Popular
						</div>
					{/if}

					<h3 class="text-xl font-semibold text-[rgb(var(--color-text))] mb-2">{plan.name}</h3>
					<div class="mb-4">
						<span class="text-4xl font-bold text-[rgb(var(--color-text))]">{plan.price}</span>
						<span class="text-[rgb(var(--color-text-muted))]">{plan.period}</span>
					</div>
					<p class="text-sm text-[rgb(var(--color-text-secondary))] mb-6">{plan.description}</p>

					<ul class="space-y-3 mb-8">
						{#each plan.features as feature}
							<li class="flex items-start gap-3">
								<Check class="w-5 h-5 text-[rgb(var(--color-primary-500))] flex-shrink-0 mt-0.5" />
								<span class="text-sm text-[rgb(var(--color-text-secondary))]">{feature}</span>
							</li>
						{/each}
					</ul>

					<button
						class="w-full py-3 rounded-xl font-semibold transition-all hover:scale-105"
						class:text-white={plan.popular}
						class:text-[rgb(var(--color-text))]={!plan.popular}
						class:bg-[rgb(var(--color-bg-tertiary))]={!plan.popular}
						class:hover:bg-[rgb(var(--color-border))]={!plan.popular}
						style={plan.popular ? 'background: var(--gradient-cta);' : ''}
					>
						{plan.cta}
					</button>
				</div>
			{/each}
		</div>

		<p class="text-center text-sm text-[rgb(var(--color-text-muted))] mt-8">
			All paid plans include 14-day free trial. No credit card required.
		</p>
	</div>
</section>

<!-- FAQ Section -->
<section id="faq" class="py-20 lg:py-32 bg-[rgb(var(--color-bg-secondary))]">
	<div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<p class="text-sm font-semibold text-[rgb(var(--color-accent-500))] uppercase tracking-wide mb-4">FAQ</p>
			<h2 class="text-[rgb(var(--color-text))]">Frequently asked questions</h2>
		</div>

		<div class="space-y-4">
			{#each faqs as faq, i}
				<div class="rounded-xl border border-[rgb(var(--color-border))] bg-[rgb(var(--color-surface))] overflow-hidden">
					<button
						onclick={() => openFaq = openFaq === i ? null : i}
						class="w-full px-6 py-5 flex items-center justify-between text-left"
					>
						<span class="font-semibold text-[rgb(var(--color-text))]">{faq.question}</span>
						<span class="transition-transform {openFaq === i ? 'rotate-180' : ''}">
							<ChevronDown class="w-5 h-5 text-[rgb(var(--color-text-muted))]" />
						</span>
					</button>
					{#if openFaq === i}
						<div class="px-6 pb-5">
							<p class="text-[rgb(var(--color-text-secondary))]">{faq.answer}</p>
						</div>
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 lg:py-32 relative overflow-hidden">
	<!-- Background -->
	<div class="absolute inset-0 cta-gradient-bg"></div>

	<div class="relative max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
		<h2 class="text-[rgb(var(--color-text))] mb-6">Ready to ensure accessibility compliance?</h2>
		<p class="text-xl text-[rgb(var(--color-text-secondary))] mb-10">
			Start scanning your website today. No credit card required.
		</p>

		<div class="max-w-xl mx-auto">
			<div class="flex flex-col sm:flex-row gap-3 p-2 rounded-2xl bg-[rgb(var(--color-surface))] border border-[rgb(var(--color-border))] shadow-xl">
				<input
					type="url"
					bind:value={url}
					placeholder="Enter your website URL..."
					class="flex-1 px-5 py-4 bg-transparent text-[rgb(var(--color-text))] placeholder:text-[rgb(var(--color-text-muted))] focus:outline-none text-lg"
				/>
				<button
					class="px-8 py-4 rounded-xl font-semibold text-white transition-all hover:scale-105 hover:shadow-lg flex items-center justify-center gap-2"
					style="background: var(--gradient-cta);"
				>
					Scan Free Now
					<ArrowRight class="w-5 h-5" />
				</button>
			</div>
		</div>
	</div>
</section>
