<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="content-section features-section" id="funcionalidades" use:reveal>
	<div class="section-header">
		<div>
			<span class="section-label">03 — FUNCIONALIDADES</span>
			<h2>
				Recursos pensados para
				<span>cada etapa da experiência.</span>
			</h2>
		</div>

		<p class="section-description">
			Diferentes funcionalidades trabalham em conjunto para conectar pacientes e profissionais,
			desde o primeiro relato até o acompanhamento em sessões online.
		</p>
	</div>

	<div class="features-grid">
		<article class="feature-card feature-card-large" use:reveal style="--card-index: 0">
			<div class="feature-top">
				<span class="feature-number">01</span>
				<span class="feature-category">PACIENTE</span>
			</div>

			<div class="feature-symbol">✳</div>

			<h3>Relatos e expressão pessoal</h3>
			<p>
				Espaço para compartilhar experiências e sentimentos por meio de relatos, com opções de
				publicação anônima ou identificada e diferentes possibilidades de visibilidade.
			</p>

			<div class="feature-tags">
				<span>Relatos</span>
				<span>Anonimato</span>
				<span>Publicações</span>
			</div>
		</article>

		<article class="feature-card" use:reveal style="--card-index: 1">
			<div class="feature-top">
				<span class="feature-number">02</span>
				<span class="feature-category">CONEXÃO</span>
			</div>

			<div class="feature-symbol">↗</div>

			<h3>Solicitação de conversas</h3>
			<p>
				Profissionais podem demonstrar interesse em conversar a partir dos relatos. O paciente
				mantém o controle sobre aceitar ou recusar cada solicitação.
			</p>
		</article>

		<article class="feature-card" use:reveal style="--card-index: 2">
			<div class="feature-top">
				<span class="feature-number">03</span>
				<span class="feature-category">COMUNICAÇÃO</span>
			</div>

			<div class="feature-symbol">⌁</div>

			<h3>Chat privado em tempo real</h3>
			<p>
				Após a aceitação da solicitação, paciente e profissional podem estabelecer uma conversa em
				ambiente privado, com comunicação em tempo real.
			</p>
		</article>

		<article class="feature-card" use:reveal style="--card-index: 3">
			<div class="feature-top">
				<span class="feature-number">04</span>
				<span class="feature-category">ORGANIZAÇÃO</span>
			</div>

			<div class="feature-symbol">▦</div>

			<h3>Agendamento de consultas</h3>
			<p>
				Recursos de disponibilidade e gerenciamento de horários permitem que profissionais organizem
				sua agenda e pacientes solicitem sessões.
			</p>
		</article>

		<article class="feature-card" use:reveal style="--card-index: 4">
			<div class="feature-top">
				<span class="feature-number">05</span>
				<span class="feature-category">SESSÕES ONLINE</span>
			</div>

			<div class="feature-symbol">◉</div>

			<h3>Atendimento por áudio e vídeo</h3>
			<p>
				As sessões online utilizam comunicação em tempo real com WebRTC, permitindo interação por
				áudio e vídeo entre paciente e profissional.
			</p>
		</article>

		<article class="feature-card feature-card-large" use:reveal style="--card-index: 5">
			<div class="feature-top">
				<span class="feature-number">06</span>
				<span class="feature-category">ACOMPANHAMENTO</span>
			</div>

			<div class="feature-symbol">⌁</div>

			<h3>Registro de humor e acompanhamento</h3>
			<p>
				O paciente pode registrar seu humor diariamente e visualizar cards com informações e
				reflexões geradas a partir desses registros, contribuindo para o acompanhamento pessoal.
			</p>

			<div class="feature-tags">
				<span>Humor diário</span>
				<span>Cards informativos</span>
			</div>
		</article>
	</div>
</section>

<style>
	.features-section {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
		padding: 120px 0;
	}

	.section-label {
		color: #0abf48;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 1.8px;
	}

	.section-header {
		display: flex;
		align-items: flex-end;
		justify-content: space-between;
		gap: 50px;
		margin-bottom: 56px;
	}

	.section-header h2 {
		max-width: 650px;
		margin-top: 20px;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(36px, 5vw, 56px);
		line-height: 1.12;
		letter-spacing: -2px;
	}

	.section-header h2 span {
		color: #0abf48;
	}

	.section-description {
		max-width: 350px;
		color: #66766c;
		font-size: 14px;
		line-height: 1.8;
	}

	.features-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 18px;
	}

	.feature-card {
		min-height: 310px;
		padding: 32px;
		display: flex;
		flex-direction: column;
		align-items: flex-start;

		border: 1px solid #e1eae1;
		border-radius: 16px;
		background: #ffffff;

		transition:
			transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1),
			border-color 0.35s ease,
			box-shadow 0.35s ease,
			background 0.35s ease;

		transition-delay: calc(var(--card-index, 0) * 90ms);
	}

	.feature-card:hover {
		transform: translateY(-7px);
		border-color: #a8dfb5;
		box-shadow: 0 20px 40px rgb(23 37 30 / 9%);
	}

	.feature-card-large {
		background: #f0faf0;
	}

	.feature-top {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.feature-number {
		color: #0abf48;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 13px;
		font-weight: 700;
	}

	.feature-category {
		color: #849389;
		font-size: 9px;
		font-weight: 700;
		letter-spacing: 1.3px;
	}

	.feature-symbol {
		width: 44px;
		height: 44px;
		margin: 28px 0 20px;

		display: grid;
		place-items: center;

		border-radius: 12px;
		background: #e0ffe0;
		color: #0abf48;
		font-size: 25px;

		transition:
			transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1),
			background 0.35s ease,
			color 0.35s ease;
	}

	.feature-card:hover .feature-symbol {
		transform: rotate(-8deg) scale(1.1);
		background: #0abf48;
		color: #ffffff;
	}

	.feature-card h3 {
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 21px;
		line-height: 1.3;
	}

	.feature-card p {
		max-width: 480px;
		margin-top: 12px;
		color: #66766c;
		font-size: 13px;
		line-height: 1.8;
	}

	.feature-tags {
		display: flex;
		flex-wrap: wrap;
		gap: 8px;
		margin-top: 22px;
	}

	.feature-tags span {
		padding: 7px 10px;
		border: 1px solid #d5ead8;
		border-radius: 20px;
		color: #597260;
		font-size: 10px;
		font-weight: 600;
		transition:
			background 0.25s ease,
			border-color 0.25s ease,
			color 0.25s ease;
	}

	.feature-tags span:hover {
		background: #e0ffe0;
		border-color: #a8dfb5;
		color: #0abf48;
	}

	@media (max-width: 800px) {
		.section-header {
			flex-direction: column;
			align-items: flex-start;
			gap: 20px;
		}

		.section-description {
			max-width: 600px;
		}
	}

	@media (max-width: 600px) {
		.features-section {
			width: calc(100% - 40px);
			padding: 80px 0;
		}

		.section-header h2 {
			letter-spacing: -1.5px;
		}

		.features-grid {
			grid-template-columns: 1fr;
		}

		.feature-card {
			min-height: auto;
			padding: 26px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.feature-card,
		.feature-symbol,
		.feature-tags span {
			transition: none;
		}

		.feature-card:hover {
			transform: none;
		}

		.feature-card:hover .feature-symbol {
			transform: none;
		}
	}
</style>
