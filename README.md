# SAP CPUs

This repository implements a series of "Simple as Possible" ([SAP](https://en.wikipedia.org/wiki/Simple-As-Possible_computer)) CPUs
in a variety of forms: Logisim, FPGA, and PCB.

It is inspired by Ben Eater's [excellent tutorial](https://eater.net/8bit) on building an 8-bit computer from scratch on a
breadboard, which is itself inspired from *Digital Computer Electronics* by Albert Paul Malvino and Jerald A. Brown.

This project was created with my son as a way to teach him computing fundamentals.

# Documentation

## Building
```
# Install this package in a python virtual environment
poetry install
# Compile the microcoee and other ROMs
make
```

## CPU Architectures

### SAP-1

This is almost identical to the version of SAP-1 described in *Digital Computer Electronics* which has only 5 instructions:
LDA, ADD, SUB, OUT, and HLT.

It is described well [here](https://deeprajbhujel.blogspot.com/2015/12/sap-1-instructions-and-instruction-cycle.html).

### SAP-1b

In Progress. This will be Ben Eater's version of the SAP-1 computer with added jump and conditionals.

### SAP-1.5

Planned. An upgraded version of SAP-1b with more instructions and larger memory, while still being able to be physically
realized on a breadboard with minimal new parts from the Ben Eater kit.

### SAP-2 and SAP-3

The *Digital Computer Electronics* book describes 16-bit SAP-2 and SAP-3 architectures. However, since this is a 8-bit
CPU, we decided to take the approach found in [The 8-bit SAP-3](https://github.com/rolf-electronics/The-8-bit-SAP-3/tree/master)
and create, you guessed it, 8-bit versions.

## Logisim

The [Logisim](http://www.cburch.com/logisim/) versions of these CPUs are found in the `logisim` directory, with a few
helper scripts to load different CPU architectures.  If we were to redo this project, we would suggest using
a newer fork of Logisim, like [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution).

1. Set the `LOGISIM_PATH` environment variable to the location of logisim.jar:
1. Use `open <CPU>` to open a given CPU in Logisim.
1. Use `run <CPU> <PROGRAM>` to run a given program on the given CPU in the terminal.

## PCB Design

### Backplane

The PCB designs are inspired on the modular backplane design used in the [NQSAP-PCB project](https://tomnisbet.github.io/nqsap-pcb/)
which is itself based on [another project](https://www.reddit.com/r/beneater/comments/pn4j6j/finally_complete_with_all_bugs_fixed/).

However, we wanted to keep the same breadboard-like layout from Ben Eater
Their design is based around 100mm x 100mm modules, in order to take advantage of discount pricing of plcpcb.com.
This backplane is designed to support 100mm x 100mm modules, interconnected with a 40 pin bus.





