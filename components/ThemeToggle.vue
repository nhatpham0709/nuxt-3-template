<template>
  <div class="flex items-center">
    <Listbox
      v-if="currentStyle === 'dropdown-right-top'"
      v-model="themeSetting"
      as="div"
      class="relative flex items-center"
    >
      <ListboxLabel class="sr-only">
        {{ $t('components.theme_switcher.theme') }}
      </ListboxLabel>
      <ListboxButton
        type="button"
        class="flex dark:hidden"
        :title="$t('components.theme_switcher.change_theme')"
        @click="themeSetting = 'dark'"
      >
        <span class="flex justify-center items-center">
          <IconUil:moon />
        </span>
      </ListboxButton>
      <ListboxButton
        type="button"
        class="hidden dark:flex"
        :title="$t('components.theme_switcher.change_theme')"
        @click="themeSetting = 'light'"
      >
        <span class="flex justify-center items-center">
          <IconUil:sun />
        </span>
      </ListboxButton>
    </Listbox>
  </div>
</template>

<script lang="ts" setup>
import { Listbox, ListboxButton, ListboxLabel } from '@headlessui/vue'
import { IThemeSettingOptions } from '~/utils/theme'

// micro compiler
const props = defineProps({
  type: {
    type: String,
    default: 'dropdown-right-top',
  },
})

// state
const themeSetting = useState<IThemeSettingOptions>('theme.setting')
const currentStyle = toRef(props, 'type')
</script>
