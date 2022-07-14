# Dimipay total sales amount spreadsheet

## install

```
yarn install
```

## cli

```
yarn cli
```

### cli usage

```
Usage: cli [options]

Options:
  -y, --year <number>    target year (default: current year)
  -m, --month <number>   target month (default: current month)
  -o, --output <string>
  --no-separator         separate amount with comma
  -f, --force            overwrite output file (default: false)
  --skip-zero            skip zero amount (default: false)
  -h, --help             display help for command
```

### example

```
yarn cli -m 6 -f --skip-sero
```

outpue default is `{year}-{month} sales amount.xlsx`

## API

import `Generator`

```js
import Generate from '.';
const generator = new Generator();
```

the only allowed method is `generate`

```ts
generator.generate({
  year?: number;
  month?: number;
  output?: string;
  separator?: boolean;
  skipZero?: boolean;
  force?: boolean;
})
```

## result

| 날짜       | 판매 금액 |
| ---------- | --------- |
| 2020-06-23 | 425,000   |
| 2020-06-24 | 425,000   |
| 2020-06-25 | 425,000   |
| 2020-06-26 | 425,000   |
| 2020-06-27 | 320,000   |
