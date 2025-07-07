# 🚗 Summer Analytics 2025 Capstone Project
## Dynamic Pricing Engine for Urban Parking Lots

This project implements a dynamic pricing engine for parking lots based on real-time occupancy and external factors like traffic, queue length, and spatial competition. The objective is to build three progressively advanced models:

---

## 📊 Models Implemented

### 🧩 Model 1: Linear Pricing
- Price increases linearly with occupancy.
- Simple baseline to benchmark against.

### 🧠 Model 2: Demand-Based Pricing
- Factors:
  - Occupancy Ratio
  - Queue Length
  - Traffic Conditions Nearby
  - Special Day Flag
  - Vehicle Type Weight
- Normalized demand is scaled and mapped to price range.

### 📍 Model 3: Competitive Pricing
- Enhances Model 2 by:
  - Computing nearby lots within 1 km (via Haversine)
  - Adjusting pricing based on nearby prices at the same timestamp
  - Final price = Base + η × (AvgNearby - Own)

---

## 🛠 Tech Stack Used

- Python
- Pandas
- NumPy
- Bokeh (for interactive plots)
- Matplotlib (for debugging)
- Google Colab
- GitHub

---

## 🧭 Architecture Diagram

```mermaid
flowchart TD
    A[Load & Clean Dataset] --> B[Model 1: Linear Pricing]
    A --> C[Model 2: Demand-Based Pricing]
    C --> D[Model 3: Competitive Adjustment]
    D --> E[Final Price Output + Plots]
