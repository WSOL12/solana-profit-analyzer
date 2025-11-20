# Solana DEX Arbitrage Bot

This project implements core logic for analyzing price differences between decentralized exchanges (DEXs) on Solana.
It focuses on evaluating routing outputs, comparing token conversion paths, and inspecting potential discrepancies between swap quotes.

## Overview

The system includes the following components:

* Token pair selection and configuration
* Integration with a routing engine capable of generating swap paths
* Support for circular route analysis
* Comparison of quote outputs for selected markets
* Basic modeling for multi-hop and alternative routing paths

The project currently focuses on the **WSOL/USDC** pair and includes preliminary logic for route evaluation.

## Architecture

### Routing Engine Interface

Retrieves path candidates and associated quote data from an external routing engine.
Includes support for filtering by token mints and enabling circular route generation.

### Quote Comparison

Analyzes differences between multiple routing options by comparing:

* Expected input/output amounts
* Route composition
* Path structure
* Resulting deltas between alternative routes

### Logging

Outputs structured information for inspection, including slot data, timing metrics, and quote deltas.

## Notes

* Program logic is still under development.
* Certain components (such as on-chain execution modules) are not implemented.
* Current implementation is limited to a single token pair and routing mode.

## References

* [https://station.jup.ag/docs/apis/self-hosted](https://station.jup.ag/docs/apis/self-hosted)
* [https://spl.solana.com/token](https://spl.solana.com/token)

