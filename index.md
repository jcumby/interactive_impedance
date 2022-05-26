
## Simulator to understand impedance spectroscopy

This website provides an interactive simulation designed to explain 
electrochemical impedance spectroscopy (EIS) by analogy with water flow through pipes.
The simulation can be accessed <a href='interactive_impedance.html'>here</a>.


This project was developed at the University of Edinburgh to assist with teaching impedance spectroscopy as part of
chemistry courses in solid state materials chemistry, with a focus on battery materials.
It is released as a freely available open educational resource for use in other disciplines, however.

This project is made freely available under a CC-BY license. If you use 
this project or any of the code within it, please cite this original work!
![CC-BY logo]('by.svg')


## Electrochemical Impedance Background

### Electrical conduction

Many materials conduct electricity, for instance metals like copper or iron. How well a material
conducts electricity can be quantified by its resistance[^1], or how well it opposes the flow of charge.
The electrical current ($I$, in amps) flowing through a material is related to this resistance ($R$, in ohms) through 
the relatively simple "Ohm's law":

$$
I = \frac{V}{R}
$$

Here, $V$ is the voltage (measured in volts) across the material. For now, we can think of voltage as
the 'driving force' or 'pressure' causing the flow of current.

Although we tend to think of metals when we talk about electrical conductivity[^2], we can (in principle) measure
the resistance of anything; wood, water, silicon...! Those materials with higher resistance are typically classed
as semiconductors or insulators. While they are terrible for making wires to plug in toasters, these materials are 
very important; semiconductors form the basis of all computers, while insulators are important to make sure electrical
current goes where we want it to safely.

### Impedance

Measuring the resistance of a material when applying a constant voltage is useful, but only gives one number. While useful,
this doesn't give us much information to work out what is happen at a microscopic level during electronic conduction. 
For example, imagine a material where the charge carriers (e.g. electrons) could only move a short distance before they
stop due to an obstruction or some other reason.[^3] When you first apply a voltage to this material the electrons will move
(creating a current), but when they hit the obstruction this movement will cease (i.e. the current will become zero). Experimentally,
it is actually very difficult to measure the initial motion, so this material would probably appear to have a very high resistance.

The solution to this problem is to change the direction of the voltage *before* the electron hits the obstruction. This way, 
we will measure the motion of the electron without the obstruction, giving a low resistance. This is known as an "alternating current"
(AC) technique, where we apply a sinusoidal voltage, and measure the resulting sinusoidal current. 

Thinking more about this, the resistance must depend on how fast (the frequency) we change the direction of the voltage; at high
frequencies the electron never has time to hit the obstruction, so we just measure the resistance of the moving electron. At very low frequencies
(in the extreme this is not changing direction at all) the electrons will hit the obstruction and give a very high resistance. Somewhere
in the middle, we should see a combination of both processes occurring. Clearly, by applying a varying voltage at different frequencies we
can learn quite a lot about what happens in our material.

Fortunately, we can extend Ohm's law to account for this AC technique. Here, we call the resistance an impedance, $Z$ which depends on the 
frequency of the voltage change ($\omega$).[^4] Because $V$ and $I$ now vary with time ($t$), the exact value they take depends on the time 
at which they are measured.

$$
I_t = \frac{V_t}{Z(\omega)}
$$

Because we apply a voltage of the form
$$
V_t = V_0 \sin(\omega t)
$$
our current $I$ must also be sinusoidal. 

**Note, though, that the current doesn't necessarily have to change direction at the same time
as the voltage!**

This is a tricky idea, but a helpful analogy is to think of momentum. Imagine a spacecraft approaching a 
distant planet very fast, but aiming to land on the surface. When the 'retro-rockets' start the spacecraft doesn't
immediately stop; it takes a while after the force starts before the existing momentum is reduced to zero (and ideally, this occurs
on the surface of the planet!). In this analogy, the spacecraft is the current and the retro-rockets are the voltage; even 
though the voltage has changed direction, it takes a while for the current to change too.





## Notes

[^1]: Note that resistance (and impedance) depends on how much material you have; a 3 cm long wire has 10,000 times less resistance than a 3 km long wire! To get round this, materials scientists refer to the 'resistivity' of a material, which is independent of how much of it there is. In this tutorial, we are ignoring this difference for simplicity.
[^2]: Conductivity is the inverse of resistivity, i.e. a higher resistivity gives a lower conductivity.
[^3]: This is not as crazy as it seems; electrons are typically 'bound' to atoms, and although they can slosh around a bit, they often cannot escape the atom completely.
[^4]: Here we are using angular frequency to simplify things, but it is related to the frequency $f$ (in Hz) by $\omega = 2\pi f$.