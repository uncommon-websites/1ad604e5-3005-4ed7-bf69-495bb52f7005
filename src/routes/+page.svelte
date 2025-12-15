<script>
    import Header from "$lib/components/Header.svelte";
    import Hero from "$lib/components/Hero.svelte";
    import Logos from "$lib/components/Logos.svelte";
    import PressCards from "$lib/components/PressCards.svelte";
    import ImpactSection from "$lib/components/ImpactSection.svelte";
    import FeaturesSection from "$lib/components/FeaturesSection.svelte";
    import EngineSection from "$lib/components/EngineSection.svelte";
    import AwardsSection from "$lib/components/AwardsSection.svelte";
    import VideoSection from "$lib/components/VideoSection.svelte";
    import PressList from "$lib/components/PressList.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class="min-h-screen bg-white font-sans text-black selection:bg-[#FF4438] selection:text-white">
    <Header />
    <main>
        <Hero />
        <Logos />
        <PressCards />
        <ImpactSection />
        <FeaturesSection />
        <EngineSection />
        <AwardsSection />
        <VideoSection />
        <PressList />
    </main>
    <Footer />
</div>

