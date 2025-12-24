<script lang="ts">
    import { Accordion } from "bits-ui";
    let { data } = $props();
</script>

<h1>---</h1>

<h1>Welcome to ESTUD!</h1>

<Accordion.Root class="w-full sm:max-w-[70%]" type="multiple">
    {#each data.info as item (item.value)}
        <Accordion.Item
            value={item.value}
            class="border-dark-10 group border-b px-1.5"
        >
            <Accordion.Header>
                <Accordion.Trigger
                    class="flex w-full flex-1 select-none items-center justify-between py-5 text-[15px] font-medium transition-all [&[data-state=open]>span>svg]:rotate-180"
                >
                    <span class="w-full text-left font-bold">
                        {item.title}
                    </span>
                    <span
                        class="hover:bg-dark-10 inline-flex size-8 items-center justify-center rounded-[7px] bg-transparent"
                    >
                        a
                    </span>
                </Accordion.Trigger>
            </Accordion.Header>
            <Accordion.Content
                class="data-[state=closed]:animate-accordion-up data-[state=open]:animate-accordion-down overflow-hidden text-sm tracking-[-0.01em]"
            >
                <div class="pb-[25px]">
                    {item.content}
                </div>
            </Accordion.Content>
        </Accordion.Item>
    {/each}
</Accordion.Root>
