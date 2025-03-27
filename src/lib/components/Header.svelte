<script lang="ts">
    const items =[
        {label: "Contact" , href: "/contact"},
        {label: "About", href: "/about"}
    ]
</script>

<div class="flex w-full items-center justify-center fixed top-6 self-center">
    <div class="flex flex-row items-center justify-between px-6 border rounded-sm w-fit gap-8 bg-background">
        <img src="/personalFlow.png" alt="Personal Flow" class="size-20">
        <nav>
            <ul class="flex flex-row gap-4">
                {#each items as {href, label}}
                <li>
                    <a {href}>
                        <p>{label}</p>
                    </a>
                </li>
                {/each}
            </ul>
        </nav>
    </div>
</div>