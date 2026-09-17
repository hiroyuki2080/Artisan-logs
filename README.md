# Hiroyuki
Artisan `.alog` files from a Quest M3s modified to log exhaust CO and drop when CO hits a set limit.
This is a data dump plus an open question, not a finished method paper.

Question:

> If CO tracks roast chemistry, why doesn't the same ppm give the same
> color on different coffees?

## Why these files exist

JP6173395 / US10278406 treats in-roast CO as a roast-degree signal
and says the relationship is roughly independent of origin.

I ran that idea on a Quest M3s.

What worked:
- CO can be logged in Artisan
- a numeric limit can trigger drop
- the same ppm bands can be reused across coffees

What did not line up:
- visual Agtron card
- L* after grinding

Same drop CO ≠ same color. That gap is the point of this repo.

## Machine

- Roaster: Quest M3s
- Charge: 200 g (see each `.alog`)
- Control / log: Artisan
- Extra channel: CO GAS
- Drop: CO GAS Limit
- Also logged: ET, BT, heater, fan, room temp / humidity when noted

CO is a concentration. Probe placement, airflow, chaff, and leaks
change the number. Compare logs before comparing ppm values.

## Logs

All roast recipes and curves are in the `.alog` files.
