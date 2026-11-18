
<section class="events-section" id="eventos">
  <div class="section-container">
    <div class="section-heading">
      <span class="eyebrow">03 — EVENTOS E PROCESSAMENTO</span>
      <h2>Desacoplar processos.<br /><span>Manter tudo em movimento.</span></h2>
      <p>
        O TherapistFriend utiliza eventos de domínio e processamento assíncrono
        para organizar operações que não precisam bloquear a resposta principal
        da aplicação.
      </p>
    </div>

    <div class="concept">
      <div class="concept-icon">↗</div>
      <div>
        <strong>Do acontecimento ao processamento</strong>
        <p>
          Um registro de humor pode iniciar outras operações sem concentrar
          toda a lógica em uma única requisição.
        </p>
      </div>
    </div>

    <div class="flow">
      <div class="flow-step">
        <span class="step-number">01</span>
        <div class="step-icon">☺</div>
        <h3>Registro de humor</h3>
        <p>O paciente registra seu estado emocional na plataforma.</p>
        <span class="step-tag">Ação do usuário</span>
      </div>

      <div class="flow-connector">
        <span>→</span>
        <small>Evento</small>
      </div>

      <div class="flow-step">
        <span class="step-number">02</span>
        <div class="step-icon">⚡</div>
        <h3>Domain Events</h3>
        <p>O acontecimento permite acionar operações relacionadas sem acoplar diretamente seus módulos.</p>
        <span class="step-tag">Desacoplamento</span>
      </div>

      <div class="flow-connector">
        <span>→</span>
        <small>Enfileiramento</small>
      </div>

      <div class="flow-step">
        <span class="step-number">03</span>
        <div class="step-icon">◈</div>
        <h3>Redis + BullMQ</h3>
        <p>O processamento é encaminhado para execução assíncrona.</p>
        <span class="step-tag">Fila de tarefas</span>
      </div>

      <div class="flow-connector">
        <span>→</span>
        <small>Processamento</small>
      </div>

      <div class="flow-step">
        <span class="step-number">04</span>
        <div class="step-icon">✳</div>
        <h3>Análise por IA</h3>
        <p>O microsserviço textual processa as informações e gera cards relacionados ao humor.</p>
        <span class="step-tag">Inteligência artificial</span>
      </div>
    </div>

    <div class="realtime">
      <div class="realtime-line"></div>
      <div class="realtime-content">
        <div class="realtime-icon">⌁</div>
        <div>
          <span class="realtime-label">ATUALIZAÇÃO EM TEMPO REAL</span>
          <h3>Socket.IO</h3>
          <p>
            Após o processamento, os resultados são disponibilizados na
            interface do paciente por meio de comunicação em tempo real,
            sem depender de uma atualização manual da página.
          </p>
        </div>
        <div class="realtime-status">
          <span></span>
          Comunicação em tempo real
        </div>
      </div>
    </div>

    <div class="principles">
      <div>
        <span class="principle-number">01</span>
        <strong>Desacoplamento</strong>
        <p>Separação entre o acontecimento e as operações que reagem a ele.</p>
      </div>
      <div>
        <span class="principle-number">02</span>
        <strong>Assincronismo</strong>
        <p>Processamentos em segundo plano, sem bloquear o fluxo principal.</p>
      </div>
      <div>
        <span class="principle-number">03</span>
        <strong>Tempo real</strong>
        <p>Entrega dos resultados à interface por comunicação via Socket.IO.</p>
      </div>
    </div>

    <p class="section-note">
      Representação conceitual do fluxo implementado. Os eventos, filas e
      responsabilidades devem ser interpretados conforme a organização
      efetiva dos módulos da aplicação.
    </p>
  </div>
</section>

