---
title: "Making UART fast"
date: 2026-11-26
draft: true
---
TODO: follow-up to [UART](../uart/).

- PLL: make a clock that divides the bit rate evenly
  (e.g. Tang Nano 9K: 27 MHz → 54 MHz, 2 Mbit/s = 27 clocks per bit, 0% error)
- Run the whole design on the PLL clock, or `done`/`data` cross clock domains
- Max bit rate of the USB-UART bridge (Tang Nano's BL702 vs. FT232H / CP2102N)
- FIFO for sending/receiving bursts
