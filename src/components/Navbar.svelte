<script>
    // this was fun to make
    const nav = {
        data: new Map(),
        add: function (route, ...icon) {
            icon = icon.map((e) => "fa-" + e).join(" ");
            this.data.set(route, icon);
        },
    };

    nav.add("/", "solid", "house");
    nav.add("/about", "solid", "question");
    nav.add("/past", "solid", "backward");
    nav.add("/present", "solid", "pause");
    nav.add("/future", "solid", "forward-fast");
    nav.add("https://linkedin.com/in/garry-pereira", "brands", "linkedin");
    nav.add("https://github.com/garry-pereira", "brands", "github");

    console.log(nav);
</script>

<nav class="flex justify-around">
    <ul class="flex gap-6">
        {#each [...nav.data] as [key, value]}
            <li><a href={key}><i class={"fa-solid " + value}></i></a></li>
        {/each}
    </ul>
</nav>
