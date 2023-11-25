<script lang="ts">
    export let data;
    const item = data.items.find(obj => obj.slug === data.slug)
</script>

<h1>{item?.title}</h1>