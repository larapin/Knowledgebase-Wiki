# Tooling rules

## General tooling setup rules
1. Dado operations need a tool that can cut dado in two passes and should be slightly undersized.
2. Plunge drill operations need a tool diameter that exactly matches the designed hole size.
3. Pocket tool setup must match the exact diameter listed in the pocket layer name.
4. Interpolate diameter should usually be no more than twice the cutter diameter.

## Dovetail tooling
- Use a 1/4 inch tool for the male dovetail rout, with diameter set to about .249 to avoid arc error.
- Dovetail drawer box bits must match the material thickness and part number requirements.

## Secondary machining
For additional machining on parts with a finished perimeter:
- Use Scrap Part Recovery when loading the part.
- Set rotation angle to 0, 90, or 180 degrees.
- Set Collar to 0.
- Enable Nest to E.O.S.
