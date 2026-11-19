<script lang="ts">
	import { reveal } from '#lib/actions/reveal.ts';
</script>

<section class="security-section" id="seguranca" use:reveal>
	<div class="section-container">
		<div class="section-heading">
			<span class="eyebrow">06 — SEGURANÇA DA APLICAÇÃO</span>
			<h2>Proteção em diferentes<br /><span>camadas do sistema.</span></h2>
			<p>
				A segurança do TherapistFriend foi trabalhada desde o controle de acesso até a proteção das
				informações trocadas entre pacientes e profissionais.
			</p>
		</div>

		<div class="security-grid">
			<article class="security-card token-card" use:reveal style="--card-index: 0">
				<div class="card-top">
					<span class="card-icon">⌑</span>
					<span class="card-category">AUTENTICAÇÃO</span>
				</div>
				<h3>Tokens e controle de sessão</h3>
				<p>
					A autenticação utiliza JWT para identificar usuários e controlar o acesso aos recursos da
					aplicação.
				</p>

				<div class="token-list">
					<div>
						<span>Access Token</span>
						<strong>2 horas</strong>
					</div>
					<div>
						<span>Refresh Token</span>
						<strong>7 dias</strong>
					</div>
					<div>
						<span>Socket Token</span>
						<strong>7 dias</strong>
					</div>
				</div>
				<span class="card-footnote"> Prazos configurados na aplicação </span>
			</article>

			<article class="security-card encryption-card" use:reveal style="--card-index: 1">
				<div class="card-top">
					<span class="card-icon">◇</span>
					<span class="card-category">CRIPTOGRAFIA</span>
				</div>
				<h3>Proteção de informações</h3>
				<p>
					Diferentes mecanismos são utilizados para proteger credenciais e informações privadas.
				</p>

				<div class="encryption-item">
					<div class="encryption-symbol">256</div>
					<div>
						<strong>AES-256</strong>
						<span>Criptografia das mensagens privadas</span>
					</div>
				</div>
				<div class="encryption-item">
					<div class="encryption-symbol">BC</div>
					<div>
						<strong>bcrypt</strong>
						<span>Hash de senhas para armazenamento</span>
					</div>
				</div>
			</article>

			<article class="security-card middleware-card" use:reveal style="--card-index: 2">
				<div class="card-top">
					<span class="card-icon">⌘</span>
					<span class="card-category">MIDDLEWARES</span>
				</div>
				<h3>Controle no fluxo das requisições</h3>
				<p>
					Middlewares centralizam verificações e tratam responsabilidades transversais antes que as
					operações sejam executadas.
				</p>

				<div class="middleware-list">
					<div>
						<span class="middleware-dot"></span>
						<div>
							<strong>auth</strong>
							<small>Verificação da autenticação</small>
						</div>
					</div>
					<div>
						<span class="middleware-dot"></span>
						<div>
							<strong>authorize</strong>
							<small>Controle de permissões</small>
						</div>
					</div>
					<div>
						<span class="middleware-dot"></span>
						<div>
							<strong>validation</strong>
							<small>Validação de dados com Joi</small>
						</div>
					</div>
					<div>
						<span class="middleware-dot"></span>
						<div>
							<strong>verifySocketToken</strong>
							<small>Verificação de acesso via Socket</small>
						</div>
					</div>
					<div>
						<span class="middleware-dot"></span>
						<div>
							<strong>errorHandler</strong>
							<small>Tratamento centralizado de erros</small>
						</div>
					</div>
				</div>
			</article>

			<article class="security-card approval-card" use:reveal style="--card-index: 3">
				<div class="card-top">
					<span class="card-icon">✓</span>
					<span class="card-category">CONTROLE DE ACESSO</span>
				</div>
				<h3>Validação de profissionais</h3>
				<p>
					O cadastro de profissionais passa por uma etapa de aprovação administrativa antes que o
					perfil seja considerado validado na plataforma.
				</p>

				<div class="approval-flow">
					<div class="approval-step">
						<span>01</span>
						<strong>Cadastro</strong>
					</div>
					<div class="approval-arrow">→</div>
					<div class="approval-step">
						<span>02</span>
						<strong>Análise administrativa</strong>
					</div>
					<div class="approval-arrow">→</div>
					<div class="approval-step approved">
						<span>03</span>
						<strong>Validação</strong>
					</div>
				</div>
			</article>
		</div>

		<div class="security-principle" use:reveal>
			<div class="principle-icon">⬡</div>
			<div>
				<span>PRINCÍPIO DE PROJETO</span>
				<h3>Segurança não é uma funcionalidade isolada.</h3>
				<p>
					Ela está distribuída entre autenticação, autorização, validação, proteção de dados e
					regras de acesso, acompanhando diferentes etapas de utilização da plataforma.
				</p>
			</div>
		</div>

		<p class="section-note" use:reveal>
			Os mecanismos apresentados representam recursos implementados no projeto. A presença desses
			mecanismos, isoladamente, não equivale a uma auditoria ou certificação de segurança.
		</p>
	</div>
