# Biomes:

* Ice 
* Tropical
* Mountains
* Desert
* Ocean

We'll model the state of each biome and the weather moving between them.

## 1. Core State Variables

Each biome i is characterized by two primary state variables at a given time t:

* Temperature (T_i(t)): Measured in arbitrary units (e.g., °C).
* Moisture (M_i(t)): Measured as a percentage (0-100%) or a unitless "humidity index" (0.0 to 1.0).

## 2. Biome "Ideal" States and Homeostasis

Each biome has an "ideal" or equilibrium state that it naturally tends toward without external influence (weather from neighbors). This represents the local geography and albedo.

### Ice Biome: 
Very cold, moderate moisture (locked in ice).
  * T_ideal_ice = -10
  * M_ideal_ice = 60
  
### Desert Biome: 
Very hot, very dry.
  * T_ideal_desert = 35
  * M_ideal_desert = 10
  
### Tropical Biome: 
Warm, very wet.
  * T_ideal_tropical = 28
  * M_ideal_tropical = 85
  
### Mountain Biome: 
Cold, variable moisture. Let's assume moderately dry.
  * T_ideal_mountain = 5
  * M_ideal_mountain = 40

   
The biome will naturally drift toward its ideal state at a certain rate:
* ΔT_i = α_T * (T_ideal_i - T_i(t))
* ΔM_i = α_M * (M_ideal_i - M_i(t))
