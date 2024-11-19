<template>
  <ul>
    <li
        @click="setCrypto('BTC')"
        :className="crypto == 'BTC' ? 'active' : ''"
    >
        Bitcoin
    </li>
    <li
        @click="setCrypto('ETH')"
        :className="crypto == 'ETH' ? 'active' : ''"
    >
        ETH
    </li>
    <li
        @click="setCrypto('USDT')"
        :className="crypto == 'USDT' ? 'active' : ''"
    >
        USDT
    </li>
  </ul>
</template>

<script>
    export default {
        props: {
            crypto: {
                type: String,
                required: true,
            },
            setCrypto: {
                type: Function,
                required: true
            }
        },
    }
</script>

<style scoped>
    ul {
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid #000;
  }

  li {
    display: block;
    background: #1A032D;
    color: #fff;
    padding: 20px 0;
  }

  li:hover, li.active {
    background: #24043e;
    cursor: pointer;
  }
</style>
