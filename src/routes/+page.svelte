<script>
  import Hero from "$lib/components/sections/Hero.svelte";
  import Features from "$lib/components/sections/Features.svelte";
  import PlugLogic from "$lib/components/sections/PlugLogic.svelte";
  import FinalCTA from "$lib/components/sections/FinalCTA.svelte";
  import Navbar from "$lib/components/layout/Navbar.svelte";
  import LogoSlider from "$lib/components/sections/LogoSlider.svelte";
  import Features1 from "$lib/components/sections/Features1.svelte";
  import SectionWrapper from "$lib/components/wrapper/SectionWrapper.svelte";
  import ComparisonSection from "$lib/components/sections/ComparisonSection.svelte";
  import AgentSection from "$lib/components/sections/AgentSection.svelte";
  import Planats from "$lib/components/sections/Planats.svelte";
  import Footer from "$lib/components/layout/Footer.svelte";
</script>

<Navbar />
<Hero />
<!-- <LogoSlider /> -->

<SectionWrapper>
  <ComparisonSection />
  <Features />
</SectionWrapper>

<Features1 />
<PlugLogic />
<FinalCTA />
<AgentSection />
<Planats />

<Footer />
