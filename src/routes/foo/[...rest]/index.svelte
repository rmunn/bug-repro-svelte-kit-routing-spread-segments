<script context="module">
    export function load({ page }) {
        console.log(page);
        return {
            props: { params: page.params }
        }
    }
</script>

<script>
    export let params;
</script>

<p>
    Rest: {params.rest}
</p>