</section>

<style>
	.security-section {
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
		margin-bottom: 56px;
	}

	.eyebrow {
		display: inline-block;
		margin-bottom: 20px;
		color: #b8ef6b;
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
		color: #b8ef6b;
	}

	.section-heading > p {
		max-width: 610px;
		margin-top: 22px;
		color: #b2c0b5;
		font-size: 1.05rem;
		line-height: 1.8;
	}

	.security-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 18px;
	}

	.security-card {
		min-width: 0;
		padding: 30px;
		border: 1px solid #34463a;
		border-radius: 18px;
		background: #202f26;

		transition:
			transform 0.4s cubic-bezier(0.2, 0.8, 0.2, 1),
			border-color 0.35s ease,
			background 0.35s ease,
			box-shadow 0.35s ease;
	}

	.security-card:hover {
		transform: translateY(-7px);
		border-color: #789b65;
		background: #24372b;
		box-shadow: 0 20px 45px rgb(0 0 0 / 16%);
	}

	.card-top {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 12px;
		margin-bottom: 27px;
	}

	.card-icon {
		display: grid;
		width: 44px;
		height: 44px;
		place-items: center;
		border-radius: 12px;
		background: #304b37;
		color: #b8ef6b;
		font-size: 1.35rem;
		transition:
			transform 0.35s ease,
			background 0.35s ease,
			color 0.35s ease;
	}

	.security-card:hover .card-icon {
		transform: rotate(-8deg) scale(1.1);
		background: #b8ef6b;
		color: #17251e;
	}

	.card-category {
		color: #b8ef6b;
		font-size: 0.66rem;
		font-weight: 700;
		letter-spacing: 0.12em;
	}

	.security-card h3 {
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.35rem;
		letter-spacing: -0.035em;
	}

	.security-card > p {
		margin-top: 12px;
		color: #b2c0b5;
		font-size: 0.88rem;
		line-height: 1.75;
	}

	.token-list {
		margin-top: 28px;
		border-top: 1px solid #3a4c3f;
	}

	.token-list > div {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 12px;
		padding: 14px 0;
		border-bottom: 1px solid #3a4c3f;
		transition:
			padding 0.3s ease,
			background 0.3s ease;
	}

	.token-list > div:hover {
		padding-inline: 9px;
		background: rgb(184 239 107 / 5%);
	}

	.token-list span {
		color: #b2c0b5;
		font-size: 0.85rem;
	}

	.token-list strong {
		color: #b8ef6b;
		font-size: 0.85rem;
		transition: transform 0.3s ease;
	}

	.token-list > div:hover strong {
		transform: translateX(-3px);
	}

	.card-footnote {
		display: block;
		margin-top: 14px;
		color: #89998d;
		font-size: 0.7rem;
	}

	.encryption-item {
		display: flex;
		align-items: center;
		gap: 16px;
		margin-top: 26px;
		padding: 17px;
		border: 1px solid #3a4c3f;
		border-radius: 12px;
		transition:
			transform 0.3s ease,
			border-color 0.3s ease,
			background 0.3s ease;
	}

	.encryption-item:hover {
		transform: translateX(5px);
		border-color: #789b65;
		background: #263b2d;
	}

	.encryption-symbol {
		display: grid;
		width: 48px;
		height: 48px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 12px;
		background: #304b37;
		color: #b8ef6b;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 0.9rem;
		font-weight: 700;
		transition:
			transform 0.35s ease,
			background 0.35s ease;
	}

	.encryption-item:hover .encryption-symbol {
		transform: rotate(-6deg) scale(1.08);
		background: #b8ef6b;
		color: #17251e;
	}

	.encryption-item strong,
	.encryption-item span {
		display: block;
	}

	.encryption-item strong {
		font-size: 0.95rem;
	}

	.encryption-item span {
		margin-top: 5px;
		color: #b2c0b5;
		font-size: 0.78rem;
		line-height: 1.5;
	}

	.middleware-list {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 20px 15px;
		margin-top: 28px;
	}

	.middleware-list > div {
		display: flex;
		align-items: flex-start;
		gap: 10px;
		min-width: 0;
		transition: transform 0.3s ease;
	}

	.middleware-list > div:hover {
		transform: translateX(5px);
	}

	.middleware-dot {
		width: 7px;
		height: 7px;
		flex-shrink: 0;
		margin-top: 6px;
		border-radius: 50%;
		background: #b8ef6b;
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
	}

	.middleware-list > div:hover .middleware-dot {
		transform: scale(1.5);
		box-shadow: 0 0 10px rgb(184 239 107 / 55%);
	}

	.middleware-list strong,
	.middleware-list small {
		display: block;
		overflow-wrap: anywhere;
	}

	.middleware-list strong {
		font-size: 0.83rem;
	}

	.middleware-list small {
		margin-top: 5px;
		color: #aab9ad;
		font-size: 0.72rem;
		line-height: 1.5;
	}

	.approval-flow {
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 9px;
		margin-top: 38px;
	}

	.approval-step {
		display: flex;
		flex: 1;
		flex-direction: column;
		gap: 12px;
		min-width: 0;
	}

	.approval-step span {
		display: grid;
		width: 32px;
		height: 32px;
		place-items: center;
		border: 1px solid #526758;
		border-radius: 50%;
		color: #b8ef6b;
		font-size: 0.72rem;
		transition:
			transform 0.3s ease,
			background 0.3s ease,
			border-color 0.3s ease;
	}

	.approval-step:hover span {
		transform: scale(1.12);
		border-color: #b8ef6b;
		background: #304b37;
	}

	.approval-step strong {
		font-size: 0.77rem;
		line-height: 1.5;
	}

	.approval-step.approved span {
		border-color: #b8ef6b;
		background: #b8ef6b;
		color: #17251e;
	}

	.approval-step.approved:hover span {
		background: #b8ef6b;
	}

	.approval-arrow {
		color: #8ea394;
	}

	.security-principle {
		display: flex;
		align-items: flex-start;
		gap: 22px;
		margin-top: 30px;
		padding: 30px;
		border: 1px solid #526b53;
		border-radius: 18px;
		background: #263a2c;
		transition:
			transform 0.35s ease,
			border-color 0.35s ease,
			background 0.35s ease,
			box-shadow 0.35s ease;
	}

	.security-principle:hover {
		transform: translateY(-5px);
		border-color: #8eae75;
		background: #2b4131;
		box-shadow: 0 18px 40px rgb(0 0 0 / 12%);
	}

	.principle-icon {
		display: grid;
		width: 48px;
		height: 48px;
		flex-shrink: 0;
		place-items: center;
		border-radius: 13px;
		background: #3b563d;
		color: #b8ef6b;
		font-size: 1.5rem;
		transition:
			transform 0.35s ease,
			background 0.35s ease;
	}

	.security-principle:hover .principle-icon {
		transform: rotate(10deg) scale(1.08);
		background: #b8ef6b;
		color: #17251e;
	}

	.security-principle > div:last-child > span {
		color: #b8ef6b;
		font-size: 0.67rem;
		font-weight: 700;
		letter-spacing: 0.12em;
	}

	.security-principle h3 {
		margin-top: 10px;
		font-family: 'Space Grotesk', sans-serif;
		font-size: 1.35rem;
	}

	.security-principle p {
		max-width: 750px;
		margin-top: 10px;
		color: #b2c0b5;
		font-size: 0.88rem;
		line-height: 1.75;
	}

	.section-note {
		margin-top: 30px;
		color: #89998d;
		font-size: 0.75rem;
		line-height: 1.6;
	}

	@media (max-width: 760px) {
		.security-grid {
			grid-template-columns: 1fr;
		}

		.security-section {
			padding: 80px 0;
		}
	}

	@media (max-width: 600px) {
		.section-container {
			width: calc(100% - 40px);
		}

		.security-card {
			padding: 23px;
		}

		.middleware-list {
			grid-template-columns: 1fr;
		}

		.security-principle {
			padding: 22px;
		}

		.approval-flow {
			align-items: flex-start;
		}

		.approval-step strong {
			font-size: 0.7rem;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.security-card,
		.card-icon,
		.token-list > div,
		.token-list strong,
		.encryption-item,
		.encryption-symbol,
		.middleware-list > div,
		.middleware-dot,
		.approval-step span,
		.security-principle,
		.principle-icon {
			transition: none !important;
			transform: none !important;
		}
	}
</style>
