<script lang="ts">
    let activeTab: 'feedback' | 'reputation' | 'analytics' = 'feedback';

    const tabs: { id: 'feedback' | 'reputation' | 'analytics', label: string }[] = [
        { id: 'feedback', label: 'NPS Feedback' },
        { id: 'reputation', label: 'Reputation Management' },
        { id: 'analytics', label: 'AI Analytics' }
    ];

    const content = {
        feedback: {
            title: 'NPS Feedback',
            description: 'Automated NPS surveys delivered at the perfect moment after each customer interaction. Real-time alerts let you respond to concerns before they become cancellations.',
        },
        reputation: {
            title: 'Reputation Management',
            description: 'Manage your online presence across 100+ directories. Turn satisfied customers into 5-star reviews and maintain consistent brand reputation across all locations.',
        },
        analytics: {
            title: 'AI Analytics',
            description: 'Listen360 AI analyzes thousands of customer comments to identify trends, sentiment patterns, and growth opportunities — quantifying insights that drive action.',
        }
    };
</script>

<section class="py-24 max-w-[1400px] mx-auto px-6">
    <div class="grid lg:grid-cols-2 gap-16 items-center">
        <!-- Left Grid of Faces -->
        <div class="grid grid-cols-6 gap-2 opacity-50">
            {#each Array(24) as _, i}
                <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                    <img src={`https://i.pravatar.cc/150?img=${i + 10}`} alt="Face" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
                </div>
            {/each}
        </div>

        <!-- Right Content -->
        <div>
            <div class="flex flex-col gap-6 items-start">
                {#each tabs as tab}
                    <button 
                        class="text-3xl font-serif transition-colors duration-300 text-left {activeTab === tab.id ? 'text-black' : 'text-gray-300 hover:text-gray-500'}"
                        onclick={() => activeTab = tab.id}
                    >
                        {tab.label}
                    </button>
                    
                    {#if activeTab === tab.id}
                        <div class="pl-4 border-l-2 border-[#FF8300] mt-2 mb-8 animate-in fade-in slide-in-from-left-2 duration-300">
                            <p class="text-lg text-gray-600 mb-8 max-w-md">
                                {content[tab.id].description}
                            </p>
                            <a href="/" class="inline-block border border-[#FF8300] text-[#FF8300] text-[11px] font-bold tracking-widest uppercase px-8 py-4 hover:bg-[#FF8300] hover:text-white transition-colors">
                                LEARN MORE
                            </a>
                        </div>
                    {/if}
                {/each}
            </div>
        </div>
    </div>
</section>
