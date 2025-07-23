# ⚡ Energy Allocation Optimization using Genetic Algorithm (GA)

This project implements a **Genetic Algorithm (GA)** in Python to optimize energy allocation from multiple energy sources to multiple demand nodes. The objective is to **minimize cost**, **reduce energy loss**, and **maximize demand satisfaction**. The notebook also includes **CPU usage monitoring** for both serial and parallel GA execution.

---

## 📌 Project Overview

Energy distribution is a challenging problem due to the increasing demand and limited energy resources. Efficient allocation ensures reliability, economic feasibility, and grid stability. This notebook models the problem as a **constrained optimization task** and uses **Genetic Algorithms** for optimization.

---

## 📂 Files

| File Name         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `Untitled1.ipynb` | Jupyter Notebook implementing the energy allocation GA with CPU monitoring |

---

## ⚙️ Features

- ✅ Chromosome encoding for multi-source, multi-node allocation  
- ✅ Fitness function considering cost, loss, and demand satisfaction  
- ✅ Genetic operations: selection, crossover, mutation  
- ✅ Serial and parallel execution support  
- ✅ CPU usage tracking using `psutil`  
- ✅ Visualizations for performance metrics  

---

## 🧬 Problem Formulation

- **Inputs**:
  - Number of sources `S`
  - Number of demand nodes `N`
  - Time slots (optional)
  - Cost matrix, loss matrix, and demand vector

- **Objective**:
  - Maximize: Demand fulfillment
  - Minimize: Cost and transmission losses

- **Constraints**:
  - Total supply ≤ generation capacity  
  - Total demand ≤ supplied energy  
  - Source and node capacity limits  


## 🧪 Chromosome Encoding

Each chromosome represents the energy flow from all sources to all nodes. Example:

Gene = [E11, E12, ..., E1N, E21, ..., ESN]

Where:
- `Eij` = Energy from source `i` to node `j`



📊 Fitness Function

python
fitness = alpha * (1 - total_loss/maximum_possible_loss) + 
          beta * (total_demand_satisfied / total_demand) - 
          gamma * (total_cost / maximum_cost)
Tunable weights alpha, beta, gamma balance priorities

🚀 How to Run
1. Clone the Repository
git clone [https://github.com/Sushant2080-0140/MLPC-Group]
2. Install Dependencies
Make sure Python ≥3.8 is installed.
pip install numpy matplotlib pygad psutil
3. Launch the Notebook
jupyter notebook MLPC_Group_Assignment.ipynb

🖥️ CPU Usage Monitoring
The notebook includes CPU monitoring functions using the psutil library:
Tracks usage during GA execution
Plots CPU usage over time
Helps compare serial vs parallel efficiency

📈 Output Visualization
Fitness over generations
Allocation heatmaps
CPU usage plots
Performance comparison charts

🧠 Potential Enhancements
Implement multiprocessing-based parallel GA
Integrate real-world energy demand datasets (e.g., NEA data)
Add GUI for real-time simulation
Run on HPC or cloud environments

👨‍💻 Author
Member of LG3_Group 1
BCS(Hons) Students | IIMS College

🙌 Acknowledgements
PyGAD – Genetic Algorithm library for Python
psutil – System monitoring
Energy optimization research papers and real-world grid data



