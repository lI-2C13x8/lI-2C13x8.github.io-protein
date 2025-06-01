<script setup>
import TableRow from './TableRow.vue';
</script>

<template>
  <main class="p-a-top">
    <section class="p-a-top--mv">
      <h1>たんぱく質摂取会<br>2025年6月28日</h1>
    </section>
    <section class="p-a-top--description">
      <h2>
        <span>
          たんぱく質摂取会とは、、<br />
          乳を絞って乳を飲ませてから親(?) を食す<br />
          由緒正しき文化的交流を促進する会である。
        </span>
        <span>
          「お前らの親も所詮、<br />
          人間様の胃袋に入るんだよ」
        </span>
        <span>
          この気持ちを持って美味しい肉を求めて<br />
          島を目指す冒険譚である。
        </span>
        <span>
          美味しい緑と景色と乳に囲まれて<br />
          たんぱく質を楽しく美味しく感謝して<br />
          摂取するだ！！
        </span>
        <span>
          Come on, you too!<br />
          Let's make a fine nice bulk!
        </span>
      </h2>
    </section>
    <section class="p-a-top--schedule">
      <h3><img src="/top--schedule--title.png" alt="タイムテーブル"></h3>
      <table class="p-a-top--schedule__table">
        <TableRow title-hour="8" title-minute="00">
          ニコニコレンタカー　南武庫之荘で手続き
        </TableRow>
        <TableRow title-hour="8" title-minute="30">
          武庫之荘駅で武庫之荘組PickUp
        </TableRow>
        <TableRow title-hour="9" title-minute="00">
          武庫之荘組　尼崎出発
        </TableRow>
        <TableRow title-hour="10" title-minute="00">
          舞子駅で舞子組PickUp
        </TableRow>
        <TableRow title-hour="10" title-minute="15">本土出発</TableRow>
        <TableRow title-hour="11" title-minute="15">淡路島牧場到着</TableRow>
        <TableRow title-hour="11" title-minute="30">
          肉の下拵えは生産者（仮）と<br />ふれあいから乳を与えて乳を絞れ
        </TableRow>
        <TableRow title-hour="13" title-minute="00">
          肉はBBQにあり！！<br />たんぱく質に備えよ！！
        </TableRow>
        <TableRow title-hour="14" title-minute="30">
          撤収ーー！！<br />現状復帰！！！
        </TableRow>
        <TableRow title-hour="15" title-minute="00">淡路島牧場　出発</TableRow>
        <TableRow title-hour="15" title-minute="45">淡路島SA到着</TableRow>
        <TableRow title-hour="17" title-minute="00">舞子組　舞子駅到着</TableRow>
        <TableRow title-hour="18" title-minute="00">武庫之荘組　尼崎へ</TableRow>
      </table>
    </section>
  </main>
</template>

<style lang="scss" scoped>
.p-a-top {
  width: 100%;
  margin: 0 auto;
  background: var(--color-white);
  overflow: hidden;
  section {
    padding-left: 20px;
    padding-right: 20px;
  }
  &--mv {
    position: relative;
    background: url('/top--mv--image.jpg') no-repeat center bottom;
    padding-top: calc(100% * 360 / 402);
    background-size: 100% auto;
    h1 {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      opacity: 0;
    }
  }
  &--description {
    h2 {
      color: var(--color-black);
      font-size: 1.125rem;
      display: flex;
      flex-direction: column;
      gap: 1em;
      text-align: center;
    }
  }
  &--schedule {
    padding-top: 60px;
    padding-bottom: 60px;
    h3 {
      margin: 0 auto 30px;
      img {
        width: 100%;
        height: auto;
      }
      // width: calc(100% * 218 / 402);
    }
    &__table {
      background: url('/top--schedule--frame.png') no-repeat center top;
      background-size: 100% 100%;
      padding: 10px;
      display: flex;
      flex-direction: column;
      gap: 20px;
    } // &__table
  }
}
@media screen and (min-width: 769px) {
  .p-a-top {
    max-width: 804px;
  }
}
</style>
