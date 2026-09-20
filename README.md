# Gridpoint-ClumsyCoders
# 📍 GRIDPOINT

### Where should the warehouse go?

**GRIDPOINT** is a demand-aware warehouse location optimization platform that helps businesses determine where warehouses should be placed based on **customer demand, geographic position, and delivery distance**.

Built by **ClumsyCoders** for a hackathon.

---

## 🚀 Live Demo

### [Launch GRIDPOINT →](https://gridpoint-optimizer--surajpandeyftb.replit.app/dashboard)

**Data & Analytics:**
https://gridpoint-optimizer--surajpandeyftb.replit.app/data

---

# 🎯 The Problem

For an e-commerce company, deciding **where to place warehouses** is a major logistics challenge.

Different neighborhoods have:

* Different numbers of daily orders
* Different geographic locations
* Different delivery distances

A warehouse placed at the simple geographic center may not necessarily be the most efficient location.

### The challenge

> **Where should a company place its warehouse(s) to minimize overall delivery effort and cost?**

GRIDPOINT approaches this as an optimization problem.

---

# 💡 Our Solution

GRIDPOINT analyzes neighborhood-level demand and geographic positions to identify warehouse locations that can reduce overall delivery distance.

Instead of treating every neighborhood equally, GRIDPOINT gives greater importance to areas generating more orders.

### Core concept

```text
Neighborhood Data
       ↓
Order Demand
       ↓
Geographic Coordinates
       ↓
Demand-Weighted Distance
       ↓
Optimization
       ↓
Recommended Warehouse Locations
       ↓
Delivery Efficiency
```

---

# 🖥️ Product

GRIDPOINT provides an interactive dashboard where users can explore the optimization process and results.

### Dashboard

The dashboard provides a visual overview of the network, demand distribution and recommended warehouse configuration.

![GRIDPOINT Dashboard](docs/screenshots/dashboard.png)

---

# 📊 Data & Analytics

GRIDPOINT includes a dedicated data interface for working with the underlying neighborhood and demand information.

**Explore the live data interface:**

👉 https://gridpoint-optimizer--surajpandeyftb.replit.app/data

The data layer forms the foundation of the optimization process by connecting:

* 📍 Geographic locations
* 📦 Order demand
* 🏭 Warehouse requirements
* 🚚 Delivery distances

---

# ⚙️ How GRIDPOINT Works

## 1️⃣ Collect Demand Data

The system starts with neighborhood-level information such as:

* Location
* Latitude / longitude
* Daily order volume

---

## 2️⃣ Model Demand

Each neighborhood is treated as a demand point.

Higher-order neighborhoods receive greater weight in the optimization process.

For example:

```text
Neighborhood A → 500 orders/day
Neighborhood B → 100 orders/day
Neighborhood C → 50 orders/day
```

Neighborhood A therefore has a much greater influence on the warehouse placement.

---

## 3️⃣ Calculate Delivery Distance

GRIDPOINT evaluates the distance between demand points and potential warehouse locations.

The optimization focuses on minimizing the total demand-weighted delivery distance.

### Simplified objective

```text
Minimize:

Σ (Demandᵢ × Distanceᵢ)
```

This means that serving a high-demand neighborhood from a distant warehouse has a larger impact than serving a low-demand neighborhood from the same distance.

---

## 4️⃣ Optimize Warehouse Locations

The system evaluates possible warehouse configurations and identifies locations that reduce the overall delivery burden.

---

## 5️⃣ Visualize the Result

Instead of returning only a number, GRIDPOINT presents the result visually through the dashboard.

This allows users to understand:

* Where warehouses are located
* Where demand is concentrated
* How the network is distributed
* What the resulting optimization looks like

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │        USER         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   GRIDPOINT WEB UI  │
                    │      Dashboard      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    DATA LAYER       │
                    │                     │
                    │ Demand + Locations  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   OPTIMIZATION      │
                    │       ENGINE        │
                    │                     │
                    │ Demand × Distance   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      RESULTS        │
                    │                     │
                    │ Warehouse Locations │
                    │ + Network Metrics   │
                    └─────────────────────┘
```

---

# 🧠 Why Demand Weighting?

A normal geographic-center approach assumes that every location matters equally.

GRIDPOINT takes a different approach.

Consider:

```text
                 Orders

Area A             ████████████████████  800

Area B             ███████               300

