<script lang="ts">
    let activeTab: 'clinicians' | 'revenue' | 'nurses' = 'clinicians';

    const tabs: { id: 'clinicians' | 'revenue' | 'nurses', label: string }[] = [
        { id: 'clinicians', label: 'Clinicians' },
        { id: 'revenue', label: 'Revenue Cycle' },
        { id: 'nurses', label: 'Nurses' }
    ];

    const content = {
        clinicians: {
            title: 'Clinicians',
            description: 'Contextually aware, clinically useful, and billable AI-generated notes — in real time',
        },
        revenue: {
            title: 'Revenue Cycle',
            description: 'Streamline coding and billing with AI that understands clinical context and documentation requirements.',
        },
        nurses: {
            title: 'Nurses',
            description: 'Reduce documentation burden and focus more on patient care with automated nursing notes.',
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
                        <div class="pl-4 border-l-2 border-[#FF4438] mt-2 mb-8 animate-in fade-in slide-in-from-left-2 duration-300">
                            <p class="text-lg text-gray-600 mb-8 max-w-md">
                                {content[tab.id].description}
                            </p>
                            <a href="/" class="inline-block border border-[#FF4438] text-[#FF4438] text-[11px] font-bold tracking-widest uppercase px-8 py-4 hover:bg-[#FF4438] hover:text-white transition-colors">
                                LEARN MORE
                            </a>
                        </div>
                    {/if}
                {/each}
            </div>
        </div>
    </div>
</section>
