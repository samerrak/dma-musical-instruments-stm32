# DAC, Timers, Interrupts, DMA, and Analog Interfacing

## Introduction
This project explores the generation and control of audio signals using the **STM32L4+ microcontroller**'s DAC, timers, interrupts, and DMA. The main objective is to generate audio signals and regulate them efficiently using hardware resources to achieve precise timing and minimize CPU usage.

---

## Part 1: Signal Generation with Software Delay

### Overview
In this part, waveforms such as **sine**, **triangle**, and **sawtooth** are manually generated using software delays and output via DAC channels connected to a speaker. The focus is on understanding the fundamental operation of the DAC.

# Part 2: Signal Generation with Timers, Interrupts, and DMA

## Overview
Part 2 focuses on transitioning from a software-based method of signal generation to a hardware-based approach. By leveraging timers, interrupts, and DMA, this method significantly improves timing accuracy, reduces CPU workload, and enables more efficient signal generation. 

---

## A. Button Interrupts
Button interrupts are configured to allow user input by detecting rising edges on a GPIO pin. This eliminates the need for continuous polling and reduces CPU usage. When the button is pressed, the program cycles through four modes. Each mode is indicated by an LED pattern and corresponds to a specific waveform or signal frequency.

### Key Features:
- **Mode Cycling**: The program switches between four modes with each button press.
- **LED Indication**: LED patterns provide a visual indication of the current mode.
- **Efficiency**: The use of interrupts enables instant reaction to user input without affecting other tasks.

---

## B. DAC Using Timer Interrupts
Timers are configured to generate periodic interrupts, ensuring precise timing for DAC updates. This approach eliminates the inaccuracies caused by software delays and guarantees consistent signal generation.

### Key Features:
- **Precise Timing**: Timers ensure that DAC updates occur at regular intervals.
- **Waveform Control**: Precomputed waveform samples are used to update the DAC output, resulting in smooth and continuous signal generation.
- **Accuracy**: Each sample is sent to the DAC with precise timing, producing high-quality waveforms.

---

## Observations
- **Improved Signal Quality**: Timer-based signal generation produces smooth and consistent waveforms compared to the software delay method.
- **Oscilloscope Validation**: Generated waveforms were observed on an oscilloscope, confirming the accuracy of the output.
- **Efficiency**: The use of hardware-based signal generation reduces CPU workload and ensures reliable performance.

---

## Conclusion
The use of button interrupts and timers significantly enhances the signal generation process. Button interrupts provide efficient user interaction, while timers ensure precise DAC updates. This hardware-based approach demonstrates the importance of leveraging microcontroller peripherals for efficient and accurate signal processing.
