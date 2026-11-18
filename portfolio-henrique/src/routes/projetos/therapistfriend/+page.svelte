<script lang="ts">
  import ProjectNavbar from './components/ProjectNavbar.svelte';
  import ProjectHero from './components/ProjectHero.svelte';
  import ProjectFacts from './components/ProjectFacts.svelte';
  import ChallengeSection from './components/ChallengeSection.svelte';
  import SolutionSection from './components/SolutionSection.svelte';
  import FeaturesSection from './components/FeaturesSection.svelte';

  import ArchitectureSection from './components/ArchitectureSection.svelte';
  import EventsSection from './components/EventsSection.svelte';
  import SecuritySection from './components/SecuritySection.svelte';
  import AiSection from './components/AiSection.svelte';
  import ResultsSection from './components/ResultsSection.svelte';

  import TechnologiesSection from './components/TechnologiesSection.svelte';
  import LearningSection from './components/LearningSection.svelte';
  import ProjectFooter from './components/ProjectFooter.svelte';
</script>

<svelte:head>
  <title>TherapistFriend — Projeto | Henrique</title>

  <meta
    name="description"
    content="Conheça o desenvolvimento do TherapistFriend, uma plataforma web que conecta pacientes e profissionais da saúde mental."
  />
</svelte:head>

<div class="project-page">
  <ProjectNavbar />

  <main>
    <ProjectHero />
    <ProjectFacts />

    <ChallengeSection />
    <SolutionSection />
    <FeaturesSection />

    <ArchitectureSection />
    <EventsSection />
    <SecuritySection />
    <AiSection />

    <ResultsSection />
    <TechnologiesSection />
    <LearningSection />
  </main>

  <ProjectFooter />
</div>

<style>
  .project-page {
    --tf-green: #0fd850;
    --tf-yellow: #f9f047;
    --tf-blue: #a8d8ea;
    --tf-soft: #e0ffe0;
    --tf-ink: #17251e;
    --tf-muted: #66766c;

    min-height: 100vh;
    background: #f7faf6;
    color: var(--tf-ink);
    font-family: 'DM Sans', sans-serif;
  }
</style>