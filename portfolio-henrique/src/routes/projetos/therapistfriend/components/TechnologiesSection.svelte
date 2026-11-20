<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="technologies-section" id="tecnologias" use:reveal>
	<div class="technologies-container">
		<div class="section-heading" use:reveal>
			<span class="section-label">09 — TECNOLOGIAS</span>

			<h2>
				Uma stack construída para
				<span>conectar diferentes soluções.</span>
			</h2>

			<p>
				O desenvolvimento do TherapistFriend integrou tecnologias para aplicações web, processamento
				assíncrono, comunicação em tempo real, segurança e inteligência artificial.
			</p>
		</div>

		<div class="technology-grid">
			<article class="technology-card" use:reveal>
				<div class="technology-card-header">
					<span class="technology-index">01</span>
					<span class="technology-icon">⌘</span>
				</div>

				<h3>Frontend</h3>
				<p>Interface e experiência de usuário.</p>

				<div class="technology-list">
					<span>React</span>
					<span>React Router</span>
					<span>CSS Modules</span>
					<span>Axios</span>
				</div>
			</article>

			<article class="technology-card">
				<div class="technology-card-header">
					<span class="technology-index">02</span>
					<span class="technology-icon">⌘</span>
				</div>

				<h3>Backend</h3>
				<p>Regras de negócio, APIs e organização da aplicação.</p>

				<div class="technology-list">
					<span>Node.js</span>
					<span>TypeScript</span>
					<span>Express</span>
					<span>Sequelize</span>
				</div>
			</article>

			<article class="technology-card">
				<div class="technology-card-header">
					<span class="technology-index">03</span>
					<span class="technology-icon">▤</span>
				</div>

				<h3>Dados e processamento</h3>
				<p>Persistência, filas e execução de tarefas assíncronas.</p>

				<div class="technology-list">
					<span>PostgreSQL</span>
					<span>Redis</span>
					<span>BullMQ</span>
				</div>
			</article>

			<article class="technology-card">
				<div class="technology-card-header">
					<span class="technology-index">04</span>
					<span class="technology-icon">⌁</span>
				</div>

				<h3>Comunicação em tempo real</h3>
				<p>Conexões, eventos e comunicação entre serviços.</p>

				<div class="technology-list">
					<span>Socket.IO</span>
					<span>WebRTC</span>
					<span>Coturn</span>
					<span>gRPC</span>
				</div>
			</article>

			<article class="technology-card">
				<div class="technology-card-header">
					<span class="technology-index">05</span>
					<span class="technology-icon">✳</span>
				</div>

				<h3>Inteligência artificial</h3>
				<p>Processamento textual e reconhecimento de emoções.</p>

				<div class="technology-list">
					<span>Python</span>
					<span>Flask</span>
					<span>Ollama</span>
					<span>Llama 3</span>
					<span>YOLOv8</span>
					<span>AffectNet</span>
				</div>
			</article>

			<article class="technology-card">
				<div class="technology-card-header">
					<span class="technology-index">06</span>
					<span class="technology-icon">⬡</span>
				</div>

				<h3>Infraestrutura e segurança</h3>
				<p>Ambiente de execução, autenticação e proteção de dados.</p>

				<div class="technology-list">
					<span>Docker</span>
					<span>JWT</span>
					<span>bcrypt</span>
					<span>AES-256</span>
					<span>Nodemailer</span>
					<span>Twilio</span>
				</div>
			</article>
		</div>

		<div class="technologies-footer" use:reveal>
			<span class="footer-line"></span>
			<p>
				As tecnologias foram integradas de acordo com as necessidades de cada módulo, formando uma
				aplicação com diferentes serviços especializados.
			</p>
			<span class="footer-line"></span>
		</div>
	</div>
</section>

