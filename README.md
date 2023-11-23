# Ladder

Incremental buying or selling of any crypto asset

## reason to be

Trading crypto is a game of dealing with harsh volatility and the uncertainties of timing the market. Most traders get it wrong. Throw in human emotions and all you get is anxiety rather than profits. Ladder trading is a strategy to minimize the risks and reap greater rewards. This software automates the strategy while removing human emotions.

## what is latter trading?

Ladder trading is incremental buying or selling of any crypto asset rather than opting for a single price. These incremental buy or sell orders are called ladder steps. Ladder trading will limit your losses during the market fluctuations by spreading in and out of positions. 

Should you want to exit the market and sell your asset, your average sell price will be closer to the ATH. Should you want to enter the market and buy an asset, you'll be buying dips and your average buy price will be closer to the bottom. Either way, you'll maximize your profits by pushing the average price in the desired direction.

In essence, you are executing a better dollar-cost-averaging (DCA) trading strategy where you are selling (or buying) an asset regularly, doing away with the attempt at the market timing. Because this software will slowly but surely increase your order size, your average price will be better.

## benefits

* minimize the risks
* does away with the need for timing the market
* tackling high volatility
* less anxiety

## exchanges

At the time of this writing, the software supports the following exchanges:
* [Coinbase](https://www.coinbase.com)
* [Bitstamp](https://www.bitstamp.net)
* [Binance](https://www.binance.com)

## usage

`./ladder [command] [flags]`

## commands

Use `./ladder [command] --help` for more information about a command.

Please note none of the below commands will actually place any orders unless you include `--dry-run=false` with your command line.

## sell

Usage: `./ladder sell [flags]`

| flag              | description                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------|
| --exchange        | name or code of the exchange                                                                |
| --asset           | name of the asset you will want to sell (example `BTC`)                                     |
| --quote           | name of the asset you will want to receive (example `USDT`)                                 |
| --start-at-price  | price where you will want to start selling at                                               |
| --stop-at-price   | price where you will want to stop selling                                                   |
| --start-with-size | size of your first sell order (in base asset)                                               |
| --mult            | multiplier that defines the number of orders and the distance between them (default `1.05`) |
| --size            | the quantity you will want to sell (in base asset)                                          |

## buy

Usage: `./ladder buy [flags]`

| flag              | description                                                                                 |
|-------------------|---------------------------------------------------------------------------------------------|
| --exchange        | name or code of the exchange                                                                |
| --asset           | name of the asset you will want to buy (example `BTC`)                                      |
| --quote           | name of the asset you will want to spend (example `USDT`)                                   |
| --start-at-price  | price where you will want to start buying at                                                |
| --stop-at-price   | price where you will want to stop buying                                                    |
| --start-with-size | size of your first buy order (in quote asset)                                               |
| --mult            | multiplier that defines the number of orders and the distance between them (default `1.05`) |
| --size            | the quantity you will want to buy (in quote asset)                                          |

## cancel

Usage: `./ladder cancel [flags]`

| flag              | description                  |
|-------------------|------------------------------|
| --exchange        | name or code of the exchange |
| --asset           | base asset                   |
| --quote           | quote asset                  |
| --side            | `buy` or `sell`              |
