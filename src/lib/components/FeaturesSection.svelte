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
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-30s-natural-smile--1766102994687-0.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-40s-friendly-express-1766102999272-1.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-50s-confident-smil-1766103002947-2.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-20s-approachable-smi-1766103007202-3.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-40s-warm-expressio-1766103010615-4.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-30s-genuine-smile-pr-1766103013458-5.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-man-in-his-50s-confident-expres-1766103016401-6.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-woman-in-her-30s-friendly-smile-1766103019892-7.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-man-in-his-60s-wise-expression--1766103144045-0.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-woman-in-her-20s-bright-smile-m-1766103147508-1.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-40s-professional-s-1766103149882-2.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-50s-approachable-exp-1766103153214-3.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-50s-professional-s-1766103574032-0.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-her-20s-cheerful-look-ca-1766103578108-1.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-man-in-his-40s-warm-expression--1766103580343-2.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-woman-in-her-30s-genuine-smile--1766103583142-3.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-40s-confident-look-1766103586124-4.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-50s-distinguished-sm-1766103589412-5.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-man-in-his-30s-friendly-express-1766103514572-0.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-woman-in-her-20s-bright-smile-m-1766103518144-1.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-woman-in-her-50s-warm-demeanor--1766103521280-2.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-man-in-his-40s-approachable-exp-1766103523956-3.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-american-man-in-his-20s-energetic-smile--1766103526543-4.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
            <div class="aspect-square bg-gray-200 overflow-hidden rounded-sm">
                <img src="/generated/image-european-woman-in-her-40s-professional-s-1766103529170-5.webp" alt="Customer" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-300" />
            </div>
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
