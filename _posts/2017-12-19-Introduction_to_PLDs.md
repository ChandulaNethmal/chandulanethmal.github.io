---
title: "Introduction to Programmable Logic Devices"
date: "2017-12-19" 
---

## PROGRAMMABLE LOGIC DEVICES(PLDS)
A PLD is an electronic component used to build reconfigurable digital circuits. Unlike a traditional logic gate, which has a fixed function, a PLD has an undefined function at the time of manufacture which can be defined according to the end user’s requirement. Before the PLD can be used in a circuit it must be programmed, that is, reconfigured.

<iframe width="560" height="315" src="https://1.bp.blogspot.com/-ei3IIYwhLeI/WkhKTQbbfzI/AAAAAAAAAs8/IqHVzsqMYbYwwFK_dJPznBf39236YnApQCLcBGAs/s1600/IC.jpg" frameborder="0" allowfullscreen></iframe>

## How PLDs realized their Programmability
A PLD is a combination of a reconfigurable logic array and a memory device. The memory is used to store the inputs that was given to the chip during programming and outputs. Most of the methods for storing data in an integrated circuit have been adapted for use in PLDs. These include:
·         Silicon antifuses
·         SRAM
·         EPROM or EEPROM cells
·         Flash memory
·         Silicon antifuses are connections that are made by applying a voltage across a modified area of silicon inside the chip. They are called antifuses because they act in the opposite way to normal fuses, which begin life as connections until they are broken by an electric current.
<iframe width="560" height="315" src="https://2.bp.blogspot.com/-UKiy7NrqVBE/WjiR2u1XuGI/AAAAAAAAAro/f92qwmO3HEog6VK63YBC6zvIl0LYHxoPgCLcBGAs/s320/VIA.GIF" frameborder="0" allowfullscreen></iframe>

 Antifuse

·         SRAM, or static RAM, is a volatile type of memory, meaning that its contents are lost each time the power is switched off. SRAM-based PLDs therefore have to be programmed every time the circuit is switched on. This is usually done automatically by another part of the circuit.
·         An EPROM cell is a MOS (metal-oxide-semiconductor) transistor that can be switched on by trapping an electric charge permanently on its gate electrode. This is done by a PAL programmer. The charge remains for many years and can only be removed by exposing the chip to strong ultraviolet light in a device called an EPROM eraser.

 
·         Flash memory is non-volatile, retaining its contents even when the power is switched off. It can be erased and reprogrammed as required. This makes it useful for PLD memory.

 There are several kinds of PLDs available with different kind performances.

## Simple Programmable Logic Devices (SPLDs)
Simple programmable logic devices (SPLD) are the simplest, smallest and least-expensive forms of programmable logic devices. SPLDs can be used in boards to efficiently replace standard logic components (AND, OR, and NOT gates), such as 7400-series TTL.
They typically contain 4 to 22 fully connected macrocells which are typically consist of some combinatorial logic and a flip-flop. In other words, a small Boolean logic equation can be built within each macrocell. This equation will combine the state of some number of binary inputs into a binary output and, if necessary, store that output in the flip-flop until the next clock edge. Of course, the particulars of the available logic gates and flip-flops are specific to each manufacturer and product family. But the general idea is always the same.



#    1.    PROM
(Programmable ROM)
PROM is the oldest ancestor of the PLD family which is used to create arbitrary combinational logic functions of a number of inputs. M input address and N output data line ROM can produce N separate logic circuits (of up to M inputs)

#    2.    PLA
 (programmable Logic Array)
A programmable logic array (PLA) has a programmable AND gate array, which links to a programmable OR gate array, which can then be conditionally complemented to produce an output.


#   3.    PAL
(Programmable Array Logic)
PAL devices have arrays of transistor cells arranged in a "fixed-OR, programmable-AND" plane used to implement "sum-of-products" binary logic equations for each of the outputs in terms of the inputs and either synchronous or asynchronous feedback from the outputs.

#   4.    GAL
(Generic Array Logic)
This device has the same logical properties as the PAL but can be erased and reprogrammed.  The GAL is very useful in the prototyping stage of a design, when any bugs in the logic can be corrected by reprogramming. GALs are programmed and reprogrammed using a PAL programmer, or by using the in-circuit programming technique on supporting chips.


## Complex programmable logic Devices (CPLD)
PALs PLAs and GALs are available only in small sizes, equivalent to a few hundred logic gates. For bigger logic circuits, complex programmable Logic Devices can be used. These contain the equivalent of several PALs linked by programmable interconnections, all in one integrated circuit. CPLDs can replace thousands, or even hundreds of thousands, of logic gates.

Some CPLDs are programmed using a PAL programmer, but this method becomes inconvenient for devices with hundreds of pins. A second method of programming is to solder the device to its printed circuit board, then feed it with a serial data stream from a computer. The CPLD contains a circuit that decodes the data stream and configures the CPLD to perform its specified logic function. Some manufacturers such as ALTERA use JTAG to program CPLD's in-circuit from .JAM files.

##   Field Programmable Gate Array ( FPGA)

FPGA is an abbreviation for “Field Programmable Gate Array”. Basically FPGA is a huge array of gates which can be programmed and reconfigured any time anywhere using kind of hardware implementation languages called Hardware Description Languages (HDL). “Huge array of gates” is an oversimplified description of FPGA. This is one of  advanced members of Programming Logic Devices (PLD) family. 

<iframe width="560" height="315" src="https://3.bp.blogspot.com/-YigaK8X9yGc/WjiWmRw6LAI/AAAAAAAAAsQ/WP9MyqfLo8sC5uDrJrwH94GvS9L7fa42QCLcBGAs/s200/F7716724-01.jpg" frameborder="0" allowfullscreen></iframe>

Altera Cyclone IV FPGA chip

<iframe width="560" height="315" src="https://4.bp.blogspot.com/-AsGSFkhbcQ0/WkhKdfBB0NI/AAAAAAAAAtA/_f8L_nKO6_0vH9_SrXdLSPIKVoWWWEDvgCLcBGAs/s1600/fpga_284x177.jpg" frameborder="0" allowfullscreen></iframe>

In the above PLDs we were able program only the gate array for particular application. But when we are involved in complex analysis and processing through more complex logic levels we may need the programmability of the gates as well as connections. FPGA which are capable of giving the programmability to the connections is the best solution for such kind of applications.

