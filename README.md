# IMC Prosperity 2024: trading algorithms

Trading bots from team **Happy Holiday Cruisers** for IMC Prosperity 2024, an
algorithmic trading competition. Each bot is a `Trader` class whose `run()` method
receives the simulated exchange's order books every tick and returns orders.

## Strategies

Both files trade the round-one products, AMETHYSTS and STARFRUIT, within a position
limit of 20 each:

- **AMETHYSTS:** a stable product priced around 10,000. Buy below and sell above
  that fair value.
- **STARFRUIT:** a drifting product. Track an exponential moving average of the
  price and place bids just below it and asks just above it.

`AlgoTraining1.py` and `AlgoTraining2.py` are two iterations of the same bot with
different parameters and logic.

## Running

The files import `datamodel`, the competition's own module (`OrderDepth`,
`TradingState`, `Order` and so on). They were run inside the Prosperity simulator,
so they won't run on their own without it.
