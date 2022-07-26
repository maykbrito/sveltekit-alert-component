<script>
    import { fade } from 'svelte/transition'
    import { ALERT_TYPES, alertMessage, alertType} from './alert-store'

    $: bgClass = () => {
        if ($alertType === ALERT_TYPES.SUCCESS) {
            return 'bg-green-100'
        } else if ($alertType === ALERT_TYPES.DANGER) {
            return 'bg-red-100'
        } else {
            return 'bg-blue-100' 
        }
    }
</script>

<div class="h-10 mb-6">
    {#if $alertMessage}
        <span transition:fade="{{duration: 500}}"
            class={`text-gray-900 text-center rounded-md p-4 mb-4 ${bgClass() }`}>
            {$alertMessage}
        </span>
    {/if}
</div>