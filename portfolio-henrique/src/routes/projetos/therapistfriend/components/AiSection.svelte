<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="ai-section" id="inteligencia-artificial" use:reveal>
	<div class="section-container">
		<div class="section-heading">
			<span class="eyebrow">07 — INTELIGÊNCIA ARTIFICIAL</span>
			<h2>Duas abordagens.<br /><span>Um objetivo: gerar insights.</span></h2>
			<p>
				A inteligência artificial foi integrada ao TherapistFriend em duas frentes complementares:
				processamento de linguagem natural e visão computacional.
			</p>
		</div>

		<div class="ai-intro" use:reveal>
			<div class="intro-symbol">✳</div>
			<div>
				<strong>IA aplicada ao contexto da saúde mental</strong>
				<p>
					Os modelos auxiliam na organização e interpretação de informações da plataforma. Seus
					resultados são recursos de apoio, não diagnósticos clínicos ou substitutos da avaliação
					profissional.
				</p>
			</div>
		</div>

		<div class="ai-cards">
			<article class="ai-card text-ai" use:reveal style="--card-index: 0">
				<div class="ai-card-header">
					<div>
						<span class="ai-label">01 / PROCESSAMENTO DE TEXTO</span>
						<h3>Análise textual</h3>
					</div>
					<div class="ai-illustration text-illustration">
						<div class="chat-bubble bubble-one">...</div>
						<div class="chat-bubble bubble-two">Aa</div>
						<div class="chat-orbit"></div>
					</div>
				</div>

				<p class="ai-description">
					Um microsserviço desenvolvido em Python e Flask utiliza o Ollama com o modelo Llama 3 para
					interpretar informações textuais fornecidas pela plataforma.
				</p>

				<div class="ai-flow">
					<div class="ai-flow-item">
						<span>ENTRADA</span>
						<strong>Relatos e registros de humor</strong>
					</div>
					<div class="ai-flow-arrow">↓</div>
					<div class="ai-flow-item">
						<span>PROCESSAMENTO</span>
						<strong>Flask + Ollama + Llama 3</strong>
					</div>
					<div class="ai-flow-arrow">↓</div>
					<div class="ai-flow-item result">
						<span>RESULTADO</span>
						<strong>Análises e cards informativos</strong>
					</div>
				</div>

				<div class="ai-tech">
					<span>Python</span>
					<span>Flask</span>
					<span>Ollama</span>
					<span>Llama 3</span>
				</div>
			</article>

			<article class="ai-card vision-ai" use:reveal style="--card-index: 1">
				<div class="ai-card-header">
					<div>
						<span class="ai-label">02 / VISÃO COMPUTACIONAL</span>
						<h3>Identificação de emoções</h3>
					</div>
					<div class="ai-illustration vision-illustration">
						<div class="face-frame">
							<div class="face-eye left"></div>
							<div class="face-eye right"></div>
							<div class="face-mouth"></div>
							<span class="corner top-left"></span>
							<span class="corner top-right"></span>
							<span class="corner bottom-left"></span>
							<span class="corner bottom-right"></span>
						</div>
						<div class="scan-line"></div>
					</div>
				</div>

				<p class="ai-description">
					Um microsserviço em Python utiliza modelos YOLOv8 para detectar rostos nos quadros de
					vídeo e identificar expressões emocionais durante as sessões on-line.
				</p>

				<div class="ai-flow">
					<div class="ai-flow-item">
						<span>ENTRADA</span>
						<strong>Quadros de vídeo da sessão</strong>
					</div>
					<div class="ai-flow-arrow">↓</div>
					<div class="ai-flow-item">
						<span>PROCESSAMENTO</span>
						<strong>Detecção facial + classificação emocional</strong>
					</div>
					<div class="ai-flow-arrow">↓</div>
					<div class="ai-flow-item result">
						<span>RESULTADO</span>
						<strong>Expressões identificadas e informações visuais</strong>
					</div>
				</div>

				<div class="ai-tech">
					<span>Python</span>
					<span>YOLOv8</span>
					<span>AffectNet</span>
					<span>gRPC</span>
				</div>
			</article>
		</div>

		<div class="model-details">
			<div class="model-heading">
				<span class="eyebrow">DETALHES TÉCNICOS</span>
				<h3>Treinamento e configuração do modelo visual</h3>
				<p>
					O modelo de classificação emocional foi treinado com dados organizados no formato YOLO
					para o conjunto AffectNet.
				</p>
			</div>

			<div class="metrics-grid">
				<div class="metric" use:reveal style="--card-index: 0">
					<span>ARQUITETURA</span>
					<strong>YOLOv8n</strong>
					<small>Modelo de detecção e classificação</small>
				</div>
				<div class="metric" use:reveal style="--card-index: 1">
					<span>IMAGEM DE ENTRADA</span>
					<strong>224 × 224</strong>
					<small>Resolução utilizada no treinamento emocional</small>
				</div>
				<div class="metric" use:reveal style="--card-index: 2">
					<span>CONFIANÇA</span>
					<strong>0.54</strong>
					<small>Threshold configurado na inferência emocional</small>
				</div>
				<div class="metric" use:reveal style="--card-index: 3">
					<span>TREINAMENTO</span>
					<strong>100 épocas</strong>
					<small>Batch 64 · Otimizador AdamW</small>
				</div>
			</div>

			<div class="model-note">
				<span class="note-icon">i</span>
				<p>
					A detecção facial e a classificação emocional são etapas distintas do processamento
					visual. O modelo de detecção facial utiliza configuração própria, separada dos parâmetros
					do modelo emocional.
				</p>
			</div>
		</div>

		<div class="ai-disclaimer" use:reveal>
			<div class="disclaimer-icon">!</div>
			<div>
				<strong>Uso responsável dos resultados</strong>
				<p>
					Expressões faciais e textos não determinam, isoladamente, o estado psicológico de uma
					pessoa. As análises são informações auxiliares e devem ser interpretadas com cautela pelos
					profissionais.
				</p>
			</div>
		</div>
	</div>
