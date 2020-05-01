---
title: "Serial Communication"
date: "2018-04-17" 
---
 
##  Serial Communication
Most of the electronic designs which are based on integrated circuits are doing data communication with external peripherals connected in to the same design or with another device. Any kind of embedded system which having a micro-controller or a microprocessor are definitely capable and need data communication. Also, that kind of designs are having several circuits combined together using a communication protocol.

<iframe width="560" height="315" src="https://2.bp.blogspot.com/-sdxozX2ZjQE/WtYt1-qsVTI/AAAAAAAAA5c/l_B-530VzwAMq_d6B4dJXmvoE3-7oJYaQCLcBGAs/s320/U5dspZFBZGsSau4jpiCKeJZmDVEi5Mr_1680x8400.jpg" frameborder="0" allowfullscreen></iframe>

In order to perform a successful data communication between any kind of two devices, they must have a common communication protocol. Communication protocols can be divided into several categories considering their properties.  Most common and widely used two categories are;

·        Serial Communication Protocols 
·        Parallel Communication Protocols

## Parallel Communication
In parallel communication protocols, one entity (Transmitter) can send more than one bit at a time. In other word communication can be done with several data bits transmitting parallelly using several physical lines.  Usually we can see bunch of wires which are serving as data busses in parallel communication devices. Following figure shows a typical 8-bit parallel communication port.

<iframe width="560" height="315" src="https://4.bp.blogspot.com/-3qpbZtdXJ7E/WtYuW5kDVUI/AAAAAAAAA5k/d6JkJPEWJbMfIH1j1ofe-RBiueFISs1FwCLcBGAs/s320/50e1cca6ce395fbc27000000.png" frameborder="0" allowfullscreen></iframe>

According to the figure there are 8 data lines to communication and another wire to send a clock signal. This clock signal is sending in order to having a synchronization between two entities. Width of the data bus can be varied such as 4-bits, 8bits, 16-bits,32-bits etc.

## Serial Communication 
Here we are sending a stream of data as a single bit at a time. This communication method needs only a pair of data lines to transmit data bits. But sometimes we need to use another clock signal line also. 
<iframe width="560" height="315" src="https://1.bp.blogspot.com/-YdHO5A0vbXk/WtYuuiqy3jI/AAAAAAAAA5o/4qXC_CsJdyMQZi-AH13_4NV3f_jCxrjVwCLcBGAs/s320/50e1ccf1ce395f962b000000.png" frameborder="0" allowfullscreen></iframe>
Above figure shows a single direction serial communication model between two entities with a clock signal at the bottom line. It sends a set of 8bits (one byte) serially using a single line but using several clock cycles. That means spend more time than sending parallelly.

## Parallel vs. Serial
When we compare these two categories of protocols, each have their own pros and cons. Parallel communication is really faster than serial communication because it sends multiple bits in a single clock cycle, while the serial protocol uses multiple clock cycles to send the same data amount.
But it saves number of physical wires of a design and reduce the hardware complexity. On the other hand, upper layers of the communication model needed to handle serial data by may be increasing the software complexity.
In some projects number of output/input pins of a micro-controller or an ASIC will be a critical thing rather than the complexity of the code. Then it will be a great relief with having a serial communication protocol with you. 

## Synchronous and Asynchronous Communication
## What is synchronization?
When there is a digital data communication between any kind of two electronic devices or circuits, both of them should have some common things. Specially a common rhythm between two entities. That means a common clock rate to determine where the data bits or frames are starting and ending. So, maintaining a common clock rate and common rising and falling edges of the clock signal between two devices is called the synchronization.
There are two different synchronization methods for data transmission which are differ by the clock source. In Synchronous method an external clock signal is supplied over the medium (ex- extra line for clock signal) while asynchronous method has no need of external clock but, the receiver entity can recover clock signal and synchronize using some specific data signal variations such as start and stop bits.

<iframe width="560" height="315" src="https://4.bp.blogspot.com/-qvMi3VMZSRs/WtYvOgjulgI/AAAAAAAAA54/yGWMT8XdtNsBjB_BLhbRPkB0x_XSVYpGQCLcBGAs/s1600/soa-synchronous_vs_asynchronous_methods_desktop.jpg" frameborder="0" allowfullscreen></iframe>
 Comparison between Synchronous and Asynchronous

