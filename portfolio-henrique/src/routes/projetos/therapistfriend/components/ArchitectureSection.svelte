<script lang="ts">
  import { reveal } from '#lib/actions/reveal.ts';

</script>

<section class="architecture-section" id="arquitetura"  use:reveal>
  <div class="container">
    <div class="section-heading">
      <span class="eyebrow">03 / ARQUITETURA DE SOFTWARE</span>
      <h2>
        Organização para manter
        <span>a complexidade sob controle.</span>
      </h2>
      <p>
        O backend foi estruturado utilizando uma abordagem DDD Light,
        separando responsabilidades entre as camadas da aplicação e
        organizando as funcionalidades em módulos de negócio.
      </p>
    </div>

    <div class="architecture-layout">
      <div class="architecture-diagram">
        <div class="diagram-label">ESTRUTURA DO BACKEND</div>

        <div class="layer api">
          <div class="layer-icon">01</div>
          <div class="layer-content">
            <span>CAMADA DE ENTRADA</span>
            <strong>Interface</strong>
            <p>Rotas, controllers e comunicação HTTP</p>
          </div>
          <span class="folder">src/interface</span>
        </div>

        <div class="layer-connector">
          <span></span>
          <small>ENCAMINHAMENTO</small>
          <span></span>
        </div>

        <div class="layer application">
          <div class="layer-icon">02</div>
          <div class="layer-content">
            <span>REGRAS DE APLICAÇÃO</span>
            <strong>Application</strong>
            <p>Casos de uso, DTOs e orquestração</p>
          </div>
          <span class="folder">src/application</span>
        </div>

        <div class="layer-connector">
          <span></span>
          <small>REGRAS DE NEGÓCIO</small>
          <span></span>
        </div>

        <div class="layer domain">
          <div class="layer-icon">03</div>
          <div class="layer-content">
            <span>NÚCLEO DO NEGÓCIO</span>
            <strong>Domain</strong>
            <p>Conceitos, regras e comportamentos do domínio</p>
          </div>
          <span class="folder">src/domain</span>
        </div>

        <div class="infrastructure-area">
          <div class="infrastructure-heading">
            <span>04 / INFRAESTRUTURA</span>
            <small>IMPLEMENTAÇÕES E INTEGRAÇÕES</small>
          </div>

          <div class="infrastructure-items">
            <div>
              <strong>Database</strong>
              <span>PostgreSQL / Sequelize</span>
            </div>
            <div>
              <strong>Serviços Externos</strong>
              <span>Serviços e integrações</span>
            </div>
            <div>
              <strong>Mensageria</strong>
              <span>Redis / BullMQ</span>
            </div>
          </div>

          <span class="folder infrastructure-folder">
            src/infrastructure
          </span>
        </div>

        <div class="container-note">
          <div class="container-symbol">{'{ }'}</div>
          <div>
            <strong>setupContainer</strong>
            <p>
              Composição das dependências e configuração dos componentes
              da aplicação.
            </p>
          </div>
          <span>DEPENDENCY INJECTION</span>
        </div>
      </div>

      <aside class="architecture-aside">
        <div class="aside-number">01 — ORGANIZAÇÃO</div>
        <h3>Separação de responsabilidades.</h3>
        <p>
          Cada camada possui uma responsabilidade específica.
          Essa organização reduz o acoplamento entre as regras
          de negócio e os detalhes técnicos de implementação.
        </p>

        <div class="architecture-principles">
          <div>
            <span>01</span>
            <div>
              <strong>DDD Light</strong>
              <p>
                Organização do código orientada aos conceitos e
                responsabilidades do domínio.
              </p>
            </div>
          </div>

          <div>
            <span>02</span>
            <div>
              <strong>SOLID</strong>
              <p>
                Aplicação de princípios para favorecer coesão,
                extensibilidade e manutenção.
              </p>
            </div>
          </div>

          <div>
            <span>03</span>
            <div>
              <strong>Dependency Injection</strong>
              <p>
                Dependências configuradas centralmente, evitando
                que os casos de uso precisem instanciar diretamente
                suas implementações.
              </p>
            </div>
          </div>
        </div>
      </aside>
    </div>

    <div class="modules-area">
      <div class="modules-heading">
        <div>
          <span class="eyebrow">ORGANIZAÇÃO FUNCIONAL</span>
          <h3>Módulos do sistema</h3>
        </div>
        <p>
          As funcionalidades foram agrupadas conforme suas
          responsabilidades dentro da plataforma.
        </p>
      </div>

      <div class="module-list">
        <span>Usuário</span>
        <span>Paciente</span>
        <span>Profissional</span>
        <span>Administrador</span>
        <span>Relato</span>
        <span>Agenda</span>
        <span>Chat</span>
        <span>Sessão</span>
        <span>Relatórios</span>
        <span>Notificação</span>
        <span>Autenticação</span>
        <span>Especialidades</span>
        <span>Humor</span>
      </div>
    </div>

    <div class="architecture-observation">
      <span>NOTA DE IMPLEMENTAÇÃO</span>
      <p>
        O padrão adotado é uma abordagem DDD Light, com separação
        entre API, aplicação, domínio e infraestrutura. A estrutura
        prioriza a organização das responsabilidades sem exigir
        a implementação de todos os elementos do DDD tático.
      </p>
    </div>
  </div>
