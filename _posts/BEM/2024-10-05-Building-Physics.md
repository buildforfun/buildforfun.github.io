---
layout: post
categories: [ sustainability]
title:  "Building Physics"
date:   2024-10-05 07:00:00
---

## Introduciton to Building Physics

Building physicists apply physics to buildings to enhance the energy efficiency, thermal performance, and sustainability of buildings. Building Physics can be broken into:
- energy and heat
- light
- sound
- air movement
- moisture

## Energy and thermodynamics
What is energy? Energy is the ability to do work. It's measured in joules. There are different forms of energy:
- Kinetic energy
- Thermal energy
- Potential energy
- Chemical energy
- Nuclear energy
- Electrical energy

In building physics, the focus is thermal energy. What is thermal energy? Thermal energy is the vibrations of atoms in a substance due to the rise of temperature. There are three main modes of heat/thermal energy transfer in buildings:
1. Conduction: heat transfer via solids
2. Convection: heat transfer via fluid movement
3. Radiation: heat transfer vis EM waves

This falls under a major branch in physics called thermodynamics which looks at heat, work, temperature, and their relation to energy and entropy. It focuses on how thermal energy is converted to and from other forms of energy, and how it affects matter. Thermodynamics is governmed by 4 laws:
1. zeroth law of thermodynamics: if A and C are in equilibrium with B then A and C are also in equilibrium
2. first law of thermodynamics: energy cannot be created or destroyed, it can only be transferred
3. second law of thermodynamics: heat does not transfer from cold to hot
4. third law of thermodynamics: as temp approaches absolute zero, entropy goes to zero

### The three modes of heat transfer
### Conduction
Conduction is a fundamental mode of heat transfer that occurs when materials are in direct contact. In this process, kinetic energy is transferred from the hotter particles - those with more vibrational energy to adjacent particles with less energy.

Solids are more effective at transferring heat via conduction due to their closely packed atoms. In contrast, conduction in liquids and gases is more random because of the greater spacing between particles.
![alt text](/assets/image-5.png)

Thermal conductivity is the ability of a material to transmit heat by conduction. Generally, the order from lowest to highest thermal conductivity is gases, thermal insulators, liquids, non-metal solids, and metals.

Fourier’s law is the governing equation for heat transfer by conduction which says heat flux is proportional to thermal gradient across the material.

### Convection
Convection is the mechanism of heat transfer due to the movement of particles and the random collision between particles due to the movement. There are two main types of convection:
1. Natural convection: Where the particles move due to a natural process like buoyancy.
2. Forced convection: Where particles move due to a device like a fan or a pump.<br>
   ![alt text](/assets/image-7.png){:width="20%"}

A radiator warms up due to hot water being passed through the pipework by a pump from the boiler, this is an example of forced convection. The radiator then transfers heat to the air from the hot surface on the radiator. As the temperature of air near the radiator increases the density decreases and the air rises due to buoyancy, this is an example of natural convection.<br>
    ![alt text](/assets/image-8.png){:width="20%"}<br>

The rate of heat transfer is described by Newton’s law of cooling. The convective surface convective surface heat transfer coefficient from lowest to highest is: natural convection in gasses, (natural convection in liquids, forced convection in gases and forced convection in liquids are similar but forced convection with liquids could be higher), boiling and condensation has the highest.
   ![alt text](/assets/image-9.png){:width="20%"}<br>


### Radiation
When particles with energy above absolute zero energy move (thermal energy) this causes electromagnetic waves (EM) waves to be released; this is  thermal radiation. We can first look at black bodies as they are an idealised form of bodies that absorb all radiation.
![alt text](/assets/image-10.png){:width="40%"}<br>

A black body emitter that has a higher temperature emits with a higher emissive power and radiates at shorter wavelengths.
![alt text](/assets/image-11.png){:width="20%"}<br>

In reality, some bodies are absorbed, transmitted and reflected. To capture the surface property of a material, emissivity is used in the formula. Black bodies have an emissivity of 1.<br>
![alt text](/assets/image-12.png){:width="20%"}<br>

### What Happens When More Heat Is Added To A System?

When heat is added to a system, two main things can change: the sensible heat and the latent heat.

Sensible heat is when the temperature rises, but there is no change in system volume or pressure.
The kinetic energy of the particles increases. The sensible heat can be calculated using the system mass, specific heat capacity and the change in temperature.

When more heat is added to a system the state of the system changes, this is where the energy is stored or released this is described as latent heat.
This is where internal energy or potenital energy of the system changes. 

![alt text](/assets/image-3.png){:width="60%"}<br>

The graph below shows the various processes by which latent heat can occur. It’s worth noting that the temperature during latent heat changes does not change as shown by the horizontal lines in the graph below.

![alt text](/assets/image-4.png){:width="60%"}<br> 

The application to building is mostly:
- Sensible cooling/heating affects air temperature. Heat transfer through the building envelope is primarily sensible heat
- Latent cooling/heating affects moisture content/humidity. Moisture management in the envelope involves latent heat processes

