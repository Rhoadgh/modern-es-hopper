# Modern ES Starter (Hopper-v4)

This is a modernized fork of the OpenAI Evolution Strategies starter code. It has been updated to run on **macOS (Apple Silicon)** using **Python 3.10+** and **TensorFlow 2.15+**.

## 🚀 Key Modernizations
- **Environment:** Migrated from `gym` to `gymnasium` (Hopper-v4).
- **Architecture:** Compatibility fixes for Apple Silicon M1/M2/M3 chips.
- **Visualization:** Included `record_hopper.py` for headless MP4 generation.

## 📦 Setup
1. `conda activate EShopper`
2. `export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES`

## 🏃 Running the Experiment
### **Step 1: Start the Master**
```bash
python -m es_distributed.main master --exp_str configurations/hopper.json
```
### **Step 2: Start the Workers**
```bash
python -m es_distributed.main workers --num_workers 4
```
### **Step 3: Record Progress**
```bash
python record_hopper.py
```
Original research by OpenAI (2017). Modernized by Rhoad Ghunaim.

## 📊 Results
The Hopper begins learning stable hopping patterns within ~40 iterations.
