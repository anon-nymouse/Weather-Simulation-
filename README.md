# Biomes:

* Ice 
* Tropical
* Mountains
* Desert
* Ocean

We'll model the state of each biome and the weather moving between them.

1. Core State Variables

Each biome i is characterized by two primary state variables at a given time t:

* Temperature (T_i(t)): Measured in arbitrary units (e.g., °C).
* Moisture (M_i(t)): Measured as a percentage (0-100%) or a unitless "humidity index" (0.0 to 1.0).
