# MicroprocessorDesign
Some microprocessor designs, designed using Proteus, software part done by Assembly

Can be opened with Proteus v8.6 or v8.9

Interrupt Program uses 8255, 8253A,8259, 8086, DAC for interrupt, setting time frequency and 74273-74154 for Addressing.
NMI is an unmaskable interrupt so even interrupt flag IF=0 it can interrupt. At program 8253 generates impulse based on 
frequency clock (setted 1 second period) and it triggers 8259's ICW1,AX register's value increments. NMI button increments
AX register's value too. AX register's value can be seen in 7 segment at 8255's portA. Assembly Code assigns interrupt program's
offset and code segment value to vector table.


![alt text](https://github.com/DevMilk/MicroprocessorDesign/new/master/Interrupt.png)


SamplingWave Program uses 8255 to read impulses at 8253A at every impulse, input signal's value assigned to an array
and when 60 sample is done, sampled signal can be seen in monitor

![alt text](https://github.com/DevMilk/MicroprocessorDesign/new/master/Sample.png)


Generating square wave with 8254:

![alt text](https://github.com/DevMilk/MicroprocessorDesign/new/master/Square.png)
