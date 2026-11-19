<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="learning-section" id="aprendizados" use:reveal>
	<div class="learning-container">
		<div class="learning-heading" use:reveal>
			<span class="section-label">10 — EXPERIÊNCIA CONSTRUÍDA</span>

			<h2>
				Engenharia de software
				<span>aplicada na prática.</span>
			</h2>

			<p>
				O desenvolvimento do TherapistFriend envolveu decisões técnicas e integração de diferentes
				tecnologias para construir uma aplicação completa, organizada e preparada para experiências
				em tempo real.
			</p>
		</div>

		<div class="learning-content">
			<div class="learning-intro" use:reveal>
				<span class="intro-symbol">✳</span>

				<h3>Mais do que implementar funcionalidades, conectar diferentes partes de um sistema.</h3>

				<p>
					Ao longo do projeto, trabalhei desde a estruturação do backend até a integração de
					serviços especializados, buscando manter responsabilidades bem definidas e uma comunicação
					consistente entre os módulos.
				</p>
			</div>

			<div class="learning-list">
				<article class="learning-item" use:reveal>
					<span class="learning-number">01</span>

					<div>
						<h3>Arquitetura e organização</h3>
						<p>
							Aplicação de DDD Light, princípios SOLID, injeção de dependência e separação de
							responsabilidades para estruturar o backend.
						</p>
					</div>

					<span class="learning-arrow">↗</span>
				</article>

				<article class="learning-item">
					<span class="learning-number">02</span>

					<div>
						<h3>Processamento assíncrono e eventos</h3>
						<p>
							Integração de Domain Events, Redis e BullMQ para coordenar tarefas em segundo plano e
							comunicação entre módulos.
						</p>
					</div>

					<span class="learning-arrow">↗</span>
				</article>

				<article class="learning-item">
					<span class="learning-number">03</span>

					<div>
						<h3>Comunicação em tempo real</h3>
						<p>
							Implementação de recursos com Socket.IO e WebRTC, incluindo troca de mensagens e
							sessões online com áudio e vídeo.
						</p>
					</div>

					<span class="learning-arrow">↗</span>
				</article>

				<article class="learning-item">
					<span class="learning-number">04</span>

					<div>
						<h3>Integração de inteligência artificial</h3>
						<p>
							Desenvolvimento e integração de microsserviços para análise textual e reconhecimento
							de emoções por visão computacional.
						</p>
					</div>

					<span class="learning-arrow">↗</span>
				</article>

				<article class="learning-item">
					<span class="learning-number">05</span>

					<div>
						<h3>Segurança e proteção de dados</h3>
						<p>
							Implementação de autenticação, autorização, validações, criptografia de mensagens e
							mecanismos de controle de acesso.
						</p>
					</div>

					<span class="learning-arrow">↗</span>
				</article>
			</div>
		</div>
	</div>
</section>

<style>
	.learning-section {
		padding: 120px 0;
		background: #17251e;
		color: #f7faf6;
	}

	.learning-container {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
	}

	.section-label {
		color: #0fd850;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 1.8px;
	}

	.learning-heading {
		max-width: 760px;
	}

	.learning-heading h2 {
		margin-top: 20px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(36px, 5vw, 56px);
		line-height: 1.12;
		letter-spacing: -2px;
	}

	.learning-heading h2 span {
		display: block;
		color: #0fd850;
	}

	.learning-heading > p {
		max-width: 650px;
		margin-top: 24px;
		color: #aab8ae;
		font-size: 15px;
		line-height: 1.9;
	}

	.learning-content {
		display: grid;
		grid-template-columns: 0.8fr 1.2fr;
		gap: 90px;
		margin-top: 72px;
		align-items: start;
	}

	.learning-intro {
		position: sticky;
		top: 40px;
	}

	.intro-symbol {
		width: 52px;
		height: 52px;
		display: grid;
		place-items: center;
		border: 1px solid #3b5945;
		border-radius: 14px;
		color: #0fd850;
		font-size: 27px;

		transition:
			transform 0.4s ease,
			background 0.4s ease,
			border-color 0.4s ease;
	}

	.learning-intro:hover .intro-symbol {
		transform: rotate(45deg);
		background: rgb(15 216 80 / 10%);
		border-color: #0fd850;
	}

	.learning-intro h3 {
		margin-top: 28px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 27px;
		line-height: 1.35;
		letter-spacing: -0.8px;
	}

	.learning-intro p {
		margin-top: 20px;
		color: #aab8ae;
		font-size: 14px;
		line-height: 1.9;
	}

	.learning-list {
		border-top: 1px solid #35463b;
	}

	.learning-item {
		display: grid;
		grid-template-columns: 38px 1fr 20px;
		gap: 18px;
		align-items: start;
		padding: 27px 14px;
		margin-inline: -14px;
		border-bottom: 1px solid #35463b;
		border-radius: 8px;
		transition:
			transform 0.3s ease,
			background 0.3s ease,
			border-color 0.3s ease;
	}

	.learning-item:hover {
		transform: translateX(6px);
		background: rgb(255 255 255 / 3%);
		border-bottom-color: #0fd850;
	}

	.learning-number {
		padding-top: 3px;
		color: #0fd850;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 12px;
		font-weight: 700;
		transition: transform 0.3s ease;
	}

	.learning-item:hover .learning-number {
		transform: translateX(3px);
	}

	.learning-item h3 {
		color: #f7faf6;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 17px;
	}

	.learning-item p {
		margin-top: 9px;
		color: #aab8ae;
		font-size: 13px;
		line-height: 1.8;
	}

	.learning-arrow {
		color: #0fd850;
		font-size: 17px;
		transition: transform 0.3s ease;
	}

	.learning-item:hover .learning-arrow {
		transform: translate(3px, -3px);
	}

	@media (max-width: 850px) {
		.learning-content {
			grid-template-columns: 1fr;
			gap: 45px;
		}

		.learning-intro {
			position: static;
			max-width: 600px;
		}
	}

	@media (max-width: 600px) {
		.learning-section {
			padding: 80px 0;
		}

		.learning-container {
			width: calc(100% - 40px);
		}

		.learning-heading h2 {
			letter-spacing: -1.5px;
		}

		.learning-item {
			grid-template-columns: 28px 1fr 16px;
			gap: 12px;
		}

		.learning-item h3 {
			font-size: 15px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.learning-item,
		.learning-number,
		.learning-arrow,
		.intro-symbol {
			transition: none;
		}

		.learning-item:hover,
		.learning-item:hover .learning-number,
		.learning-item:hover .learning-arrow,
		.learning-intro:hover .intro-symbol {
			transform: none;
		}
	}
</style>
