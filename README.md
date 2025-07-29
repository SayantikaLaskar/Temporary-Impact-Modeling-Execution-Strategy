# 📊 Temporary Impact Modeling & Execution Strategy

This repository contains my submission for **Blockhouse Work Trial Task 2**, focused on analyzing **temporary market impact** and designing an efficient **order allocation strategy** using real-world limit order book data.

---

## 📁 Contents

- `Blockhouse Assignment.ipynb`: Google Colab notebook with complete implementation
- `Blockhouse_Report.docx`: Detailed report of findings
- `data/`: Folder containing the 3 L2 datasets (FROG, CRWV, SOUN)
- `README.md`: Project overview and usage instructions

---

## 📌 Objective

1. **Model the Temporary Impact Function**  
   Derive the cost of executing a market order of size `x` at time `t` using historical L2 data.
   - Estimate:  
     \[
     g_t(x) = \frac{\text{Total cost to buy } x \text{ shares}}{x}
     \]
   - Compare actual `gₜ(x)` with a **linear approximation** \( βₜ x \)

2. **Design Order Allocation Strategy**  
   Formulate and simulate strategies to execute `S` shares over a trading day:
   - **Uniform Allocation**: Spread evenly across 390 minutes
   - **Greedy Allocation**: Allocate more volume in low-slippage minutes

---

## 🧠 Methods

- Simulated order execution using top 10 ask levels
- Plotted and analyzed `gₜ(x)` across 3 stocks: FROG, CRWV, SOUN
- Fitted linear models for slippage estimation
- Compared total execution cost of different strategies

---

## 💻 Requirements

- Python 3.7+
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scikit-learn`

---

## 🚀 Running the Notebook

You can run the notebook in Google Colab:

1. Open [`blockhouse_task2.ipynb`](./blockhouse_task2.ipynb)
2. Upload the 3 datasets when prompted (FROG, CRWV, SOUN)
3. Execute all cells to reproduce the analysis

---

## 📊 Results Summary

| Strategy         | Total Cost    | Notes                 |
|------------------|---------------|------------------------|
| Uniform Allocation | $341,947.50   | Low consistent slippage |
| Greedy Allocation  | $352,137.71   | High burst impact       |

---

## 📝 Report

See `Blockhouse_Phase2_Report_SayantikaLaskar.pdf` for detailed methodology, plots, and analysis.

---

## 📧 Author

**Sayantika Laskar**  
B.Tech CSE | VIT Bhopal  
Email: *sayantikalaskar@email.com*  
GitHub: [@sayantika-laskar](https://github.com/sayantika-laskar)

---

## 🏁 Acknowledgment

This project was completed as part of the Blockhouse Intern Phase 2 Trial Assignment (July 2025).

