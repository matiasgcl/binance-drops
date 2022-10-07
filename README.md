# binance-drops

This script basically will compute (individually, for each coin separately) amplitude and time ellapsed for the *biggest* drop produced on a given data range, using user-defined timeframe for the candles considered.

Why this would matter?

> You can estimate relative strength for each coin on a given data range (how much/how fast did it drop? does it drop faster/slower than other coins? it is lagged? etc.)

Use: just fill the information asked when required (follow the given examples, I never handle exceptions on my own code! sorry :-))
1. How many coins you want to see (at the beginning it will tell you how many are possible, your size will tell you how many you need to see).
2. Timeframe for computations (i.e. TF for the retrieved Klines).
3. Initial date-time for computations.
4. Final date-time for computations.
5. Wait for the output.
6. Open the spreadsheet on your favorite program!

Some definitions for what you will see:
1. Time High (Open): Date-time when the candle where the top is captured OPENS.
2. Time Low (Close): Date-time when the candle where the bottom is captured CLOSES. By definition this time is ALWAYS after the top (algorithmically, we catch the low and eliminate all the candles after, so in this way we actually capture the drop from the top before the 'crash').
3. T High - T Low: The difference (measured in hours:minutes:seconds) between Time High (Open) and Time Low (Close) (>=0 by definition), the smaller the timeframe, the more precise this quantity is with respect to the exact time elapsed from top to bottom.

With respect to binance-bounces, this one computes the drop before the bottom is reached.

Example:

![Example](Example.png)