Area C             ██                     80
```

A warehouse positioned slightly closer to Area A can potentially have a much greater impact on total delivery effort than one optimized purely around geographic centrality.

This makes **demand-weighted optimization** particularly useful for delivery networks.

---

# 🌎 Potential Applications

GRIDPOINT can be applied to several real-world logistics scenarios:

### 🛒 E-commerce

Determine where fulfillment centers should be established based on customer demand.

### 🚚 Last-Mile Delivery

Reduce the distance between warehouses and high-demand areas.

### 🏪 Retail

Optimize regional distribution centers around store demand.

### 📦 Supply Chain

Evaluate different warehouse configurations before making infrastructure investments.

### 🏭 Network Planning

Compare different warehouse scenarios as demand patterns change.

---

# 📈 Key Features

| Feature                   | Description                            |
| ------------------------- | -------------------------------------- |
| 📍 Geographic Mapping     | Visualize demand locations             |
| 📦 Demand Analysis        | Account for different order volumes    |
| 🏭 Warehouse Optimization | Identify efficient warehouse locations |
| 📊 Analytics              | Understand network-level metrics       |
| 🗺️ Visualization         | See demand and warehouse placement     |
| 🌐 Web Dashboard          | Interactive browser-based interface    |
| 🚀 Live Deployment        | Accessible through the web             |

---

# 🔮 Future Scope

GRIDPOINT can be extended significantly beyond the current hackathon MVP.

### 🛣️ Real Road Networks

Replace straight-line distance with actual road-network travel distance.

### 🚦 Traffic-Aware Optimization

Incorporate traffic patterns and expected travel time.

### 🏭 Warehouse Capacity

Add constraints such as:

```text
Warehouse A → 10,000 orders/day
Warehouse B → 15,000 orders/day
```

The optimizer could then ensure that warehouses aren't overloaded.

### ⏱️ Delivery Time Windows

Optimize locations based not only on distance but also required delivery times.

### 💰 Cost Optimization

Combine:

```text
Warehouse Cost
+
Transportation Cost
+
Delivery Cost
```

to determine the overall network cost.

### 📡 Real-Time Demand

Connect GRIDPOINT to live order data and continuously update recommendations.

### 🔄 What-If Scenarios

Allow users to compare:

```text
1 Warehouse
vs
2 Warehouses
vs
3 Warehouses
```

and understand how the network changes.

---

# 🛠️ Technology

GRIDPOINT is a web-based optimization application.

### Core Components

* Interactive web dashboard
* Geographic visualization
* Demand analysis
* Warehouse location optimization
* Data visualization
* Web deployment

### Deployment

**Replit**

---

# 🤖 AI-Assisted Development

AI tools were used as development assistants during the hackathon.

### ChatGPT

Used for:

* Ideation
* Architecture discussions
* Debugging
* Documentation
* Problem decomposition

### Google Gemini

Used for:

* Alternative approaches
* Research
* Validation
* Brainstorming

### Claude

Used for:

* Code reasoning
* Reviewing approaches
* Refinement
* Debugging assistance

AI tools were used as development assistants. The **GRIDPOINT concept, product direction, implementation, integration and final decisions were developed and assembled by ClumsyCoders.**

---

# 👨‍💻 Team

## ClumsyCoders

### 🧑‍💻 GRIDPOINT

**Hackathon Project**

> *Where should the warehouse go?*

---

# 🎥 Demo

### Live Application

👉 **https://gridpoint-optimizer--surajpandeyftb.replit.app/dashboard**

### Data Interface

👉 **https://gridpoint-optimizer--surajpandeyftb.replit.app/data**

---

# 📑 Presentation

Our complete hackathon presentation is available in:

[GridPoint.pdf](https://github.com/user-attachments/files/32433701/GridPoint.pdf)





# 📸 Screenshots

<img width="1600" height="894" alt="image" src="https://github.com/user-attachments/assets/81428d00-6205-454d-8e9d-d222f7659ede" />
<img width="1600" height="891" alt="image" src="https://github.com/user-attachments/assets/372457c7-090d-4b43-b3c3-3fcd5785bc16" />
<img width="1600" height="880" alt="image" src="https://github.com/user-attachments/assets/e31905c8-d0e9-46aa-948c-fdabaa6bbd63" />
<img width="1600" height="905" alt="image" src="https://github.com/user-attachments/assets/4cf79166-cd7c-41a3-b266-753f92e76fe9" />
<img width="1600" height="898" alt="image" src="https://github.com/user-attachments/assets/65f1310d-021c-4c95-a4a9-f04a3506f45c" />
<img width="1600" height="852" alt="image" src="https://github.com/user-attachments/assets/8c3b6399-e2f8-426f-8752-debc99ed14f9" />
<img width="1600" height="862" alt="image" src="https://github.com/user-attachments/assets/0b43014a-ebda-4fa9-aa01-d73506be0039" />
<img width="1600" height="847" alt="image" src="https://github.com/user-attachments/assets/d687a23e-8699-42ad-bfad-40184c9fd3e9" />
<img width="1600" height="856" alt="image" src="https://github.com/user-attachments/assets/dbb912cc-0a12-4ca1-a011-58bf1169d671" />
<img width="1600" height="798" alt="image" src="https://github.com/user-attachments/assets/2178c94e-7d76-4f32-8f1d-7175af75418a" />


---

# ⭐ Project Vision

GRIDPOINT aims to turn a complicated logistics question into a simple decision:

> **Given where customers are and how much they order, where should the warehouse go?**

---

## 📍 GRIDPOINT

**ClumsyCoders**

*Demand → Optimization → Better Locations → Better Delivery*
