# Quadrature Down Converter (QDC)

## Overview

This project implements a **Quadrature Down Converter (QDC)** using analog circuit blocks such as a quadrature oscillator, MOSFET-based mixer, amplifier stage, and RC low-pass filter.

The system converts a high-frequency input signal into lower-frequency **in-phase (I)** and **quadrature-phase (Q)** components. The design was simulated using **LTSpice** and verified through hardware testing using a **Digital Storage Oscilloscope (DSO)** and waveform generator.

## Features

- Quadrature oscillator with approximately 90° phase difference
- MOSFET switch-based mixer for frequency downconversion
- RC low-pass filter for extracting IF components
- Amplifier stage for signal conditioning
- LTSpice simulation and hardware implementation
- DSO waveform and FFT-based verification

## System Architecture

```text
Input Signal
     |
     v
Quadrature Oscillator
   /               \
  v                 v
I-Phase LO       Q-Phase LO
  |                 |
  v                 v
Mixer 1          Mixer 2
  |                 |
  v                 v
Low Pass Filter  Low Pass Filter
  |                 |
  v                 v
IF(I)            IF(Q)
```

## Working Principle

The quadrature oscillator generates two sinusoidal local oscillator signals with a phase difference of approximately 90°. These signals are used as I and Q local oscillator inputs.

The input RF signal is applied to mixer stages, where it is multiplied with the local oscillator signals. This produces sum and difference frequency components. The low-pass filter removes the high-frequency components and retains the required lower-frequency intermediate-frequency signal.

## Circuit Blocks

### 1. Quadrature Oscillator

Generates two sinusoidal signals of the same frequency with an approximate 90° phase difference.

### 2. Mixer Circuit

Uses MOSFET switching action to perform frequency translation of the input signal.

### 3. Low-Pass Filter

Removes high-frequency components after mixing and extracts the desired IF output.

### 4. Amplifier Stage

Improves the output signal level while maintaining waveform integrity.

## Components Used

- UA741 Operational Amplifiers
- NMOS Transistor
- Resistors
- Capacitors
- RC Low-Pass Filter
- Function Generator
- Digital Storage Oscilloscope
- LTSpice

## Simulation and Testing

The circuit was first designed and tested in LTSpice. Individual blocks such as the oscillator, mixer, filter, and amplifier were simulated separately before combining them into the final QDC system.

Hardware testing was carried out using a waveform generator and DSO. FFT analysis was used to verify the expected frequency components after mixing.

## Results

- Oscillator frequency obtained: approximately 150 kHz
- Phase difference achieved: approximately 90°
- Successful downconversion observed
- Difference-frequency component verified through FFT
- Final I and Q outputs obtained after filtering

## Applications

- Wireless communication receivers
- Frequency translation circuits
- Signal demodulation
- RF front-end systems
- Analog signal processing

## Tools Used

- LTSpice
- Keysight Digital Storage Oscilloscope
- Function Generator
- Analog circuit components

## Team Members

- Ardra P
- Sayana Sajan
- Shreya Vinoj

## Conclusion

This project successfully demonstrates the working of a Quadrature Down Converter using analog circuit design. The quadrature oscillator generated two signals with an approximate 90° phase difference, while the mixer and low-pass filter stages performed frequency downconversion and IF extraction. Both simulation and hardware results validated the expected operation of the system.

## License

This project is intended for academic and educational purposes.
