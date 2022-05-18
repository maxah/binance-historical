# binance-historical

Utility to retrieve historical data from Binance.

![Alt Text](https://raw.githubusercontent.com/maxgfr/binance-historical/main/.github/assets/main.gif)

## Usage

### With the cli

```sh
npm install -g binance-historical
binance-historical download

# or by using npx
npx binance-historical download
```

### With the library

```ts
import { getKline, Kline } from 'binance-historical';

const result: Array<Kline> = await getKline(
  'ETHUSDT',
  '4h',
  new Date('01-09-2020'),
  new Date('01-12-2021'),
);

console.log(result);
// [
//   ...,
//   {
//     openTime: 1579953600000,
//     open: '159.30000000',
//     high: '161.00000000',
//     low: '158.70000000',
//     close: '160.41000000',
//     volume: '25015.67605000',
//     closeTime: 1579967999999,
//     quoteAssetVolume: '4001959.95527980',
//     trades: 14330,
//     takerBaseAssetVolume: '13000.12296000',
//     takerQuoteAssetVolume: '2079824.44045350',
//     ignored: '0'
//   },
//   ...
// ]
```
