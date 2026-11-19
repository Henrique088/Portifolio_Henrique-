<script lang="ts">
	const screenshots = [
		{
			number: '01',
			title: 'Experiência do paciente',
			description:
				'Área de interação com relatos, registros de humor e recursos de acompanhamento.',
			image: '/images/therapistfriend/paciente.png'
		},
		{
			number: '02',
			title: 'Área do profissional',
			description:
				'Ambiente para visualizar relatos, gerenciar solicitações e acompanhar pacientes.',
			image: '/images/therapistfriend/profissional.png'
		},
		{
			number: '03',
			title: 'Comunicação privada',
			description: 'Chat e recursos de comunicação entre pacientes e profissionais.',
			image: '/images/therapistfriend/chat.png'
		},
		{
			number: '04',
			title: 'Análise e inteligência artificial',
			description:
				'Recursos de análise textual e visualização de informações geradas pelos serviços de IA.',
			image: '/images/therapistfriend/ia.png'
		}
	];

	const highlights = [
		{
			number: '01',
			title: 'Plataforma full stack',
			description:
				'Integração entre interface web, backend, banco de dados e microsserviços especializados.'
		},
		{
			number: '02',
			title: 'Arquitetura organizada',
			description:
				'Separação de responsabilidades com DDD Light, princípios SOLID e injeção de dependências.'
		},
		{
			number: '03',
			title: 'Comunicação em tempo real',
			description: 'Integração de Socket.IO e WebRTC para comunicação e sessões on-line.'
		},
		{
			number: '04',
			title: 'Inteligência artificial',
			description:
				'Aplicação de modelos locais para análise textual e identificação de expressões faciais.'
		}
	];

	type Screenshot = (typeof screenshots)[number];

	let zoomedScreenshot = $state<Screenshot | null>(null);

	function fecharZoom() {
		zoomedScreenshot = null;
	}

	function handleKeydown(event: KeyboardEvent) {
		if (event.key === 'Escape' && zoomedScreenshot) {
			fecharZoom();
		}
	}

	$effect(() => {
		if (!zoomedScreenshot) return;

		const originalOverflow = document.body.style.overflow;
		document.body.style.overflow = 'hidden';

		// Roda automaticamente quando zoomedScreenshot vira null ou o componente é destruído
		return () => {
			document.body.style.overflow = originalOverflow;
		};
	});

	import { reveal } from '#lib/actions/reveal.ts';
</script>

<!-- Permite fechar o zoom pressionando a tecla ESC -->
<svelte:window onkeydown={handleKeydown} />

