# UART Transmitter Verification using SystemVerilog

## Overview
This project implements a non-UVM, class-based verification environment for a UART transmitter using SystemVerilog. It uses object-oriented programming, constrained random stimulus generation, mailboxes, and a self-checking scoreboard to compare expected data against the data reconstructed from the serial TX output.

## Features
- Randomized 8-bit transaction generation
- Class-based testbench architecture
- Generator and driver communication using mailboxes
- UART serial data monitoring and reconstruction (LSB first)
- Self-checking scoreboard for expected-versus-observed data comparison
- PASS/FAIL reporting for transaction-level verification
- Clock and reset handling

## Verification Architecture
Generator → Driver → UART DUT → Monitor → Scoreboard

The generator also sends expected transactions directly to the scoreboard through a separate mailbox.

## Technologies
- SystemVerilog
- Object-oriented verification
- Mailboxes and virtual interfaces
- QuestaSim / ModelSim or a compatible simulator

## Learning Objectives
This project demonstrates the fundamentals of building a reusable, self-checking SystemVerilog verification environment before progressing to UVM-based verification.

**Scope:** The current implementation focuses on verifying transmitted data bytes in a simplified UART transmitter. Baud-rate accuracy and comprehensive protocol assertions are outside the current scope.