</section>

<style>
  .architecture-section {
    padding: 120px 0;
    background: #17251e;
    color: #f5f7f3;
  }

  .container {
    width: min(1180px, calc(100% - 64px));
    margin-inline: auto;
  }

  .section-heading {
    max-width: 760px;
    margin-bottom: 75px;
  }

  .eyebrow {
    color: #0fd850;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 2px;
  }

  .section-heading h2 {
    margin-top: 23px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: clamp(36px, 5vw, 58px);
    line-height: 1.15;
    letter-spacing: -2px;
  }

  .section-heading h2 span {
    display: block;
    color: #0fd850;
  }

  .section-heading > p {
    max-width: 650px;
    margin-top: 23px;
    color: #aab9ae;
    font-size: 14px;
    line-height: 1.9;
  }

  .architecture-layout {
    display: grid;
    grid-template-columns: 1.3fr .7fr;
    gap: 70px;
    align-items: center;
  }

  .architecture-diagram {
    padding: 30px;
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 12px;
    background: #1c2d23;
  }

  .diagram-label {
    margin-bottom: 25px;
    color: #82978a;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1.7px;
  }

  .layer {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px;
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 8px;
    background: #23382b;
  }

  .layer-icon {
    display: grid;
    width: 38px;
    height: 38px;
    flex-shrink: 0;
    place-items: center;
    border-radius: 7px;
    background: rgba(255,255,255,.08);
    color: #0fd850;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 12px;
    font-weight: 700;
  }

  .layer-content {
    flex: 1;
    min-width: 0;
  }

  .layer-content > span {
    color: #0fd850;
    font-size: 8px;
    font-weight: 700;
    letter-spacing: 1.2px;
  }

  .layer-content strong {
    display: block;
    margin-top: 5px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 19px;
  }

  .layer-content p {
    margin-top: 5px;
    color: #aab9ae;
    font-size: 10px;
    line-height: 1.6;
  }

  .folder {
    color: #819488;
    font-family: monospace;
    font-size: 10px;
    white-space: nowrap;
  }

  .layer-connector {
    display: flex;
    height: 42px;
    align-items: center;
    justify-content: center;
    gap: 12px;
  }

  .layer-connector span {
    width: 25px;
    height: 1px;
    background: rgba(15,216,80,.5);
  }

  .layer-connector small {
    color: #819488;
    font-size: 8px;
    letter-spacing: 1px;
  }

  .api {
    border-left: 3px solid #a8d8ea;
  }

  .application {
    border-left: 3px solid #f9f047;
  }

  .domain {
    border-left: 3px solid #0fd850;
  }

  .infrastructure-area {
    margin-top: 18px;
    padding: 20px;
    border: 1px dashed rgba(15,216,80,.4);
    border-radius: 8px;
    background: rgba(15,216,80,.035);
  }

  .infrastructure-heading {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    margin-bottom: 16px;
  }

  .infrastructure-heading span {
    color: #0fd850;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .infrastructure-heading small {
    color: #819488;
    font-size: 8px;
  }

  .infrastructure-items {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 9px;
  }

  .infrastructure-items div {
    display: flex;
    min-height: 80px;
    flex-direction: column;
    justify-content: center;
    gap: 7px;
    padding: 10px;
    border-radius: 6px;
    background: #23382b;
  }

  .infrastructure-items strong {
    font-size: 11px;
  }

  .infrastructure-items span {
    color: #aab9ae;
    font-size: 9px;
    line-height: 1.5;
  }

  .infrastructure-folder {
    display: block;
    margin-top: 15px;
    text-align: right;
  }

  .container-note {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-top: 20px;
    padding: 18px;
    border: 1px solid rgba(168,216,234,.3);
    border-radius: 8px;
    background: rgba(168,216,234,.06);
  }

  .container-symbol {
    display: grid;
    width: 42px;
    height: 42px;
    flex-shrink: 0;
    place-items: center;
    border-radius: 8px;
    background: rgba(168,216,234,.12);
    color: #a8d8ea;
    font-family: monospace;
    font-size: 20px;
  }

  .container-note > div:nth-child(2) {
    flex: 1;
  }

  .container-note strong {
    font-family: monospace;
    font-size: 13px;
  }

  .container-note p {
    margin-top: 5px;
    color: #aab9ae;
    font-size: 10px;
    line-height: 1.6;
  }

  .container-note > span {
    color: #a8d8ea;
    font-size: 8px;
    font-weight: 700;
    letter-spacing: 1px;
    text-align: right;
  }

  .architecture-aside {
    display: flex;
    flex-direction: column;
  }

  .aside-number {
    color: #819488;
    font-size: 9px;
    letter-spacing: 1.5px;
  }

  .architecture-aside h3 {
    margin-top: 20px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 30px;
    line-height: 1.25;
  }

  .architecture-aside > p {
    margin-top: 17px;
    color: #aab9ae;
    font-size: 13px;
    line-height: 1.9;
  }

  .architecture-principles {
    display: flex;
    flex-direction: column;
    gap: 25px;
    margin-top: 35px;
  }

  .architecture-principles > div {
    display: flex;
    gap: 16px;
  }

  .architecture-principles > div > span {
    color: #0fd850;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 13px;
  }

  .architecture-principles strong {
    font-size: 13px;
  }

  .architecture-principles p {
    margin-top: 7px;
    color: #aab9ae;
    font-size: 11px;
    line-height: 1.8;
  }

  .modules-area {
    margin-top: 85px;
    padding-top: 35px;
    border-top: 1px solid rgba(255,255,255,.13);
  }

  .modules-heading {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    gap: 30px;
    margin-bottom: 25px;
  }

  .modules-heading h3 {
    margin-top: 12px;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 25px;
  }

  .modules-heading > p {
    max-width: 340px;
    color: #aab9ae;
    font-size: 12px;
    line-height: 1.8;
  }

  .module-list {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .module-list span {
    padding: 11px 15px;
    border: 1px solid rgba(255,255,255,.14);
    border-radius: 5px;
    color: #dce7de;
    font-size: 11px;
  }

  .module-list span:hover {
    border-color: #0fd850;
    color: #0fd850;
  }

  .architecture-observation {
    display: flex;
    gap: 25px;
    margin-top: 45px;
    padding: 20px 22px;
    border-left: 2px solid #f9f047;
    background: rgba(249,240,71,.045);
  }

  .architecture-observation > span {
    flex-shrink: 0;
    color: #f9f047;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 1px;
  }

  .architecture-observation p {
    color: #aab9ae;
    font-size: 11px;
    line-height: 1.8;
  }

  @media (max-width: 900px) {
    .architecture-layout {
      grid-template-columns: 1fr;
      gap: 55px;
    }

    .architecture-aside {
      max-width: 650px;
    }
  }

  @media (max-width: 600px) {
    .architecture-section {
      padding: 85px 0;
    }

    .container {
      width: calc(100% - 40px);
    }

    .architecture-diagram {
      padding: 15px;
    }

    .layer {
      flex-wrap: wrap;
      padding: 14px;
    }

    .folder {
      width: 100%;
      padding-left: 54px;
    }

    .infrastructure-items {
      grid-template-columns: 1fr;
    }

    .infrastructure-heading {
      flex-direction: column;
    }

    .container-note {
      flex-wrap: wrap;
    }

    .container-note > span {
      width: 100%;
      text-align: left;
    }

    .modules-heading {
      align-items: flex-start;
      flex-direction: column;
    }

    .architecture-observation {
      flex-direction: column;
      gap: 10px;
    }
  }
</style>