<style>
	.technologies-section {
		padding: 120px 0;
		background: #f0faf0;
	}

	.technologies-container {
		width: min(1180px, calc(100% - 64px));
		margin: 0 auto;
	}

	.section-heading {
		max-width: 760px;
		margin-bottom: 56px;
	}

	.section-label {
		color: #0abf48;
		font-size: 11px;
		font-weight: 700;
		letter-spacing: 1.8px;
	}

	.section-heading h2 {
		margin-top: 20px;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: clamp(36px, 5vw, 56px);
		line-height: 1.12;
		letter-spacing: -2px;
	}

	.section-heading h2 span {
		color: #0abf48;
	}

	.section-heading p {
		max-width: 650px;
		margin-top: 24px;
		color: #66766c;
		font-size: 15px;
		line-height: 1.9;
	}

	.technology-grid {
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: 16px;
	}

	.technology-card {
		min-height: 260px;
		padding: 28px;
		border: 1px solid #dce9dc;
		border-radius: 14px;
		background: #fafffa;
		transition:
			transform 0.35s cubic-bezier(0.2, 0.8, 0.2, 1),
			border-color 0.35s ease,
			box-shadow 0.35s ease,
			background 0.35s ease;
	}

	.technology-card:hover {
		transform: translateY(-7px);
		border-color: #a8ddb4;
		background: #ffffff;
		box-shadow: 0 18px 38px rgb(23 37 30 / 8%);
	}

	.technology-card-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.technology-index {
		color: #0abf48;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 12px;
		font-weight: 700;
		transition: transform 0.3s ease;
	}

	.technology-card:hover .technology-index {
		transform: translateX(3px);
	}

	.technology-icon {
		width: 38px;
		height: 38px;
		display: grid;
		place-items: center;
		border-radius: 10px;
		background: #e0ffe0;
		color: #0abf48;
		font-size: 20px;
		transition:
			transform 0.35s ease,
			background 0.35s ease,
			color 0.35s ease;
	}

	.technology-card:hover .technology-icon {
		transform: rotate(-8deg) scale(1.12);
		background: #0fd850;
		color: #17251e;
	}

	.technology-card h3 {
		margin-top: 25px;
		color: #17251e;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 19px;
		transition: color 0.3s ease;
	}

	.technology-card:hover h3 {
		color: #087d35;
	}

	.technology-card p {
		margin-top: 8px;
		color: #849389;
		font-size: 12px;
		line-height: 1.6;
	}

	.technology-list {
		display: flex;
		flex-wrap: wrap;
		gap: 8px;
		margin-top: 22px;
	}

	.technology-list span {
		padding: 7px 10px;
		border: 1px solid #dce9dc;
		border-radius: 6px;
		background: #ffffff;
		color: #526257;
		font-size: 11px;
		font-weight: 600;
		transition:
			transform 0.25s ease,
			background 0.25s ease,
			border-color 0.25s ease,
			color 0.25s ease;
	}

	.technology-list span:hover {
		transform: translateY(-3px);
		border-color: #a8ddb4;
		background: #e0ffe0;
		color: #087d35;
	}

	.technologies-footer {
		margin-top: 50px;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 24px;
	}

	.technologies-footer p {
		max-width: 570px;
		color: #66766c;
		font-size: 13px;
		line-height: 1.8;
		text-align: center;
	}

	.footer-line {
		width: 55px;
		height: 1px;
		background: #c8ddca;
	}

	@media (max-width: 900px) {
		.technology-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}
	}

	@media (max-width: 600px) {
		.technologies-section {
			padding: 80px 0;
		}

		.technologies-container {
			width: calc(100% - 40px);
		}

		.section-heading h2 {
			letter-spacing: -1.5px;
		}

		.technology-grid {
			grid-template-columns: 1fr;
		}

		.technology-card {
			min-height: auto;
			padding: 24px;
		}

		.technologies-footer {
			gap: 12px;
		}

		.footer-line {
			width: 20px;
			flex-shrink: 0;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.technology-card,
		.technology-icon,
		.technology-list span,
		.technology-index,
		.technology-card h3 {
			transition: none;
		}

		.technology-card:hover,
		.technology-card:hover .technology-icon,
		.technology-card:hover .technology-index,
		.technology-list span:hover {
			transform: none;
		}
	}
</style>