## Asynchronous communication
According to the previous details, here we are transmitting data without using an external clock signal. When we sending data using this method the data is sent frames, with several synchronization symbols within each frame instead of as a continuous data stream.
Normally data is sent as one byte at a time and adding start bit at the beginning of the byte and stop bit at the ending of the byte.
## Asynchronous Serial
Here data is sent through a serial interface and asynchronous method is used for synchronization. When we are considering some serial interfaces USB (Universal Serial Bus), Ethernet, I2C and SPI (Serial peripheral Interface) have widely used in many applications. Among them, I2C and SPI are serial synchronous protocols which are using extra line for clock signal other than the communication lines.
An asynchronous serial interface communicates without a support from an external clock line by minimizing the number of needed wires or number of IO pins of a device. On the other hand, we have to put some extra effort to synchronization from software side. Bluetooth modules, GPS modules, wi-fi modules and most of other modules we have used for our projects are based on this serial communication.

##  Structure of an Asynchronous Serial data frame

In asynchronous serial protocol, there are several things to consider other than the set of data bits. 

<iframe width="560" height="315" src="https://4.bp.blogspot.com/-_H6LqMUpuCo/WtYvr6_qpiI/AAAAAAAAA6A/0S_pWZllTBoPnalN9CA9o6y3btEPk4NbACLcBGAs/s400/UART_frame.png" frameborder="0" allowfullscreen></iframe>

Data bits: Each packet contain a set of data bits which has a varying length (ex-one byte). But most of the times we are using 8bit as the data bits and sometimes 7bits if we are transferring 7bit ASCII characters. Both devices should agree with the length of the frames and what are the endianness of the data bits set. 

Synchronization bits: There two or three bits in every data frame which are specially assigned as synchronization bits. Their job is to show the starting point and ending point of a data frame. Therefore, they are called as start bit and stop bits. Normally start bit contains only one bit while one or two bits for the stop bits.

Parity bits: Most of the data frames there is an error detection data bit which is based on a parity detection mechanism handled by two entities. This parity detection method is based on whether the sum of the data bits (number of ‘1’s in the data bits) are even or odd. There also two parity methods called odd parity and even parity. If the sum is odd and the even parity is used then parity bit is set to “1”.
Set the parity bit to ‘1’ or ‘0’ as following,

Even parity ---“sum of Data bits + Parity bit ---> is an even number”
Odd parity ---“sum of Data bits + Parity bit ---> is an odd number”

Apart from the data frame, there is another important thing that we need to consider in asynchronous serial communication. That is the baud rate.

## Baud Rate
In telecommunication theory, baud rate is the number of symbols sent along a channel per second. Here also it describes the same thing and the baud rate is measured by how much bits per second the serial interface can communicate. It gives us a sense how fast a serial link can send data. Normally we are using 1200, 2400, 4800, 9600,19200,38400,57600 and 115200 bits per second as standard baud rates. Most common and simple applications are using 9600 bps while the speed critical applications are using 115200 bps as the baud rate.
Whatever the data rate, the two communication entities must communicate in the same data rate in order to obtain a successful communication.

## Serial Asynchronous Interfaces in Hardware
In most of the applications we expect a duplex communication between two devices. That means either of two devices capable receive and transmit data. There are two kinds of duplex communication. One is Full-duplex which enable to receive and transmit data at the same time. Other is the Half duplex which enable transmit or receive data to one entity after other one is completed.

So, these kinds of interfaces must have two lines to receive and transmit data and another line for a common ground. 

<iframe width="560" height="315" src="https://2.bp.blogspot.com/-WPTKw8yQnm8/WtYwNGWmrsI/AAAAAAAAA6M/VcwR0bx8kqcKPoIWICQf4BIulyqnhPmlgCLcBGAs/s400/download.png" frameborder="0" allowfullscreen></iframe>

There an important thing about wiring the two entities. RX and TX pins are working relative to themselves and we must have wired them considering the system. Tx pin of one device should be connected in the RX pin of the other device and vice versa.
Bluetooth modules, GPS modules, RTC modules and Communication between two microcontrollers are some common applications of duplex.
Sometimes we are using one direction data transmission. That means we need only to transmit data to someone or only to receive data from someone. Then we use a single line to obtain the communication. This method is called as the Simplex communication.

