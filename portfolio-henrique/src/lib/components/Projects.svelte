<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section id="projetos" class="projects-section" use:reveal>
	<div class="container">
		<div class="section-top">
			<div>
				<span class="eyebrow">02 / PROJETOS</span>
				<h2>Ideias que ganharam<br /><span>vida através do código.</span></h2>
			</div>

			<p class="section-description">
				Projetos que transformam ideias em aplicações reais, reunindo tecnologia, arquitetura e
				soluções para problemas do cotidiano.
			</p>
		</div>

		<article class="featured-project">
			<div class="project-visual">
				<div class="visual-top">
					<span>PROJETO EM DESTAQUE</span>
					<span class="visual-index">01 — 01</span>
				</div>

				<div class="visual-center">
					<div class="orbit orbit-one"></div>
					<div class="orbit orbit-two"></div>
					<div class="project-logo">
						<span>TF</span>
						<i></i>
					</div>
					<div class="visual-caption">THERAPIST FRIEND</div>
				</div>

				<div class="visual-bottom">
					<span>TECNOLOGIA</span>
					<span>IMPACTO SOCIAL</span>
					<span>INTELIGÊNCIA ARTIFICIAL</span>
				</div>
			</div>

			<div class="project-info">
				<div class="project-heading">
					<span class="project-category">PLATAFORMA WEB · FULL STACK</span>
					<span class="project-number">01</span>
				</div>

				<h3>TherapistFriend</h3>

				<p class="project-description">
					Uma plataforma web gratuita que conecta pacientes e profissionais da saúde mental.
					Desenvolvida para permitir o compartilhamento de relatos, interações privadas,
					acompanhamento de humor e realização de sessões on-line, integrando recursos de
					inteligência artificial.
				</p>

				<div class="project-highlights">
					<div>
						<span class="highlight-mark">↗</span>
						<p>Relatos anônimos e conexão entre pacientes e profissionais</p>
					</div>

					<div>
						<span class="highlight-mark">↗</span>
						<p>Análise textual e identificação de expressões faciais com IA</p>
					</div>

					<div>
						<span class="highlight-mark">↗</span>
						<p>Chat privado e sessões on-line com comunicação em tempo real</p>
					</div>
				</div>

				<div class="project-stack">
					<span>React</span>
					<span>TypeScript</span>
					<span>Node.js</span>
					<span>Express</span>
					<span>PostgreSQL</span>
					<span>Redis</span>
					<span>Python</span>
					<span>YOLOv8</span>
					<span>WebRTC</span>
					<span>Socket.IO</span>
				</div>

				<a class="project-link" href="/projetos/therapistfriend">
					Explorar projeto <span>↗</span>
				</a>
			</div>
		</article>

		<div class="projects-footer">
			<span>PROJETO EM DESTAQUE · 01</span>
			<span>OUTROS PROJETOS EM BREVE</span>
		</div>
	</div>
</section>

