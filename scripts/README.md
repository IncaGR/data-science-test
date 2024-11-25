# **IFCO Data Science Challenge**

This repository contains the solution to the IFCO Data Science Challenge. The project uses Docker for consistent and reproducible results and demonstrates survival analysis and pool size estimation based on simulated data.

---

## **Project Overview**
1. **Challenge Goals**:
   - Estimate the shrinkage rate (probability of an asset not returning from a trip).
   - Estimate the pool size (number of assets available at any given time).

2. **Key Features**:
   - Simulation of trip durations using a Poisson distribution.
   - Survival analysis using Kaplan-Meier estimators.
   - Pool size estimation over time.

3. **Requirements**:
   - Python 3.8+
   - Docker installed on your machine.

---

## **Getting Started**

### **1. Build the Docker Image**
Navigate to the project directory where the `Dockerfile` is located. Use the following command to build the Docker image:

```sh
docker build -t ifco-data-science-env .
```

### **2. Run the Docker Container**
Run the Docker container with port binding and volume mapping:

```sh
docker run -it --rm -p 8888:8888 -v ${PWD}:/app ifco-data-science-env
```

If port `8888` is already in use, you can replace it with another port, e.g., `8899`:

```sh
docker run -it --rm -p 8899:8888 -v ${PWD}:/app ifco-data-science-env
```

---

## **How to Use**

### **Jupyter Notebook**
1. When the container starts, you’ll see a Jupyter Notebook URL in the terminal.
2. Copy the URL into your browser to access the Jupyter environment.
3. Open the `scripts/solution.ipynb` file to view or run the analysis.

### **Image Output**
Simulation results, including the Poisson distribution plot, are saved in the `.images/` directory. The primary image is:

- **Poisson Distribution**: `.images/poisson_dist.png`

---

## **Project Structure**

```
├── Dockerfile             # Docker instructions for environment setup
├── scripts/               # Python scripts and Jupyter notebooks
│   └── analysis.ipynb     # Main analysis notebook
├── .images/               # Directory for output images
│   └── poisson_dist.png   # Poisson distribution plot
├── README.md              # Project documentation
└── requirements.txt       # Python dependencies
```

---

## **How to Reproduce Results**

1. Follow the steps to build and run the Docker container.
2. Open the Jupyter Notebook `analysis.ipynb`.
3. Run all cells to reproduce the simulation and analysis.
4. Generated plots, like `poisson_dist.png`, will automatically be saved to the `.images/` folder.

---

## **Dependencies**

Dependencies are managed via the `requirements.txt` file. These include:
- `numpy`: For simulations and numerical operations.
- `matplotlib`: For plotting.
- `pandas`: For data manipulation.
- `lifelines`: For survival analysis.

The Dockerfile automatically installs these dependencies when building the image.

---

## **Contact**

If you have any questions or feedback, feel free to reach out.