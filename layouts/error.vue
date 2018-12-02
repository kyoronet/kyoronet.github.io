<template>
  <v-container
    fluid
    fill-height
  >
    <v-layout
      align-center
      justify-center
    >
      <div class="text-md-center">

        <h1>
          ページが見つかりません <v-icon x-large>sentiment_very_dissatisfied</v-icon>
        </h1>
        <h2 class="my-3 headline ">お探しのページは、すでに削除されたか存在しない可能性があります。</h2>
        <h2 class="my-3 headline ">アドレスが間違っていないか、ご確認ください。</h2>
      </div>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  props: {
    error: {
      type: String,
      required: true
    }
  }
}
</script>