<style>
	.projects-section {
		padding: 130px 0;
		border-top: 1px solid var(--color-border);
	}

	.section-top {
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
		gap: 40px;
		margin-bottom: 65px;
	}

	.eyebrow {
		display: block;
		margin-bottom: 24px;
		color: var(--color-primary);
		font-size: 12px;
		font-weight: 700;
		letter-spacing: 2px;
	}

	h2 {
		font-family: var(--font-heading);
		font-size: clamp(38px, 5vw, 64px);
		line-height: 1.12;
		letter-spacing: -2.5px;
	}

	h2 span {
		color: var(--color-muted);
	}

	.section-description {
		max-width: 330px;
		color: var(--color-muted);
		font-size: 14px;
		line-height: 1.8;
	}

	.featured-project {
		display: grid;
		grid-template-columns: 1fr 1fr;
		overflow: hidden;
		border: 1px solid var(--color-border);
		border-radius: 12px;
		background: var(--color-surface);
	}

	.project-visual {
		position: relative;
		display: flex;
		min-height: 520px;
		flex-direction: column;
		justify-content: space-between;
		overflow: hidden;
		padding: 28px;
		background-color: #171e19;
		background-image:
			linear-gradient(rgba(184, 239, 107, 0.055) 1px, transparent 1px),
			linear-gradient(90deg, rgba(184, 239, 107, 0.055) 1px, transparent 1px);
		background-size: 36px 36px;
	}

	.visual-top,
	.visual-bottom {
		position: relative;
		z-index: 2;
		display: flex;
		justify-content: space-between;
		gap: 12px;
		color: #a5b59a;
		font-size: 9px;
		font-weight: 700;
		letter-spacing: 1.4px;
	}

	.visual-index {
		color: var(--color-primary);
	}

	.visual-center {
		position: relative;
		display: grid;
		flex: 1;
		place-items: center;
	}

	.orbit {
		position: absolute;
		width: 290px;
		height: 290px;
		border: 1px solid rgba(184, 239, 107, 0.25);
		border-radius: 50%;
	}

	.orbit-one {
		transform: scaleY(0.55) rotate(-30deg);
	}

	.orbit-two {
		transform: scaleY(0.55) rotate(30deg);
	}

	.project-logo {
		position: relative;
		display: grid;
		width: 130px;
		height: 130px;
		place-items: center;
		border: 1px solid rgba(184, 239, 107, 0.7);
		border-radius: 32px;
		background: rgba(184, 239, 107, 0.1);
		box-shadow: 0 0 70px rgba(184, 239, 107, 0.12);
		transform: rotate(-8deg);
	}

	.project-logo span {
		color: var(--color-primary);
		font-family: var(--font-heading);
		font-size: 48px;
		font-weight: 700;
		transform: rotate(8deg);
	}

	.project-logo i {
		position: absolute;
		top: 17px;
		right: 17px;
		width: 9px;
		height: 9px;
		border-radius: 50%;
		background: var(--color-primary);
		box-shadow: 0 0 15px var(--color-primary);
	}

	.visual-caption {
		position: absolute;
		bottom: 35px;
		color: rgba(245, 245, 245, 0.65);
		font-family: var(--font-heading);
		font-size: 11px;
		letter-spacing: 5px;
	}

	.visual-bottom {
		flex-wrap: wrap;
		color: #82927b;
		font-size: 8px;
	}

	.project-info {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		padding: 45px;
	}

	.project-heading {
		display: flex;
		width: 100%;
		justify-content: space-between;
		align-items: center;
	}

	.project-category {
		color: var(--color-primary);
		font-size: 10px;
		font-weight: 700;
		letter-spacing: 1.5px;
	}

	.project-number {
		color: var(--color-muted);
		font-family: var(--font-heading);
		font-size: 13px;
	}

	.project-info h3 {
		margin-top: 34px;
		font-family: var(--font-heading);
		font-size: clamp(30px, 4vw, 43px);
		letter-spacing: -1.5px;
	}

	.project-description {
		margin-top: 18px;
		color: var(--color-muted);
		font-size: 14px;
		line-height: 1.9;
	}

	.project-highlights {
		display: flex;
		flex-direction: column;
		gap: 16px;
		margin-top: 28px;
	}

	.project-highlights > div {
		display: flex;
		align-items: center;
		gap: 12px;
	}

	.highlight-mark {
		color: var(--color-primary);
		font-size: 17px;
	}

	.project-highlights p {
		color: #d0d1d5;
		font-size: 12px;
	}

	.project-stack {
		display: flex;
		flex-wrap: wrap;
		gap: 8px;
		margin-top: 30px;
	}

	.project-stack span {
		padding: 7px 10px;
		border: 1px solid var(--color-border);
		border-radius: 4px;
		color: var(--color-muted);
		font-size: 10px;
	}

	.project-link {
		display: inline-flex;
		align-items: center;
		gap: 22px;
		margin-top: 35px;
		padding-bottom: 8px;
		border-bottom: 1px solid var(--color-primary);
		color: var(--color-primary);
		font-size: 13px;
		font-weight: 700;
		transition: gap 0.2s ease;
	}

	.project-link:hover {
		gap: 30px;
	}

	.projects-footer {
		display: flex;
		justify-content: space-between;
		gap: 20px;
		margin-top: 22px;
		color: var(--color-muted);
		font-size: 10px;
		letter-spacing: 1.3px;
	}

	@media (max-width: 850px) {
		.featured-project {
			grid-template-columns: 1fr;
		}

		.project-visual {
			min-height: 390px;
		}

		.project-info {
			padding: 32px;
		}

		.section-top {
			align-items: flex-start;
			flex-direction: column;
		}
	}

	@media (max-width: 600px) {
		.projects-section {
			padding: 90px 0;
		}

		.project-visual {
			min-height: 330px;
			padding: 20px;
		}

		.orbit {
			width: 230px;
			height: 230px;
		}

		.project-info {
			padding: 25px 20px;
		}

		.projects-footer {
			flex-direction: column;
		}
	}
</style>