## Laws of thermodynamics
1. Zeroth Law: 
   - thermal equilibrium.
   - If A and C are in equilibrium with B then A and C are also in equilibrium
2. First Law:
   - energy cannot be created or destroyed, it can only be transferred
   - ΔU = Q - W
     - Where ΔU is change in internal energy, Q is heat added to the system, and W is work done by the system.
   - The first law of thermodynamics states that the change of internal energy (U) is equal to the difference of the heat supplied (Q) to the system and the work done (W) by the system. Internal energy is the sum of all the mechanical energies of the particles (kinetic energy or potential energy). For example, in the left figure below, as heat is supplied to the system the internet energy of the particles increases and thus causes the piston to move up as work is done to the piston. 
   - ![alt text](/assets/image.png){:width="30%"}<br>
3. Second Law:
   - Heat goes from hot to cold via the three mechanisms: conduction, convection and radiation.
   - Natural processes tend to move towards increased entropy
   - Entropy: A measure of the disorder or randomness in a system
4. Third Law:
   - As temperature approaches absolute zero, entropy approaches a minimum value.
   - Perfect crystal at absolute zero has zero entropy.

## Heat transfer in buildings
The building envelope consists of:
- Walls
- Roof
- Windows and Doors
- Floors

Heat is lost in various ways in the building.  Walls are a significant source of heat loss in buildings, accounting for approximately 35% of total heat loss.

### Heat loss through walls
The main method of heat loss through walls is via conduction. There is some heat lost through convection as air leakage (gaps, cracks and poorly sealed walls). The choice of building materials significantly impacts a structure's thermal performance. Key thermal properties to consider include:
- Thermal conductivity: materials ability to absorb heat
- Heat capacity: amount of energy required to raise the temp of a material by 1C
- Thermal mass: capacity of a material to absorb energy. A high heat capacity is used to stabilise indoor temperatures.
- U-value: how well a building element conducts heat

![alt text](/assets/image-2.png){:width="60%"}<br>

Heat is lost from the inside air to the inside surface by convection and radiation. The heat is then transferred through the walls by conduction and then lost to external air from the external surface by convection and radiation. The surface resistance of the indoor and external walls depends on the heat flow direction. Temperature and velocity of air but it’s mainly heat flow direction. There are standard figures that can be looked up on this. The resistance of the wall itself can be found in the thickness of the wall over the thermal conductivity of the material. This can be used to calculate the total resistance and then the overall U-value called thermal transmittance. The overall heat loss rate through the building can then be calculated.

1. Inside to Wall Surface:
   - Heat is transferred from indoor air to the interior wall surface through convection and radiation.
2. Through the Wall:
   - Heat moves through the wall material by conduction.
3. Wall Surface to Outside:
   - Heat is lost from the exterior wall surface to the outdoor environment through convection and radiation.

Surface Resistance
- The surface resistance (Rsi for interior, Rse for exterior) depends primarily on:
  - Direction of heat flow
  - Air temperature
  - Air velocity
- Standard figures for surface resistances are available in building codes and thermal performance guides.

Wall Resistance
- The thermal resistance of the wall itself is calculated as:
  R = d / λ
  Where:
  - d is the thickness of the material
  - λ (lambda) is the thermal conductivity of the material

Total Thermal Resistance
- The total thermal resistance (R-value) is the sum of all resistances:
  R_total = Rsi + R_wall + Rse

U-Value Calculation
- The overall heat transfer coefficient (U-value) is the reciprocal of the total thermal resistance:
  U = 1 / R_total

Heat Loss Rate Calculation
- The heat loss rate through a building element can be calculated using:
  Q = U  A  ΔT
  Where:
  - Q is the heat loss rate (W)
  - U is the U-value (W/m²K)
  - A is the area of the building element (m²)
  - ΔT is the temperature difference between inside and outside (K)

Lower losses:
- Materials with low thermal conductivity and high heat capacity can reduce heat loss through walls
- High thermal mass can help stabilise indoor temperatures by absorbing excess heat during the day and releasing it at night
- Lower U-values result in less heat transfer through the entire wall assembly

### Heat loss through glazing
When there is an airspace between walls, heat transfers by convection and radiation occurs in the airspace:

![alt text](/assets/image-6.png){:width="60%"}<br>

When there is a double glazing window, there is conduction through the glass and the airgap has convection, long wavelength radiation and short wavelength radiation from the sun. Windows are a significant source of heat loss in buildings, accounting for approximately 18% of total heat loss.

1. Heat loss through windows occurs in these ways:
   - Radiation: About 2/3 of energy lost from a standard window is through radiation through the glazing.
   - Conduction: Heat is conducted through the window frame and glass.
   - Convection: A small amount of heat is lost through convection within the glazing cavity.
   - Air leakage: Heat can escape through gaps around the frame and due to the window's opening method.

