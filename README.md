# PWM Generator using Verilog

## Overview

This project implements an 8-bit PWM (Pulse Width Modulation) Generator using Verilog HDL.

PWM is a technique used to control the average power delivered to a device by changing the duty cycle of a digital signal.

## Inputs

- `clk` – Clock signal
- `reset` – Reset signal
- `duty_cycle` – 8-bit duty-cycle control

## Output

- `pwm_out` – PWM output signal

## Working Principle

An 8-bit counter continuously counts from 0 to 255.

The PWM output is HIGH when:

counter < duty_cycle

Otherwise, the output is LOW.

## Duty Cycle

| Duty Cycle Value | Approx. Duty Cycle |
|------------------|-------------------|
| 0 | 0% |
| 64 | 25% |
| 128 | 50% |
| 192 | 75% |
| 255 | ~100% |

## Files

- `pwm_generator.v` – PWM generator design
- `pwm_generator_tb.v` – Testbench
- `README.md` – Project documentation
- `simulation_result.png` – Simulation waveform

## Software Used

- Icarus Verilog
- ModelSim / Vivado
- GTKWave

## How to Run

### Compile

```bash
iverilog -o pwm pwm_generator.v pwm_generator_tb.v