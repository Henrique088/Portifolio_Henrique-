<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="solution-section" id="solucao" use:reveal>
	<div class="solution-container">
		<div class="solution-header">
			<span class="section-label">02 — A SOLUÇÃO</span>

			<h2>
				Uma plataforma.
				<span>Novas possibilidades de conexão.</span>
			</h2>

			<p>
				O TherapistFriend foi desenvolvido como uma plataforma web gratuita que aproxima pacientes e
				profissionais da saúde mental por meio de funcionalidades de interação, comunicação privada
				e acompanhamento.
			</p>
		</div>

		<div class="solution-flow">
			<article class="flow-card" use:reveal>
				<div class="flow-icon">
					<span>01</span>
				</div>

				<div>
					<span class="flow-label">EXPRESSÃO</span>
					<h3>Compartilhamento de relatos</h3>
					<p>
						O paciente pode publicar relatos sobre suas experiências, com a possibilidade de manter
						sua identidade anônima.
					</p>
				</div>
			</article>

			<div class="flow-connector">
				<span></span>
			</div>

			<article class="flow-card" use:reveal>
				<div class="flow-icon">
					<span>02</span>
				</div>

				<div>
					<span class="flow-label">APROXIMAÇÃO</span>
					<h3>Conexão com profissionais</h3>
					<p>
						Profissionais podem visualizar os relatos disponíveis e solicitar uma conversa privada.
						O paciente decide se deseja aceitar a solicitação.
					</p>
				</div>
			</article>

			<div class="flow-connector">
				<span></span>
			</div>

			<article class="flow-card" use:reveal>
				<div class="flow-icon">
					<span>03</span>
				</div>

				<div>
					<span class="flow-label">ACOMPANHAMENTO</span>
					<h3>Comunicação e sessões online</h3>
					<p>
						Após a aceitação, os usuários podem conversar em um chat privado e utilizar recursos de
						agendamento e sessões online por áudio e vídeo.
					</p>
				</div>
			</article>
		</div>

		<div class="solution-footer" use:reveal>
			<div class="solution-footer-icon">✳</div>
			<p>
				A proposta é integrar diferentes recursos em um único ambiente, tornando a experiência de
				interação entre pacientes e profissionais mais acessível e organizada.
			</p>
		</div>
	</div>
</section>

<style>
	.solution-section {
		padding: 120px 0;
		background: #e0ffe0;
	}

	.solution-container {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
	}

	.section-label {
		color: #0abf48;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 1.8px;
	}

	.solution-header {
		max-width: 780px;
	}

	.solution-header h2 {
		margin-top: 20px;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(36px, 5vw, 58px);
		line-height: 1.12;
		letter-spacing: -2px;
	}

	.solution-header h2 span {
		color: #0abf48;
	}

	.solution-header p {
		max-width: 650px;
		margin-top: 24px;
		color: #66766c;
		font-size: 15px;
		line-height: 1.9;
	}

	.solution-flow {
		margin-top: 64px;
		display: grid;
		grid-template-columns: 1fr auto 1fr auto 1fr;
		align-items: center;
		gap: 20px;
	}

	.flow-card {
		min-height: 270px;
		padding: 30px;
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		gap: 32px;
		border: 1px solid #d0ead3;
		border-radius: 16px;
		background: #f7faf6;
		transition:
			transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1),
			border-color 0.35s ease,
			box-shadow 0.35s ease;
	}

	.flow-card:hover {
		transform: translateY(-8px);
		border-color: #0abf48;
		box-shadow: 0 18px 38px rgb(23 37 30 / 9%);
	}

	.flow-icon {
		width: 46px;
		height: 46px;
		display: grid;
		place-items: center;
		border-radius: 12px;
		background: #0fd850;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 15px;
		font-weight: 700;
		transition:
			transform 0.35s ease,
			background 0.35s ease,
			box-shadow 0.35s ease;
	}

	.flow-card:hover .flow-icon {
		transform: rotate(-8deg) scale(1.1);
		background: #0abf48;
		box-shadow: 0 6px 16px rgb(10 191 72 / 20%);
	}

	.flow-label {
		color: #0abf48;
		font-size: 10px;
		font-weight: 700;
		letter-spacing: 1.5px;
	}

	.flow-card h3 {
		margin-top: 10px;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 19px;
		line-height: 1.3;
	}

	.flow-card p {
		margin-top: 12px;
		color: #66766c;
		font-size: 13px;
		line-height: 1.75;
	}

	.flow-connector {
		position: relative;
		width: 24px;
		height: 1px;
		overflow: hidden;
		background: #9ccda5;
	}

	.flow-connector span {
		position: absolute;
		inset: 0;
		width: 40%;
		background: #0abf48;
		animation: connectorFlow 2s ease-in-out infinite;
	}

	@keyframes connectorFlow {
		0% {
			transform: translateX(-100%);
		}

		100% {
			transform: translateX(250%);
		}
	}

	.solution-footer {
		max-width: 800px;
		margin-top: 56px;
		display: flex;
		align-items: center;
		gap: 20px;
	}

	.solution-footer-icon {
		flex-shrink: 0;
		color: #0abf48;
		font-size: 30px;
		transition: transform 0.4s ease;
	}

	.solution-footer:hover .solution-footer-icon {
		transform: rotate(45deg) scale(1.1);
	}

	.solution-footer p {
		color: #526257;
		font-size: 14px;
		line-height: 1.8;
		transition: color 0.3s ease;
	}

	.solution-footer:hover p {
		color: #344c3b;
	}

	@media (max-width: 900px) {
		.solution-flow {
			grid-template-columns: 1fr;
			gap: 14px;
		}

		.flow-card {
			min-height: auto;
		}

		.flow-connector {
			width: 1px;
			height: 22px;
			margin: 0 auto;
		}

		.flow-connector span {
			width: 100%;
			height: 40%;
			animation: connectorFlowVertical 2s ease-in-out infinite;
		}

		@keyframes connectorFlowVertical {
			0% {
				transform: translateY(-100%);
			}

			100% {
				transform: translateY(250%);
			}
		}
	}

	@media (max-width: 600px) {
		.solution-section {
			padding: 80px 0;
		}

		.solution-container {
			width: calc(100% - 40px);
		}

		.solution-header h2 {
			letter-spacing: -1.5px;
		}

		.flow-card {
			padding: 24px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.flow-card,
		.flow-icon,
		.solution-footer-icon,
		.solution-footer p {
			transition: none;
		}

		.flow-card:hover,
		.flow-card:hover .flow-icon,
		.solution-footer:hover .solution-footer-icon {
			transform: none;
		}

		.flow-connector span {
			animation: none;
			width: 100%;
			height: 100%;
		}
	}
</style>
