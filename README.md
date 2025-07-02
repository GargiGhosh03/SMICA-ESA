# SMICA-ESA


---

## 🧪 What This Project Does

- ✅ Extracts 2D gnomonic sky patches from the **B-mode** polarization map.
- ✅ Trains a PyTorch **autoencoder** to detect structural anomalies.
- ✅ Computes a **local variance map** to detect statistical inhomogeneities.
- ✅ Compares **B-mode anomalies** with those from **E-mode** and **T-mode**.
- ✅ Saves anomaly patch images and analysis results for downstream use.

---

## 📡 Dataset

- **Source**: [Planck Legacy Archive – SMICA CMB IQU maps](https://pla.esac.esa.int/#maps)
- **File used**: `COM_CMB_IQU-smica_2048_R3.00_full.fits`
- Resolution: NSIDE=2048 HEALPix format.

> Ensure you have this file in `data/` before running the notebooks.

---

## 🧠 Techniques Used

| Task                    | Methods                                 |
|-------------------------|-----------------------------------------|
| Patch extraction        | `healpy.gnomview()` (64×64 patches)     |
| Preprocessing           | MinMaxScaler, Flatten                   |
| Anomaly Detection       | Autoencoder (PyTorch)                   |
| Statistical Anomaly     | Variance map + μ + 2σ threshold         |
| Visualization           | Mollweide map, patch histograms         |
| Optional                | Isolation Forest / Clustering           |

---

## 🧰 Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/yourusername/cmb-bmode-anomaly.git
cd cmb-bmode-anomaly