2. Double glazing can reduce heat loss by up to 50% compared to single glazing, while triple glazing can cut heat loss even further to around 20%.
3. The U-value measures the thermal transmittance of glazing. A lower U-value indicates better insulation.
4. The G-value measures how much solar heat is transmitted through the glazing. A lower G-value means less solar heat is transmitted.
5. Factors affecting heat loss through glazing include:
   - Type of glass (single, double, or triple pane)
   - Low-E coatings
   - Glass thickness
   - Temperature difference between inside and outside
   - Window seals
   - Gas fills between panes (e.g., argon or krypton)
6. Heat loss through windows can be calculated using the formula:
   Heat Loss = U-value x Area x ΔT
   Where ΔT is the temperature difference between inside and outside.
7. Measures to reduce heat loss through glazing include:
   - Installing double or triple glazing
   - Adding secondary glazing
   - Using heavy curtains
   - Sealing gaps and cracks around window frames

### Heat loss through roofs
Heat loss through the roof occurs primarily due to convection, as warm air rises and escapes through any gaps or poorly insulated area. Approximately 25% of a home's heat is lost through an uninsulated roof.

![alt text](/assets/image-1.png){:width="70%"}<br>


### What are thermal bridges?

Thermal bridges are areas where there is a significant change in heat transmittance. There are two types of thermal bridges:
Linear thermal bridge
- Heat transmittance can be shown as a line e.g a building edge which shows heat flowing in 2 directions.
Point thermal bridge
- Heat transmittance can be shown as a point e.g a corner which shows heat flowing in 3 directions.

![alt text](/assets/image-13.png){:width="40%"}<br>

## Infiltration and Ventilation

Infiltration and ventilation are critical factors in building energy modelling that determine the air flow patterns and energy losses in a building.

Infiltration refers to the uncontrolled flow of outdoor air into a building through cracks, gaps, and other unintentional openings in the building envelope. This air leakage is driven by pressure differences caused by wind, temperature differences, and other factors. Infiltration can lead to significant energy losses, as the outdoor air must be heated or cooled to maintain indoor comfort. To model infiltration, building energy models typically use an air tightness measurement, such as the air changes per hour (ACH) at a reference pressure (e.g. 50 Pa). This measured air tightness is then adjusted using empirical divisors to estimate the average infiltration rate under normal driving pressures. The models account for factors like building type, number of stories, and sheltering to determine the appropriate divisor. 

Ventilation, on the other hand, refers to the controlled flow of outdoor air into a building, often through mechanical systems or intentional openings like windows. Ventilation is necessary to provide fresh air and maintain indoor air quality. Building energy models account for both the uncontrolled infiltration and the controlled ventilation to determine the overall air change rate and associated heating/cooling loads. 

### Infiltration

Infiltration is the uncontrolled air leakage through the building envelope. 
Infiltration heat loss (Hi) accounts for uncontrolled air leakage through cracks and gaps. 
The modeling approach you described is commonly used:
1. Measure air tightness (e.g., ACH50) e.g blower door test or pulse test
2. Apply empirical divisors to estimate average infiltration rate
3. Account for building characteristics (type, height, sheltering)

The infiltration rate can be further refined using models that account for wind speed and temperature difference. Using:
- Simple formula:
  - Hi = ρ  Cp  Qi  ΔT
  Where:
   - Qi is the infiltration rate

### Ventilation
Ventilation is the controlled introduction of outdoor air. 
It can be natural (through windows and other openings) or mechanical (through HVAC systems).
Ventilation heat loss (Hv) is calculated based on the volume of air exchanged.

Natural Ventilation
 - Natural ventilation relies on pressure differences caused by wind and temperature gradients to move air through a building. Types include:
   - single sided (openings on one side of a space)
   - cross ventilation (opposite sides of a space)
   - stack ventilation(temperature differences to create airflow)
     - Warm air rises and exits through high openings, drawing in cooler air at lower levels
 - Mechananical ventilation:
   - Mechanical Ventilation use fans to control airflow. They can provide more consistent ventilation rates but require energy to operate.
 - Simple formula:
   - Hv = ρ  Cp  Qv  ΔT
   Where:
   - ρ is air density
   - Cp is specific heat capacity of air
   - Qv is the ventilation rate
   - ΔT is the temperature difference
  
## Total Heat Losses
Your formula for total heat loss is correct:
H = Ht + Hv + Hi
Where:
H = overall heat loss (W)
Ht = heat loss due to transmission through building envelope 
Hv = heat loss due to ventilation
Hi = heat loss due to infiltration

Let's expand on each component:
1. Transmission Heat Loss
2. Ventilation Heat Loss
3. Infiltration Heat Loss

Additional considerations:
- Ground heat losses are often calculated separately using methods like the ASHRAE slab-on-grade perimeter method
- Solar gains and internal gains (from occupants, equipment, etc.) should be subtracted from the total heat loss to determine the net heating load

Passive house is an optional standard for energy efficienct buildings.
There are specific requirements to be classed as a Passive house, however this is beyond the scope of this post.
For more information on this please visit the Passive House website which can be accessed through this [link](https://passivehouse.com/).


