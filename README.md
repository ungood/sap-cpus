# SAP CPUs

This repository implements a series of "Simple as Possible" ([SAP](https://en.wikipedia.org/wiki/Simple-As-Possible_computer)) CPUs
in a variety of forms: Logisim, FPGA, and PCB.

It is inspired by Ben Eater's [excellent tutorial](https://eater.net/8bit) on building an 8-bit computer from scratch on a
breadboard, which is itself inspired from *Digital Computer Electronics* by Albert Paul Malvino and Jerald A. Brown.

This project was created with son as a way to teach him computing fundamentals.

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

### Future

If we take this project further, I am undecided if we will build towards SAP-2 and SAP-3, or if, instead, we'll build
towards a 6502 design, so we can follow up with Ben Eater's 6502 series.

## Logisim

1. Set the `LOGISIM_PATH` environment variable to the location of logisim.jar:
3. Use `open <CPU>` to open a given CPU in Logisim.

## PCB Design

### Backplane

The PCB designs are based on the modular backplane design used in the [NQSAP-PCB project](https://tomnisbet.github.io/nqsap-pcb/)
which is itself based on [another project](https://www.reddit.com/r/beneater/comments/pn4j6j/finally_complete_with_all_bugs_fixed/).

This backplane is designed to support 100mm x 100mm modules, interconnected with a 40 pin bus.