<style>
  .events-section {
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
    margin-bottom: 58px;
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

  .concept {
    display: flex;
    align-items: center;
    gap: 20px;
    max-width: 720px;
    margin-bottom: 42px;
    padding: 22px;
    border: 1px solid #dce9dc;
    border-radius: 16px;
    background: #edf6ec;
  }

  .concept-icon {
    display: grid;
    width: 46px;
    height: 46px;
    flex-shrink: 0;
    place-items: center;
    border-radius: 13px;
    background: #d7f2d2;
    color: #267c3d;
    font-size: 1.5rem;
  }

  .concept strong {
    font-size: 0.95rem;
  }

  .concept p {
    margin-top: 5px;
    color: #68756c;
    font-size: 0.88rem;
    line-height: 1.6;
  }

  .flow {
    display: grid;
    grid-template-columns: 1fr auto 1fr auto 1fr auto 1fr;
    align-items: stretch;
    gap: 12px;
  }

  .flow-step {
    position: relative;
    min-width: 0;
    padding: 24px 19px;
    border: 1px solid #e1e9df;
    border-radius: 16px;
    background: #fff;
  }

  .step-number {
    color: #a1aaa1;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.1em;
  }

  .step-icon {
    display: grid;
    width: 48px;
    height: 48px;
    margin: 24px 0 20px;
    place-items: center;
    border-radius: 14px;
    background: #e5f5df;
    color: #398c4e;
    font-size: 1.45rem;
  }

  .flow-step h3 {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 1.05rem;
    letter-spacing: -0.025em;
  }

  .flow-step p {
    min-height: 105px;
    margin-top: 10px;
    color: #68756c;
    font-size: 0.83rem;
    line-height: 1.65;
  }

  .step-tag {
    display: inline-block;
    margin-top: 15px;
    padding: 6px 9px;
    border-radius: 6px;
    background: #f0f5ef;
    color: #398c4e;
    font-size: 0.68rem;
    font-weight: 700;
  }

  .flow-connector {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 5px;
    color: #398c4e;
  }

  .flow-connector span {
    font-size: 1.4rem;
  }

  .flow-connector small {
    color: #8a968c;
    font-size: 0.62rem;
    text-align: center;
  }

  .realtime {
    position: relative;
    margin-top: 30px;
    padding: 1px;
    border-radius: 16px;
    background: linear-gradient(110deg, #398c4e, #b8ef6b);
  }

  .realtime-content {
    display: flex;
    align-items: center;
    gap: 22px;
    padding: 28px;
    border-radius: 15px;
    background: #17251e;
    color: #fff;
  }

  .realtime-icon {
    display: grid;
    width: 52px;
    height: 52px;
    flex-shrink: 0;
    place-items: center;
    border-radius: 14px;
    background: #294633;
    color: #b8ef6b;
    font-size: 1.7rem;
  }

  .realtime-label {
    color: #b8ef6b;
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.12em;
  }

  .realtime-content h3 {
    margin-top: 7px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 1.3rem;
  }

  .realtime-content p {
    max-width: 650px;
    margin-top: 8px;
    color: #b6c4b9;
    font-size: 0.88rem;
    line-height: 1.7;
  }

  .realtime-status {
    display: flex;
    align-items: center;
    gap: 9px;
    margin-left: auto;
    color: #c6d4c8;
    font-size: 0.72rem;
    white-space: nowrap;
  }

  .realtime-status span {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: #b8ef6b;
    box-shadow: 0 0 12px #b8ef6b88;
  }

  .principles {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
    margin-top: 66px;
  }

  .principles > div {
    padding-top: 20px;
    border-top: 1px solid #dce5dc;
  }

  .principle-number {
    display: block;
    margin-bottom: 18px;
    color: #398c4e;
    font-size: 0.75rem;
    font-weight: 700;
  }

  .principles strong {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 1.05rem;
  }

  .principles p {
    margin-top: 9px;
    color: #68756c;
    font-size: 0.85rem;
    line-height: 1.7;
  }

  .section-note {
    margin-top: 44px;
    color: #929c93;
    font-size: 0.75rem;
    line-height: 1.6;
  }

  @media (max-width: 900px) {
    .flow {
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .flow-connector {
      display: none;
    }

    .flow-step p {
      min-height: 75px;
    }

    .realtime-content {
      flex-wrap: wrap;
    }

    .realtime-status {
      width: 100%;
      margin-left: 74px;
    }
  }

  @media (max-width: 600px) {
    .events-section {
      padding: 80px 0;
    }

    .section-container {
      width: calc(100% - 40px);
    }

    .flow,
    .principles {
      grid-template-columns: 1fr;
    }

    .flow-step p {
      min-height: auto;
    }

    .step-icon {
      margin: 16px 0;
    }

    .concept {
      align-items: flex-start;
    }

    .realtime-content {
      align-items: flex-start;
      padding: 22px;
    }

    .realtime-status {
      margin-left: 0;
      white-space: normal;
    }
  }
</style>
