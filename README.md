# Capstone-Project

# Dynamic Pricing for Urban Parking Lots

---

## Project Overview

Urban parking lots are a limited and valuable resource. Static pricing leads to inefficiencies such as overcrowding or underutilization. This project simulates a real-time pricing engine across 14 parking lots using historical and real-time data streams. Features used include occupancy, queue length, traffic conditions, vehicle type, and special events.

This repository includes Model 2 - Demand-Based Dynamic Pricing. The model uses a custom demand function to compute price adjustments based on current lot conditions, implemented using a real-time stream processing engine (Pathway).

---

## Tech Stack

- Python 3.x
- Pandas
- NumPy
- Pathway (streaming engine)
- Bokeh and Panel (for visualization)
- Google Colab (execution environment)

---

## Architecture Diagram

```mermaid
flowchart TD
    A[CSV Data] --> B[Pathway Streaming Engine]
    B --> C[Feature Engineering]
    C --> D[Demand Calculation]
    D --> E[Min-Max Normalization]
    E --> F[Price Calculation and Clamping]
    F --> G[Live Dashboard with Bokeh]