<section class="results-section" id="resultados" use:reveal>
	<div class="section-container">
		<div class="section-heading">
			<span class="eyebrow">08 — RESULTADOS E APRENDIZADOS</span>
			<h2>Uma ideia transformada<br /><span>em uma aplicação real.</span></h2>
			<p>
				O desenvolvimento do TherapistFriend resultou em uma plataforma web que integra diferentes
				tecnologias para aproximar pacientes e profissionais da saúde mental.
			</p>
		</div>

		<div class="gallery-heading">
			<div>
				<span class="sub-eyebrow">INTERFACE DA PLATAFORMA</span>
				<h3>O sistema em funcionamento</h3>
			</div>
			<span class="gallery-count">04 VISÕES DO SISTEMA</span>
		</div>

		<div class="screenshot-grid">
			{#each screenshots as screenshot (screenshot.number)}
				<article
					class="screenshot-card"
					use:reveal
					style={`--card-index: ${Number(screenshot.number) - 1}`}
				>
					<div class="screenshot-frame">
						<div class="browser-bar">
							<div class="browser-dots">
								<span></span>
								<span></span>
								<span></span>
							</div>
							<div class="browser-address">therapistfriend</div>
							<span class="browser-menu">•••</span>
						</div>

						<button
							type="button"
							class="zoom-trigger"
							onclick={() => (zoomedScreenshot = screenshot)}
							aria-label={`Ampliar captura de tela ${screenshot.number}`}
						>
							<img
								class="screenshot-image"
								src={screenshot.image}
								alt={`Captura de tela ${screenshot.number} — ${screenshot.title}`}
							/>
						</button>
					</div>

					<div class="screenshot-info">
						<span class="screenshot-number">{screenshot.number}</span>
						<div>
							<h4>{screenshot.title}</h4>
							<p>{screenshot.description}</p>
						</div>
					</div>
				</article>
			{/each}
		</div>

		<div class="gallery-tip">
			<span class="tip-icon">i</span>
			<p>
				As capturas apresentam diferentes áreas do TherapistFriend. Clique em qualquer imagem para
				ampliar e visualizar os detalhes da interface.
			</p>
		</div>

		<div class="highlights-section">
			<div class="highlights-heading">
				<span class="sub-eyebrow">PRINCIPAIS ENTREGAS</span>
				<h3>Mais do que uma interface.</h3>
				<p>
					O projeto envolveu decisões de arquitetura, integração entre tecnologias e desenvolvimento
					de funcionalidades distribuídas em diferentes serviços.
				</p>
			</div>

			<div class="highlights-grid">
				{#each highlights as item (item.number)}
					<article
						class="highlight-item"
						use:reveal
						style={`--card-index: ${Number(item.number) - 1}`}
					>
						<span>{item.number}</span>
						<h4>{item.title}</h4>
						<p>{item.description}</p>
					</article>
				{/each}
			</div>
		</div>

		<div class="feedback-section" use:reveal>
			<div class="feedback-symbol">✳</div>
			<div>
				<span class="sub-eyebrow">VALIDAÇÃO DAS IDEIAS</span>
				<h3>Desenvolvimento orientado por feedback.</h3>
				<p>
					Durante demonstrações da plataforma, duas psicólogas contribuíram com sugestões sobre a
					experiência de uso, a organização dos fluxos e a apresentação das informações. Os
					comentários recebidos foram considerados e incorporados em melhorias da aplicação.
				</p>
			</div>
		</div>

		<div class="final-statement" use:reveal>
			<span class="sub-eyebrow">O QUE FICOU DO PROJETO</span>
			<h3>
				Construir software também é compreender problemas, tomar decisões e conectar diferentes
				áreas do conhecimento.
			</h3>
			<p>
				O TherapistFriend reuniu desenvolvimento web, arquitetura de software, comunicação em tempo
				real e inteligência artificial em uma única experiência.
			</p>
		</div>
	</div>
</section>

<!-- Modal de Zoom (só renderiza quando há uma imagem selecionada) -->
{#if zoomedScreenshot}
	<!-- svelte-ignore a11y_click_events_have_key_events -->
	<!-- svelte-ignore a11y_no_static_element_interactions -->
	<div class="lightbox-backdrop" onclick={fecharZoom}>
		<img
			class="lightbox-image"
			src={zoomedScreenshot.image}
			alt={`Captura de tela ${zoomedScreenshot.number} — ${zoomedScreenshot.title}`}
		/>
		<span class="lightbox-hint">Clique em qualquer lugar ou pressione ESC para fechar</span>
	</div>
{/if}

<style>
	.results-section {
		padding: 112px 0;
		background: #17251e;
		color: #f5f8f3;
	}

	.section-container {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
	}

	.section-heading {
		max-width: 720px;
		margin-bottom: 72px;
	}

	.eyebrow,
	.sub-eyebrow {
		display: inline-block;
		color: #398c4e;
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.13em;
	}

	.eyebrow {
		margin-bottom: 20px;
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

	.gallery-heading {
		display: flex;
		align-items: flex-end;
		justify-content: space-between;
		gap: 20px;
		margin-bottom: 25px;
	}

	.gallery-heading h3,
	.highlights-heading h3 {
		margin-top: 10px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.8rem;
		letter-spacing: -0.045em;
	}

	.gallery-count {
		color: #929c93;
		font-size: 0.68rem;
		font-weight: 700;
		letter-spacing: 0.1em;
	}

	.screenshot-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 30px 22px;
	}

	.screenshot-card {
		min-width: 0;
		border-radius: 14px;

		transition: transform 0.4s cubic-bezier(0.2, 0.8, 0.2, 1);
	}

	.screenshot-card:hover {
		transform: translateY(-6px);
	}

	.screenshot-frame {
		overflow: hidden;
		border: 1px solid #e0e8df;
		border-radius: 14px;
		background: #f1f5ef;
		box-shadow: 0 8px 24px #17251e0a;
		transition:
			border-color 0.35s ease,
			box-shadow 0.35s ease;
	}

	.screenshot-card:hover .screenshot-frame {
		border-color: #a8d6a1;
		box-shadow: 0 18px 35px rgb(0 0 0 / 16%);
	}

	.screenshot-image {
		display: block;
		width: 100%;
		max-width: 100%;
		/* aspect-ratio: 16 / 10; */
		object-fit: cover;

		transition: transform 0.65s cubic-bezier(0.2, 0.8, 0.2, 1);
	}

	.browser-bar {
		display: flex;
		height: 39px;
		align-items: center;
		justify-content: space-between;
		gap: 12px;
		padding: 0 13px;
		border-bottom: 1px solid #e0e8df;
		background: #fff;
	}

	.browser-dots {
		display: flex;
		gap: 5px;
	}

	.browser-dots span {
		width: 7px;
		height: 7px;
		border-radius: 50%;
		background: #c5d1c4;
	}

	.browser-address {
		padding: 5px 20px;
		border-radius: 5px;
		background: #f2f5f1;
		color: #929c93;
		font-size: 0.62rem;
	}

	.browser-menu {
		color: #929c93;
		font-size: 0.7rem;
	}

	.screenshot-placeholder {
		display: flex;
		min-height: 250px;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 12px;
		padding: 24px;
		text-align: center;
	}

	.placeholder-icon {
		display: grid;
		width: 52px;
		height: 52px;
		place-items: center;
		border: 1px dashed #9eb99b;
		border-radius: 14px;
		color: #398c4e;
		font-size: 1.5rem;
	}

	.screenshot-placeholder strong {
		color: #526457;
		font-size: 0.88rem;
	}

	.screenshot-placeholder > span {
		max-width: 100%;
		overflow-wrap: anywhere;
		color: #98a399;
		font-family: monospace;
		font-size: 0.7rem;
	}

	.screenshot-info {
		display: flex;
		gap: 15px;
		margin-top: 17px;
	}

	.screenshot-number {
		color: #398c4e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 0.85rem;
		font-weight: 700;
		transition:
			transform 0.3s ease,
			color 0.3s ease;
	}

	.screenshot-card:hover .screenshot-number {
		transform: translateX(4px);
		color: #b8ef6b;
	}

	.screenshot-info h4 {
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.05rem;
		transition: color 0.3s ease;
	}

	.screenshot-card:hover .screenshot-info h4 {
		color: #b8ef6b;
	}

	.screenshot-info p {
		margin-top: 6px;
		color: #68756c;
		font-size: 0.82rem;
		line-height: 1.65;
	}

	.gallery-tip {
		display: flex;
		align-items: flex-start;
		gap: 12px;
		margin-top: 27px;
		padding: 17px;
		border-radius: 11px;
		background: #edf6ec;
	}

	.tip-icon {
		display: grid;
		width: 22px;
		height: 22px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 50%;
		background: #d7f2d2;
		color: #398c4e;
		font-size: 0.75rem;
		font-weight: 700;
	}

	.gallery-tip p {
		color: #68756c;
		font-size: 0.8rem;
		line-height: 1.65;
	}

	.highlights-section {
		margin-top: 100px;
	}

	.highlights-heading {
		max-width: 650px;
		margin-bottom: 35px;
	}

	.highlights-heading > p {
		margin-top: 12px;
		color: #68756c;
		font-size: 0.9rem;
		line-height: 1.75;
	}

	.highlights-grid {
		display: grid;
		grid-template-columns: repeat(4, minmax(0, 1fr));
		gap: 18px;
	}

	.highlight-item {
		padding-top: 20px;
		border-top: 1px solid #dce5dc;

		transition:
			transform 0.35s ease,
			border-color 0.35s ease;
	}

	.highlight-item:hover {
		transform: translateY(-5px);
		border-color: #398c4e;
	}

	.highlight-item > span {
		color: #398c4e;
		font-size: 0.75rem;
		font-weight: 700;
		transition: color 0.3s ease;
	}

	.highlight-item:hover > span {
		color: #b8ef6b;
	}

	.highlight-item h4 {
		margin-top: 18px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.05rem;
		letter-spacing: -0.025em;
		transition: color 0.3s ease;
	}

	.highlight-item:hover h4 {
		color: #b8ef6b;
	}

	.highlight-item p {
		margin-top: 10px;
		color: #68756c;
		font-size: 0.82rem;
		line-height: 1.7;
	}

	.feedback-section {
		display: flex;
		align-items: flex-start;
		gap: 22px;
		margin-top: 85px;
		padding: 32px;
		border: 1px solid #dce9dc;
		border-radius: 18px;
		background: #f7faf6;
	}

	.feedback-symbol {
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
			transform 0.35s ease,
			background 0.35s ease;
	}

	.feedback-section:hover .feedback-symbol {
		transform: rotate(12deg) scale(1.08);
		background: #b8ef6b;
	}

	.feedback-section h3 {
		margin-top: 10px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.5rem;
		letter-spacing: -0.04em;
	}

	.feedback-section p {
		max-width: 780px;
		margin-top: 12px;
		color: #68756c;
		font-size: 0.88rem;
		line-height: 1.8;
	}

	.final-statement {
		margin-top: 95px;
		padding: 55px;
		border-radius: 22px;
		background: #17251e;
		color: #f5f8f3;
		transition:
			background 0.4s ease,
			transform 0.4s ease;
	}

	.final-statement:hover {
		background: #20372a;
		transform: translateY(-4px);
	}

	.final-statement .sub-eyebrow {
		color: #b8ef6b;
	}

	.final-statement h3 {
		max-width: 850px;
		margin-top: 20px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(1.7rem, 3.5vw, 2.7rem);
		line-height: 1.25;
		letter-spacing: -0.045em;
	}

	.final-statement p {
		max-width: 650px;
		margin-top: 18px;
		color: #b2c0b5;
		font-size: 0.9rem;
		line-height: 1.8;
	}

	.zoom-trigger {
		background: none;
		border: none;
		width: 100%;
		padding: 0;
		cursor: zoom-in;
		display: block;
		background: none;
		cursor: zoom-in;
	}

	.zoom-trigger:hover .screenshot-image {
		transform: scale(1.035);
	}

	.zoom-trigger:focus-visible {
		outline: 3px solid #398c4e;
		outline-offset: -3px;
	}

	.screenshot-image {
		display: block;
		max-width: 100%;
		transition: transform 0.2s ease;
	}

	.zoom-trigger:hover .screenshot-image {
		transform: scale(1.01);
	}

	/* Fundo escuro em tela cheia */
	.lightbox-backdrop {
		position: fixed;
		inset: 0;
		background: rgba(0, 0, 0, 0.85);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 1rem;
		padding: 2rem;
		z-index: 9999;
		cursor: zoom-out;
		animation: fadeIn 0.15s ease-out;
	}

	.lightbox-image {
		max-width: 92vw;
		max-height: 85vh;
		object-fit: contain;
		border-radius: 8px;
		box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
		animation: imageZoom 0.3s cubic-bezier(0.16, 1, 0.3, 1);
	}

	@keyframes imageZoom {
		from {
			opacity: 0;
			transform: scale(0.94);
		}

		to {
			opacity: 1;
			transform: scale(1);
		}
	}

	.lightbox-hint {
		color: #d1d5db;
		font-size: 0.875rem;
	}

	@keyframes fadeIn {
		from {
			opacity: 0;
		}
		to {
			opacity: 1;
		}
	}

	@media (max-width: 900px) {
		.highlights-grid {
			grid-template-columns: repeat(2, 1fr);
			row-gap: 30px;
		}
	}

	@media (max-width: 650px) {
		.results-section {
			padding: 80px 0;
		}

		.section-container {
			width: calc(100% - 40px);
		}

		.screenshot-grid {
			grid-template-columns: 1fr;
		}

		.gallery-heading {
			align-items: flex-start;
			flex-direction: column;
		}

		.highlights-grid {
			grid-template-columns: 1fr;
		}

		.feedback-section {
			padding: 22px;
		}

		.final-statement {
			margin-top: 65px;
			padding: 30px 24px;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.screenshot-card,
		.screenshot-frame,
		.screenshot-image,
		.screenshot-number,
		.screenshot-info h4,
		.highlight-item,
		.highlight-item > span,
		.highlight-item h4,
		.feedback-section,
		.feedback-symbol,
		.final-statement,
		.lightbox-image {
			transition: none !important;
			animation: none !important;
			transform: none !important;
		}
	}
</style>
