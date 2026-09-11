---

title: IMC Prosperity 4 Trading Algorithm
summary: Trading algorithm with data visualization tools + backtester used during competition
tech_stack:
 - Python
 - Jupyter Notebooks
status: 'WIP'

links:
  - type: github
    url: https://github.com/aliu3203/prosperity4
    label: Code
---

IMC Prosperity is an algorithmic trading competition that runs over several rounds. You
upload a single Python file, it gets run against a simulated exchange, and you find out how it
did once the round closes. New products get introduced as the rounds go on, so the algorithm
has to keep growing.

Most of what I wrote is market making. Each product gets its own trader class on top of a
shared base that handles position limits, reading the order book, and packing state into the
string that gets handed back on the next tick. A few products needed something other than
quoting around a fair value, so there is an EMA based one and, for the options round, a
Black-Scholes pricer that solves for implied volatility with Newton's method.

The rest of the repo is tooling. I ran strategies through an open source backtester from the
previous year's competition so I could test against past data instead of waiting a day to
find out, and there are notebooks for reading the logs back and plotting what the algorithm
actually did.
