# Electrical

## Transformer
A transformer is used to bump up or lower energy coming into a mechanism.

### Uses
- Single phase applications: bump power up or down as needed.
- Three phase applications: can take two legs of three phase, run through a transformer, and lower energy to single phase (110V).

## Converter
A converter is used to convert single phase to three phase.

### Notes
- Single phase comes in and is converted to three phase.
- A transformer may be needed to bump 240V (three phase) to 440V.

## Relay definition
### 3 pole, double throw relay
- **3 pole** = 3 contacts on a single relay base
- **Double throw** = double acting
- A double throw means you have a common input contact supplying power to a normally open and normally closed output contact.
- A single pole contact is like a standard light switch: on or off.

## Output load note
Outputs on a Thermwood control should not be set up to handle a 24VDC, 150 mA surge suppressed solenoid load.
Use a solid state relay or a sensitive coil relay to control the solenoid.
