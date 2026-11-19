

<script lang="ts">
	const technologies = ['TypeScript', 'React', 'Node.js', 'Python', 'PostgreSQL'];
    
    import { reveal } from '#lib/actions/reveal.ts';

</script>

<section id="inicio" class="hero" use:reveal>
	<div class="container hero-content">
		<div class="hero-text">
			<div class="availability">
				<span class="status-dot"></span>
				DESENVOLVIMENTO DE SOFTWARE
			</div>

			<h1>
				Transformando<br />
				ideias em <span>soluções</span><br />
				digitais.
			</h1>

			<p class="description">
				Olá, sou Henrique. Desenvolvedor interessado em tecnologia, arquitetura de software e
				criação de soluções que geram impacto.
			</p>

			<div class="hero-actions">
				<a href="#projetos" class="primary-button">
					Explorar projetos <span>↗</span>
				</a>

				<a href="#sobre" class="secondary-button"> Conheça minha trajetória </a>
			</div>

			<div class="technologies">
				<span class="tech-label">TECNOLOGIAS</span>

				<div class="tech-list">
					{#each technologies as technology}
						<span>{technology}</span>
					{/each}
				</div>
			</div>
		</div>

		<div class="hero-visual" aria-hidden="true">
			<div class="visual-grid"></div>

			<div class="orbit orbit-one"></div>
			<div class="orbit orbit-two"></div>

			<div class="main-object">
				<div class="object-face face-front"></div>
				<div class="object-face face-top"></div>
				<div class="object-face face-side"></div>
			</div>

			<div class="floating-card card-top">
				<span class="card-icon">⌘</span>
				<div>
					<strong>Pensamento criativo</strong>
					<small>Ideias em prática</small>
				</div>
			</div>

			<div class="floating-card card-bottom">
				<span class="card-indicator"></span>
				<div>
					<strong>Construindo soluções</strong>
					<small>Uma linha por vez.</small>
				</div>
			</div>

			<span class="visual-label">FIG. 001 — DIGITAL SPACE</span>
		</div>
	</div>

	<div class="container hero-footer">
		<span>PORTFÓLIO PESSOAL</span>
		<span>ROLE PARA EXPLORAR ↓</span>
	</div>
</section>

<style>
	.hero {
		position: relative;
		overflow: hidden;
		padding-top: 100px;
		background-image:
			linear-gradient(rgba(255, 255, 255, 0.025) 1px, transparent 1px),
			linear-gradient(90deg, rgba(255, 255, 255, 0.025) 1px, transparent 1px);
		background-size: 48px 48px;
		background-position: center;
	}

	.hero-content {
		min-height: 510px;
		display: grid;
		grid-template-columns: 1fr 0.9fr;
		align-items: center;
		gap: 50px;
	}

	.hero-text {
		position: relative;
		z-index: 2;
	}

	.availability {
		display: flex;
		align-items: center;
		gap: 10px;
		color: var(--color-muted);
		font-size: 11px;
		font-weight: 600;
		letter-spacing: 1.5px;
		margin-bottom: 28px;
	}

	.status-dot,
	.card-indicator {
		width: 8px;
		height: 8px;
		border-radius: 50%;
		background: var(--color-primary);
		box-shadow: 0 0 12px rgba(184, 239, 107, 0.5);
	}

	h1 {
		font-family: var(--font-heading);
		font-size: clamp(42px, 5vw, 67px);
		line-height: 1.08;
		letter-spacing: -3px;
		font-weight: 600;
	}

	h1 span {
		color: var(--color-primary);
	}

	.description {
		max-width: 480px;
		margin-top: 26px;
		color: var(--color-muted);
		font-size: 16px;
		line-height: 1.8;
	}

	.hero-actions {
		display: flex;
		align-items: center;
		flex-wrap: wrap;
		gap: 20px;
		margin-top: 32px;
	}

	.primary-button {
		background: var(--color-primary);
		color: #101114;
		padding: 15px 20px;
		border-radius: 5px;
		font-size: 14px;
		font-weight: 700;
		transition:
			transform 0.2s,
			box-shadow 0.2s;
	}

	.primary-button:hover {
		transform: translateY(-3px);
		box-shadow: 0 8px 25px rgba(184, 239, 107, 0.2);
	}

	.primary-button span {
		margin-left: 12px;
	}

	.secondary-button {
		color: var(--color-text);
		font-size: 13px;
	}

	.secondary-button:hover {
		color: var(--color-primary);
	}

	.technologies {
		margin-top: 65px;
	}

	.tech-label {
		display: block;
		color: var(--color-muted);
		font-size: 10px;
		letter-spacing: 1.5px;
		margin-bottom: 14px;
	}

	.tech-list {
		display: flex;
		flex-wrap: wrap;
		gap: 9px;
	}

	.tech-list span {
		border: 1px solid var(--color-border);
		border-radius: 4px;
		padding: 7px 10px;
		color: #c6c8ce;
		font-size: 11px;
	}

	/* Composição gráfica */

	.hero-visual {
		position: relative;
		height: 440px;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.visual-grid {
		position: absolute;
		inset: 10%;
		background-image:
			linear-gradient(rgba(184, 239, 107, 0.08) 1px, transparent 1px),
			linear-gradient(90deg, rgba(184, 239, 107, 0.08) 1px, transparent 1px);
		background-size: 28px 28px;
		mask-image: radial-gradient(circle, black, transparent 75%);
	}

	.main-object {
		position: relative;
		width: 175px;
		height: 175px;
		transform: rotate(-30deg) skew(8deg, 8deg);
		animation: float 5s ease-in-out infinite;
		filter: drop-shadow(0 20px 35px rgba(184, 239, 107, 0.15));
	}

	.object-face {
		position: absolute;
		inset: 0;
		border: 1px solid rgba(184, 239, 107, 0.6);
	}

	.face-front {
		background: linear-gradient(135deg, #b8ef6b, #668c35);
		transform: translateZ(60px);
		box-shadow: inset -25px -25px 50px rgba(0, 0, 0, 0.25);
	}

	.face-top {
		background: #d6ffa0;
		transform: rotateX(55deg) translateY(-49px) translateZ(25px);
		opacity: 0.9;
	}

	.face-side {
		background: #547d2b;
		transform: rotateY(55deg) translateX(49px) translateZ(25px);
		opacity: 0.9;
	}

	.orbit {
		position: absolute;
		width: 350px;
		height: 120px;
		border: 1px solid rgba(184, 239, 107, 0.35);
		border-radius: 50%;
	}

	.orbit-one {
		transform: rotate(-35deg);
	}

	.orbit-two {
		transform: rotate(45deg);
		width: 300px;
		height: 180px;
		border-color: rgba(255, 255, 255, 0.13);
	}

	.floating-card {
		position: absolute;
		z-index: 2;
		display: flex;
		align-items: center;
		gap: 12px;
		padding: 14px;
		background: rgba(25, 27, 32, 0.92);
		border: 1px solid var(--color-border);
		border-radius: 7px;
		backdrop-filter: blur(12px);
		box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
	}

	.floating-card strong,
	.floating-card small {
		display: block;
	}

	.floating-card strong {
		font-size: 11px;
	}

	.floating-card small {
		color: var(--color-muted);
		font-size: 10px;
		margin-top: 4px;
	}

	.card-icon {
		color: var(--color-primary);
		font-size: 25px;
	}

	.card-top {
		top: 65px;
		right: 0;
	}

	.card-bottom {
		bottom: 65px;
		left: 0;
	}

	.visual-label {
		position: absolute;
		bottom: 5px;
		right: 0;
		color: var(--color-muted);
		font-size: 9px;
		letter-spacing: 1.5px;
	}

	.hero-footer {
		display: flex;
		justify-content: space-between;
		padding-block: 35px;
		margin-top: 45px;
		border-top: 1px solid var(--color-border);
		color: var(--color-muted);
		font-size: 10px;
		letter-spacing: 1.3px;
	}

	@keyframes float {
		0%,
		100% {
			transform: translateY(0) rotate(-30deg) skew(8deg, 8deg);
		}
		50% {
			transform: translateY(-15px) rotate(-25deg) skew(8deg, 8deg);
		}
	}

	@media (max-width: 850px) {
		.hero {
			padding-top: 70px;
		}

		.hero-content {
			grid-template-columns: 1fr;
			gap: 30px;
		}

		.hero-visual {
			height: 370px;
		}

		.technologies {
			margin-top: 40px;
		}
	}

	@media (max-width: 500px) {
		.hero {
			padding-top: 55px;
		}

		h1 {
			font-size: 43px;
			letter-spacing: -2px;
		}

		.description {
			font-size: 14px;
		}

		.hero-actions {
			align-items: flex-start;
			flex-direction: column;
		}

		.hero-visual {
			height: 310px;
		}

		.main-object {
			width: 125px;
			height: 125px;
		}

		.orbit {
			width: 270px;
		}

		.card-top {
			top: 25px;
		}

		.card-bottom {
			bottom: 30px;
		}

		.hero-footer {
			font-size: 8px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.main-object {
			animation: none;
		}

		.primary-button {
			transition: none;
		}
	}

	.card-top {
		top: 65px;
		right: 0;
		animation: cardFloat 6s ease-in-out infinite;
	}

	.card-bottom {
		bottom: 65px;
		left: 0;
		animation: cardFloat 6s ease-in-out infinite;
		animation-delay: -3s;
	}

	@keyframes cardFloat {
		0%,
		100% {
			transform: translateY(0);
		}

		50% {
			transform: translateY(-7px);
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.card-top,
		.card-bottom {
			animation: none;
		}
	}
</style>
