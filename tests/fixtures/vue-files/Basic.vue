<template functional>
  <div>
    <h1>{{ $t('header.title') }}</h1>
    <h1>{{ $tm('header.title2') }}</h1>
    <p>{{ $t("content.paragraph.p_1", { count: 'two' }) }}</p>
    <p>{{ $t('Key used as default translation. Second sentence.') }}</p>
    <p>{{ $tc(`content.paragraph.p.2`, 2) }}</p>
    <i18n path="content.link.a">
      <a place="link" href="#">{{ $t('content.link.b') }}</a>
    </i18n>
    <i18n-t keypath="content.link.a">
      <a place="link" href="#">{{ $t('content.link.b') }}</a>
    </i18n-t>
    <Translation keypath="content.link.a">
      <a place="link" href="#">{{ $t('content.link.b') }}</a>
    </Translation>
    <p v-t="'header.title'"></p>
    <p>{{ .t('header.title') }}</p>
  </div>
</template>
