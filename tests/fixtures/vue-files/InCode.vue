<script>
import { useI18n } from 'vue-i18n';

export default {
  name: 'ex3',
  data () {
    return {
      translation: $t('header.title'),
    }
  },
  setup () {
    const { t } = useI18n();

    const title = t('header.title');

    const dynamicKey = Math.round(Math.random()) ? 'key1' : 'key2';

    return {
      t,
      title,
      dynamicKey,
    }
  }
}
</script>

<template>
  <div>
    <h1>{{ title }}</h1>

    <p>{{ translation }}</p>

    <p>{{ t('header.title') }}</p>
    <p>{{ t("content.paragraph.p_1", { count: "two" }) }}</p>
    <p>{{ tc(`content.paragraph.p.2`, 2) }}</p>
  </div>
</template>
