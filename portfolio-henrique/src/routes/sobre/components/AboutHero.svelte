<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="about-hero">
	<div class="hero-container">
		<header class="about-nav">
			<a href="/" class="nav-logo">HENRIQUE<span>.</span></a>

			<a href="/" class="nav-back">
				VOLTAR AO PORTFÓLIO
				<span>↗</span>
			</a>
		</header>
		<div class="hero-topline">
			<span>UM POUCO SOBRE MIM</span>
			<span>MINHA HISTÓRIA · 2026</span>
		</div>

		<div class="hero-content">
			<div class="hero-text" use:reveal>
				<span class="hero-eyebrow">
					PRAZER, SOU HENRIQUE
					<span class="eyebrow-line"></span>
				</span>

				<h1>
					Entre ideias,
					<span>código e</span>
					<em>possibilidades.</em>
				</h1>

				<p class="hero-description">
					Sou Henrique Ribeiro, bacharel em Ciência da Computação. Uma pessoa movida pela
					curiosidade, pelo aprendizado constante e pela vontade de transformar ideias em algo
					significativo.
				</p>

				<div class="hero-details">
					<span>CIÊNCIA DA COMPUTAÇÃO</span>
					<span class="detail-dot"></span>
					<span>TECNOLOGIA & CRIATIVIDADE</span>
				</div>

				<a href="#minha-historia" class="hero-scroll">
					<span class="scroll-icon">↓</span>
					CONHEÇA MINHA HISTÓRIA
				</a>
			</div>

			<div class="hero-image-area" use:reveal>
				<div class="image-frame">
					<img src="/images/sobre/perfil.jpg" alt="Henrique Ribeiro" class="hero-image" />
				</div>

				<div class="image-caption">
					<span>PERFIL PESSOAL</span>
					<span>UM OLHAR SOBRE MIM</span>
				</div>

				<div class="decorative-circle"></div>
				<div class="decorative-note">
					<span>+</span>
					APRENDER · EXPLORAR · CONSTRUIR
				</div>
			</div>
		</div>

		<div class="hero-footer">
			<span>HENRIQUE RIBEIRO</span>
			<span>UMA HISTÓRIA EM CONSTRUÇÃO</span>
		</div>
	</div>
</section>

