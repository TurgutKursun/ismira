<script lang="ts">
    let { icon, size = "28px", padding_top = "0px", padding_bottom = "0px" } = $props()
</script>

<span class="material-symbols-outlined" 
style="font-size: {size}; padding-top: {padding_top}; padding-bottom: {padding_bottom}">{icon}</span>