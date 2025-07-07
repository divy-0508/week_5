# week_5
This project simulates such a system: participants will create an intelligent, data-driven pricing engine for 14 parking spaces using real-time data streams, basic economic theory, and ML models built from scratch, using only numpy, pandas libraries.
# 🚗 Urban Parking Dynamic Pricing Simulation

> A real-time, intelligent pricing engine for managing 14 urban parking lots using demand signals, environmental context, and competition-based adjustments.

---

## 📌 Overview

Urban parking spaces are a constrained resource, often mismanaged with static pricing. This project simulates a **dynamic, data-driven pricing engine** using real-time streams to optimize parking lot utilization across a city.

We build and deploy three pricing models:
- **Model 1: Baseline Linear Pricing**
- **Model 2: Demand-Based Intelligent Pricing**
- **Model 3: Competitive Location-Aware Pricing**

The system processes live parking data and adjusts prices continuously based on factors such as occupancy, traffic, queue length, vehicle type, and competitor prices.

---

## 🛠 Tech Stack

| Layer | Technology |
|---------------------|---------------------------|
| Language | Python |
| Data Handling | Pandas, NumPy |
| Real-Time Streaming | [Pathway](https://pathway.com) |
| Visualization | Bokeh, Panel |
| Mapping (Optional) | Geopy (for lot distances) |
| Development Env | Google Colab |

---

## 📐 System Architecture

graph TD
A[CSV Dataset] -->|Simulated streaming| B[Pathway Streaming Engine]
B --> C[Pricing Model Logic]
C --> D[Price Output Stream]

C --> E[Model 1 - Linear Pricing]
C --> F[Model 2 - Demand Based Pricing]

B --> H[Time Based Aggregation]
H --> C

D --> I[Real Time Dashboard using Bokeh and Panel]

B --> J[Optional Reroute Suggestion Logic]