<style>
	.about-hero {
		position: relative;
		overflow: hidden;
		padding: 34px 0 28px;
		background: #eae6dd;
		color: #292820;
	}

	.hero-container {
		width: min(1180px, calc(100% - 64px));
		margin-inline: auto;
	}

	.about-nav {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0 0 28px;
	}

	.nav-logo {
		color: #292820;
		font-family: var(--font-heading);
		font-size: 17px;
		font-weight: 700;
		letter-spacing: -0.7px;
	}

	.nav-logo span {
		color: #8b9875;
	}

	.nav-back {
		display: flex;
		align-items: center;
		gap: 9px;
		color: #77705f;
		font-size: 9px;
		font-weight: 700;
		letter-spacing: 1.3px;
		transition: color 0.25s ease;
	}

	.nav-back span {
		color: #8b9875;
		font-size: 15px;
	}

	.nav-back:hover {
		color: #292820;
	}

	.nav-logo:focus-visible,
	.nav-back:focus-visible {
		outline: 2px solid #8b9875;
		outline-offset: 5px;
	}

	.hero-topline,
	.hero-footer {
		display: flex;
		justify-content: space-between;
		gap: 20px;
		color: #77705f;
		font-size: 10px;
		font-weight: 600;
		letter-spacing: 2px;
	}

	.hero-topline {
		padding-bottom: 22px;
		border-bottom: 1px solid #c8bca6;
	}

	.hero-content {
		display: grid;
		grid-template-columns: 1.1fr 0.9fr;
		align-items: center;
		gap: 70px;
		padding: 76px 0 85px;
	}

	.hero-eyebrow {
		display: flex;
		align-items: center;
		gap: 13px;
		color: #77705f;
		font-size: 10px;
		font-weight: 700;
		letter-spacing: 2px;
	}

	.eyebrow-line {
		width: 36px;
		height: 1px;
		background: #8b9875;
	}

	.hero-text h1 {
		margin-top: 27px;
		font-family: var(--font-heading);
		font-size: clamp(48px, 6vw, 78px);
		font-weight: 500;
		line-height: 1.04;
		letter-spacing: -4px;
	}

	.hero-text h1 span,
	.hero-text h1 em {
		display: block;
	}

	.hero-text h1 em {
		color: #8b9875;
		font-family: Georgia, serif;
		font-weight: 400;
	}

	.hero-description {
		max-width: 460px;
		margin-top: 28px;
		color: #77705f;
		font-size: 15px;
		line-height: 1.9;
	}

	.hero-details {
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		gap: 12px;
		margin-top: 30px;
		color: #77705f;
		font-size: 9px;
		font-weight: 700;
		letter-spacing: 1px;
	}

	.detail-dot {
		width: 4px;
		height: 4px;
		border-radius: 50%;
		background: #8b9875;
	}

	.hero-scroll {
		display: inline-flex;
		align-items: center;
		gap: 12px;
		margin-top: 48px;
		color: #292820;
		font-size: 10px;
		font-weight: 700;
		letter-spacing: 1.5px;
		transition: color 0.25s ease;
	}

	.hero-scroll:hover {
		color: #8b9875;
	}

	.scroll-icon {
		display: grid;
		width: 34px;
		height: 34px;
		place-items: center;
		border: 1px solid #c8bca6;
		border-radius: 50%;
		font-size: 16px;
		transition: transform 0.25s ease;
	}

	.hero-scroll:hover .scroll-icon {
		transform: translateY(3px);
	}

	.hero-image-area {
		position: relative;
		padding: 0 20px 35px 0;
	}

	.image-frame {
		position: relative;
		z-index: 1;
		overflow: hidden;
		width: 100%;
		aspect-ratio: 0.82;
		background: #d4cbbb;
	}

	.hero-image {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center 35%;
		transition: transform 0.6s ease;
	}

	.image-frame:hover .hero-image {
		transform: scale(1.035);
	}

	/* .placeholder-symbol {
		color: #8b9875;
		font-family: var(--font-heading);
		font-size: 100px;
		font-weight: 500;
		letter-spacing: -10px;
	}

	.image-placeholder > span {
		font-size: 9px;
		font-weight: 700;
		letter-spacing: 2px;
	} */

	.image-caption {
		display: flex;
		justify-content: space-between;
		margin-top: 15px;
		color: #77705f;
		font-size: 9px;
		font-weight: 600;
		letter-spacing: 1.5px;
	}

	.decorative-circle {
		position: absolute;
		top: -35px;
		right: -25px;
		width: 130px;
		height: 130px;
		border: 1px solid #8b987570;
		border-radius: 50%;
	}

	.decorative-note {
		position: absolute;
		z-index: 2;
		right: -35px;
		bottom: 75px;
		display: flex;
		align-items: center;
		gap: 9px;
		padding: 14px 17px;
		background: #f5f2eb;
		color: #77705f;
		font-size: 8px;
		font-weight: 700;
		letter-spacing: 1px;
		box-shadow: 0 8px 25px #29282012;
	}

	.decorative-note span {
		color: #8b9875;
		font-size: 18px;
	}

	.hero-footer {
		padding-top: 20px;
		border-top: 1px solid #c8bca6;
	}

	@media (max-width: 850px) {
		.hero-content {
			grid-template-columns: 1fr 0.8fr;
			gap: 35px;
		}

		.hero-text h1 {
			font-size: clamp(43px, 6vw, 62px);
			letter-spacing: -3px;
		}

		.decorative-note {
			right: -15px;
		}
	}

	@media (max-width: 650px) {
		.about-hero {
			padding-top: 25px;
		}

		.hero-container {
			width: calc(100% - 40px);
		}

		.about-nav {
			padding-bottom: 23px;
		}

		.nav-logo {
			font-size: 15px;
		}

		.nav-back {
			font-size: 8px;
			letter-spacing: 0.8px;
		}

		.hero-topline,
		.hero-footer {
			font-size: 8px;
			letter-spacing: 1px;
		}

		.hero-topline span:last-child {
			text-align: right;
		}

		.hero-content {
			grid-template-columns: 1fr;
			gap: 45px;
			padding: 65px 0 55px;
		}

		.hero-text h1 {
			font-size: clamp(47px, 12vw, 65px);
		}

		.hero-description {
			font-size: 14px;
		}

		.hero-scroll {
			margin-top: 32px;
		}

		.hero-image-area {
			width: 85%;
			margin-left: auto;
			padding-right: 10px;
		}

		.hero-image {
			object-position: center 30%;
		}

		.decorative-circle {
			right: -15px;
			width: 95px;
			height: 95px;
		}

		.decorative-note {
			right: -15px;
			bottom: 65px;
			font-size: 7px;
		}

		.hero-footer {
			flex-direction: column;
			gap: 10px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.hero-scroll,
		.scroll-icon,
		.nav-back {
			transition: none;
		}

		.hero-scroll:hover .scroll-icon {
			transform: none;
		}

		.hero-image {
			transition: none;
		}

		.image-frame:hover .hero-image {
			transform: none;
		}
	}
</style>
