# 🧠 Neural Network Simulation – Operating Systems Project

This is my **4th semester project** for the course **Operating Systems**.  
The project simulates a **multi-layer feedforward neural network** using **processes, threads, mutex locks, and pipes** to demonstrate **parallelism, synchronization, and inter-process communication** in C++.

---

## 📌 Project Overview

The program performs:
- **Forward Propagation** across multiple layers of neurons.
- **Backpropagation** to adjust values.
- **POSIX Threads (pthreads)** for neuron-level parallelism.
- **Process forking** for layer-level parallelism.
- **Mutex locks** to avoid race conditions.
- **Pipes** for inter-process communication.

---

## 👨‍💻 Group Members

- **Moiez Asif** (21I-2483)  
- **Hamza Saeed** (21I-0671)  
- **Aasir Farrukh** (21I-0375)  

---

## 🛠 Technologies Used

- **Language:** C++ (POSIX standard)
- **OS Concepts:**
  - Process creation → `fork()`
  - Thread creation → `pthread_create()`
  - Synchronization → `pthread_mutex`
  - Inter-process communication → `pipe()`
- **Compiler:** `g++`
- **Platform:** Linux (Ubuntu recommended)

---

## ⚙️ How It Works

### **1. Network Structure**
- **Total Layers:** 7  
  - **Input Layer:** 2 neurons  
  - **Hidden Layers:** 5 layers, each with 8 neurons  
  - **Output Layer:** 1 neuron  
- Predefined weights stored in `header.h`.

### **2. Forward Propagation**
- Each **layer** is processed in a separate **process**.
- Inside each layer, **neurons** are processed in **parallel threads**.
- Outputs are sent between layers via **pipes**.

### **3. Backpropagation**
- Calculates `fx1` and `fx2` values after forward pass.
- Sends values backward through all layers using pipes.

---

## 📂 Project Structure
├── main.cpp # Main logic for forward & backward propagation

├── header.h # Predefined weights for each layer

---

## 🎯 Learning Outcomes
- Understood process vs thread parallelism.
- Implemented mutexes for thread safety.
- Used pipes for inter-process communication.
- Applied OS concepts to simulate neural network computations.

---

## 📜 License
This project is for educational purposes only.
