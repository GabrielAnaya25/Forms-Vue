<template>
  <component
    :is="to ? RouterLink : 'button'"
    :to="to"
    :type="to ? undefined : type"
    :disabled="disabled"
    :class="buttonClasses"
    v-bind="attrs"
  >
    <slot />
  </component>
</template>

<script setup>
import { computed } from 'vue'
import { RouterLink } from 'vue-router'
import { useAttrs } from 'vue'

const props = defineProps({
  to: { type: [String, Object], default: null },
  variant: { type: String, default: 'primary' },
  disabled: { type: Boolean, default: false },
  type: { type: String, default: 'button' }
})

const attrs = useAttrs()

const buttonClasses = computed(() => {
  return [
    'base-button',
    `base-button--${props.variant}`,
    { 'is-disabled': props.disabled }
  ]
})
</script>

<style scoped>
.base-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  border: none;
  font-weight: 600;
  cursor: pointer;
  text-decoration: none;
  transition: transform 0.18s, box-shadow 0.18s, background 0.18s;
}

.base-button.is-disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.base-button--primary {
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
  color: var(--color-accent);
}

.base-button--accent {
  background: var(--color-accent);
  color: var(--color-primary-dark);
  border-radius: 50px;
}

.base-button--ghost {
  background: transparent;
  color: var(--color-primary);
  padding: 0.25rem 0.5rem;
}

.base-button:hover:not(.is-disabled) {
  transform: translateY(-2px);
  box-shadow: 0 8px 15px rgba(0,0,0,0.12);
}
</style>
