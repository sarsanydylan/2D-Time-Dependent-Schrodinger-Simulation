# 🧠 2D Time-Dependent Schrödinger Equation Simulation

This project numerically solves the 2D Time-Dependent Schrödinger Equation (TDSE) using the **split-step Fourier method**.  
It visualizes the time evolution of quantum wave packets under different potential energy surfaces.

## ✨ Features
- Real-time visualization of |ψ(x, y, t)|²
- Choose between **Harmonic** and **Double-Well** potentials
- Interactive controls via **ipywidgets**
- Animated probability density and 3D surface plots
- Probability current visualization (quantum flux arrows)

## ⚙️ How It Works
The TDSE is:
\[
i \hbar \frac{\partial \psi}{\partial t} = -\frac{\hbar^2}{2m} \nabla^2 \psi + V(x,y)\psi
\]

This code uses the **split-step Fourier method**:
1. Apply half-step potential evolution in position space  
2. Transform to momentum space (FFT)
3. Apply kinetic term
4. Transform back (IFFT)
5. Apply second half potential step

This is unconditionally stable and widely used in quantum dynamics simulations.

## 📊 Visualization Outputs
- 2D heatmaps of |ψ|²  
- 3D surface plots showing spatial probability density  
- Quiver plots of probability current density

## 🚀 Example Usage
Open in Jupyter and run all cells.  
Adjust sliders and click **“Run TDSE”**.

```python
run_tdse('Harmonic', k_strength=50, sigma=0.3, kx0=20, ky0=0)
