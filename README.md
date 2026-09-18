# Readme
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

/logs
  cerrado_350ppm.alog
  cerrado_120ppm.alog
  cerrado_40ppm.alog
  nansebo_350ppm.alog
  nansebo_120ppm.alog
  nansebo_40ppm.alog
  mandheling_350ppm.alog
  mandheling_120ppm.alog
  mandheling_40ppm.alog
  caramelado_350ppm.alog
  caramelado_120ppm.alog


Open in Artisan. Do not treat the filenames as a color scale.

## Color after the roast

Ground samples, flattened with the back of a spoon.

| Coffee | Drop CO | Agtron card (visual) | L* |
|---|---:|---:|---:|
| Cerrado Tree-Dried | 350 | 35 | 15.76 |
| Cerrado Tree-Dried | 120 | 45 | 16.56 |
| Cerrado Tree-Dried | 40 | 60 | 20.31 |
| Sidamo Nansebo Natural | 350 | 40 | 14.84 |
| Sidamo Nansebo Natural | 120 | 50 | 16.16 |
| Sidamo Nansebo Natural | 40 | 65 | 19.91 |
| Mandheling Aceh Trenggiling | 350 | 35 | 15.36 |
| Mandheling Aceh Trenggiling | 120 | 45 | 16.94 |
| Mandheling Aceh Trenggiling | 40 | 50 | 17.64 |
| Caramelado Decaf | 350 | 40 | 14.57 |
| Caramelado Decaf | 120 | 50 | 16.05 |

Agtron card and L* are not a conversion table.
At 40 ppm, Mandheling is still card 50 / L* 17.64 while Nansebo is
card 65 / L* 19.91.

## Questions worth arguing

1. Is "roast degree" chemistry, color, or the cup?
2. Is a shared CO target useful if color still needs an origin offset?
3. How much of the CO signal is bean chemistry vs chaff on the heater
   vs exhaust dilution?
4. If you already drop on BT + development time, what does CO add?
5. Should Agtron / L* stay post-roast QA only?

Disagree in Issues. Pull requests with other machines / probe
positions are more useful than theory-only comments.

## Safety

Roasted coffee can hold and later release CO.
Vent the roaster. This repo is about roast control, not exposure limits.

## References

- JP6173395B2 / US10278406B2 / WO2017033676A1
- Video example (Nansebo): https://x.com/Hiroyuki2080/status/2100643843297448175

## Logs

All roast recipes and curves are in the `.alog` files.