</section>

<style>
	.ai-section {
		padding: 112px 0;
		background: #f7faf6;
		color: #17251e;
	}

	.section-container {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
	}

	.section-heading {
		max-width: 720px;
		margin-bottom: 45px;
	}

	.eyebrow {
		display: inline-block;
		margin-bottom: 20px;
		color: #398c4e;
		font-size: 0.75rem;
		font-weight: 700;
		letter-spacing: 0.13em;
	}

	h2 {
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(2.3rem, 5vw, 4rem);
		line-height: 1.08;
		letter-spacing: -0.055em;
	}

	h2 span {
		color: #398c4e;
	}

	.section-heading > p {
		max-width: 610px;
		margin-top: 22px;
		color: #68756c;
		font-size: 1.05rem;
		line-height: 1.8;
	}

	.ai-intro {
		display: flex;
		align-items: center;
		gap: 20px;
		margin-bottom: 35px;
		padding: 22px;
		border: 1px solid #dce9dc;
		border-radius: 16px;
		background: #edf6ec;
	}

	.intro-symbol {
		display: grid;
		width: 48px;
		height: 48px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 14px;
		background: #d7f2d2;
		color: #398c4e;
		font-size: 1.5rem;
        transition:
    transform 0.4s ease,
    background 0.3s ease;


	}

    .ai-intro:hover .intro-symbol {
  transform: rotate(12deg) scale(1.08);
  background: #c8e9c1;
}

	.ai-intro strong {
		font-size: 0.95rem;
	}

	.ai-intro p {
		margin-top: 6px;
		color: #68756c;
		font-size: 0.86rem;
		line-height: 1.65;
	}

	.ai-cards {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 20px;
	}

	.ai-card {
		min-width: 0;
		padding: 30px;
		border: 1px solid #e1e9df;
		border-radius: 20px;
		background: #fff;
		transition:
			transform 0.4s cubic-bezier(0.2, 0.8, 0.2, 1),
			border-color 0.35s ease,
			box-shadow 0.35s ease;
	}

	.ai-card:hover {
		transform: translateY(-7px);
		border-color: #b8dcae;
		box-shadow: 0 22px 45px rgb(23 37 30 / 9%);
	}

	.ai-card-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 15px;
		min-height: 125px;
	}

	.ai-label {
		color: #398c4e;
		font-size: 0.66rem;
		font-weight: 700;
		letter-spacing: 0.11em;
	}

	.ai-card h3 {
		margin-top: 13px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.6rem;
		letter-spacing: -0.045em;
	}

	.ai-description {
		min-height: 85px;
		margin-top: 20px;
		color: #68756c;
		font-size: 0.88rem;
		line-height: 1.75;
	}

	.ai-illustration {
		position: relative;
		display: grid;
		width: 112px;
		height: 112px;
		flex-shrink: 0;
		place-items: center;
		overflow: hidden;
		border-radius: 22px;
		background: #e9f5e5;
	}

	.chat-bubble {
		position: absolute;
		display: grid;
		place-items: center;
		border: 1px solid #a8d6a1;
		border-radius: 10px;
		background: #fff;
		color: #398c4e;
		font-family: 'Space Grotesk', sans-serif;
		font-weight: 700;
	}

	.bubble-one {
		top: 23px;
		left: 15px;
		width: 58px;
		height: 36px;
		font-size: 1.2rem;
		animation: bubbleFloat 3s ease-in-out infinite;
	}

	.bubble-two {
		right: 12px;
		bottom: 19px;
		width: 44px;
		height: 38px;
		font-size: 1.1rem;
		animation: bubbleFloat 3s ease-in-out infinite;
		animation-delay: 0.8s;
	}

	@keyframes bubbleFloat {
		0%,
		100% {
			transform: translateY(0);
		}

		50% {
			transform: translateY(-5px);
		}
	}

	@keyframes orbitPulse {
		0%,
		100% {
			transform: scale(1);
			opacity: 0.7;
		}

		50% {
			transform: scale(1.5);
			opacity: 1;
		}
	}

	.chat-orbit {
		position: absolute;
		right: 22px;
		top: 15px;
		width: 9px;
		height: 9px;
		border-radius: 50%;
		background: #b8ef6b;
		animation: orbitPulse 2s ease-in-out infinite;
	}

	.vision-illustration {
		background: #17251e;
	}

	.face-frame {
		position: relative;
		width: 60px;
		height: 72px;
		border: 1px solid #b8ef6b;
		border-radius: 45% 45% 42% 42%;
		transition:
			transform 0.4s ease,
			border-color 0.4s ease;
	}

	.vision-ai:hover .face-frame {
		transform: scale(1.08);
		border-color: #d5ff9c;
	}

	.face-eye {
		position: absolute;
		top: 26px;
		width: 5px;
		height: 5px;
		border-radius: 50%;
		background: #b8ef6b;
	}

	.face-eye.left {
		left: 14px;
	}

	.face-eye.right {
		right: 14px;
	}

	.face-mouth {
		position: absolute;
		bottom: 15px;
		left: 50%;
		width: 17px;
		height: 8px;
		border-bottom: 2px solid #b8ef6b;
		border-radius: 50%;
		transform: translateX(-50%);
	}

	.corner {
		position: absolute;
		width: 8px;
		height: 8px;
		border-color: #b8ef6b;
		border-style: solid;
	}

	.top-left {
		top: -4px;
		left: -4px;
		border-width: 1px 0 0 1px;
	}

	.top-right {
		top: -4px;
		right: -4px;
		border-width: 1px 1px 0 0;
	}

	.bottom-left {
		bottom: -4px;
		left: -4px;
		border-width: 0 0 1px 1px;
	}

	.bottom-right {
		right: -4px;
		bottom: -4px;
		border-width: 0 1px 1px 0;
	}

	.scan-line {
		position: absolute;
		top: 24px;
		left: 22px;
		width: 68px;
		height: 1px;
		background: #b8ef6b;
		opacity: 0.7;
		animation: faceScan 3s ease-in-out infinite;
	}

	@keyframes faceScan {
		0%,
		100% {
			top: 12px;
			opacity: 0.3;
		}

		50% {
			top: 92px;
			opacity: 1;
		}
	}

	.ai-flow {
		display: flex;
		flex-direction: column;
		gap: 8px;
		margin-top: 28px;
	}

	.ai-flow-item {
		display: flex;
		flex-direction: column;
		gap: 6px;
		padding: 15px 17px;
		border: 1px solid #e2eae0;
		border-radius: 11px;
		background: #f9fbf8;
		transform: translateX(5px);
		border-color: #a8d6a1;
		background: #f0f8ed;
		box-shadow: 0 5px 15px rgb(23 37 30 / 5%);
	}

	.ai-flow-item:hover {
		transform: translateX(5px);
		border-color: #398c4e;
		background: #e5f3e1;
		box-shadow: 0 5px 15px rgb(23 37 30 / 5%);
	}

	.ai-flow-item.result:hover {
		border-color: #398c4e;
		background: #e5f3e1;
	}

	.ai-flow-item span {
		color: #8a968c;
		font-size: 0.62rem;
		font-weight: 700;
		letter-spacing: 0.1em;
	}

	.ai-flow-item strong {
		font-size: 0.84rem;
		line-height: 1.5;
	}

	.ai-flow-item.result {
		border-color: #c8e5bd;
		background: #edf6ec;
	}

	.ai-flow-item.result span {
		color: #398c4e;
	}

	.ai-flow-arrow {
		color: #398c4e;
		font-size: 1rem;
		text-align: center;
        transition: transform 0.3s ease;
	}

	.ai-tech {
		display: flex;
		flex-wrap: wrap;
		gap: 8px;
		margin-top: 24px;
		transition: transform 0.3s ease;
	}

	.ai-flow-item:hover + .ai-flow-arrow {
		transform: scale(1.2);
	}

	.ai-tech span {
		padding: 7px 10px;
		border: 1px solid #dce8d9;
		border-radius: 7px;
		background: #f3f8f1;
		color: #398c4e;
		font-size: 0.7rem;
		font-weight: 600;
		transition:
			transform 0.25s ease,
			background 0.25s ease,
			border-color 0.25s ease,
			color 0.25s ease;
	}

	.ai-tech span:hover {
		transform: translateY(-3px);
		border-color: #398c4e;
		background: #398c4e;
		color: #fff;
	}

	.model-details {
		margin-top: 65px;
	}

	.model-heading {
		max-width: 680px;
		margin-bottom: 28px;
	}

	.model-heading h3 {
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.65rem;
		letter-spacing: -0.04em;
	}

	.model-heading p {
		margin-top: 10px;
		color: #68756c;
		font-size: 0.9rem;
		line-height: 1.7;
	}

	.metrics-grid {
		display: grid;
		grid-template-columns: repeat(4, minmax(0, 1fr));
		gap: 12px;
	}

	.metric {
		min-width: 0;
		padding: 22px;
		border: 1px solid #e1e9df;
		border-radius: 14px;
		background: #fff;
		transition:
			transform 0.35s ease,
			border-color 0.35s ease,
			box-shadow 0.35s ease;
	}

	.metric:hover {
		transform: translateY(-5px);
		border-color: #b8dcae;
		box-shadow: 0 12px 28px rgb(23 37 30 / 7%);
	}

	.metric span,
	.metric strong,
	.metric small {
		display: block;
	}

	.metric span {
		color: #8a968c;
		font-size: 0.62rem;
		font-weight: 700;
		letter-spacing: 0.09em;
	}

	.metric strong {
		margin-top: 16px;
		color: #398c4e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.45rem;
		letter-spacing: -0.04em;
		transition: color 0.3s ease;
	}

	.metric:hover strong {
		color: #246c38;
	}

	.metric small {
		margin-top: 8px;
		color: #68756c;
		font-size: 0.73rem;
		line-height: 1.55;
	}

	.model-note {
		display: flex;
		align-items: flex-start;
		gap: 13px;
		margin-top: 16px;
		padding: 18px;
		border-radius: 12px;
		background: #edf6ec;
	}

	.note-icon {
		display: grid;
		width: 23px;
		height: 23px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 50%;
		background: #d7f2d2;
		color: #398c4e;
		font-size: 0.8rem;
		font-weight: 700;
	}

	.model-note p {
		color: #68756c;
		font-size: 0.8rem;
		line-height: 1.65;
	}

	.ai-disclaimer {
		display: flex;
		align-items: flex-start;
		gap: 17px;
		margin-top: 35px;
		padding: 24px;
		border: 1px solid #e8e3c7;
		border-radius: 15px;
		background: #fffdf2;
		transition:
			transform 0.35s ease,
			border-color 0.35s ease,
			box-shadow 0.35s ease;
	}

	.ai-disclaimer:hover {
		transform: translateY(-3px);
		border-color: #e2d98e;
		box-shadow: 0 10px 25px rgb(23 37 30 / 5%);
	}

	.disclaimer-icon {
		display: grid;
		width: 34px;
		height: 34px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 50%;
		background: #f9f047;
		color: #4b4a24;
		font-weight: 700;
		transition: transform 0.3s ease;
	}

	.ai-disclaimer:hover .disclaimer-icon {
		transform: scale(1.1) rotate(-8deg);
	}

	.ai-disclaimer strong {
		font-size: 0.9rem;
	}

	.ai-disclaimer p {
		margin-top: 7px;
		color: #77745e;
		font-size: 0.82rem;
		line-height: 1.7;
	}

	@media (max-width: 900px) {
		.ai-cards {
			grid-template-columns: 1fr;
		}

		.metrics-grid {
			grid-template-columns: repeat(2, 1fr);
		}

		.ai-description {
			min-height: auto;
		}
	}

	@media (max-width: 600px) {
		.ai-section {
			padding: 80px 0;
		}

		.section-container {
			width: calc(100% - 40px);
		}

		.ai-card {
			padding: 22px;
		}

		.ai-illustration {
			width: 85px;
			height: 85px;
		}

		.metrics-grid {
			grid-template-columns: 1fr 1fr;
		}

		.metric {
			padding: 16px;
		}

		.metric strong {
			font-size: 1.2rem;
		}

		.ai-intro,
		.ai-disclaimer {
			align-items: flex-start;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.bubble-one,
		.bubble-two,
		.chat-orbit,
		.scan-line {
			animation: none !important;
		}

		.ai-card,
		.ai-intro,
		.intro-symbol,
		.ai-flow-item,
		.ai-flow-arrow,
		.ai-tech span,
		.metric,
		.metric strong,
		.face-frame,
		.ai-disclaimer,
		.disclaimer-icon {
			transition: none !important;
			transform: none !important;
		}
	}
</style>
