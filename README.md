# 🌋 MinGeoChem

### Mineralogical, Crystallographic and Geochemical Visualization Tool

**MinGeoChem** is an interactive educational application developed with Python and Streamlit, designed to integrate optical mineralogy, crystallography, and thermodynamic calculations into a single environment.

The application provides tools for exploring optical mineral properties, visualizing crystallographic systems in 3D, evaluating thermodynamic reactions, and generating pressure–temperature phase diagrams using the Clapeyron equation.

Developed by **Ernesto Álvarez**.

---

## 1. Features

MinGeoChem currently includes six main modules:

### 📖 1. Optical Mineralogy Atlas

An interactive mineralogical database focused on optical properties and petrographic identification.

Features:
- Mineral selection and individual mineral profiles.
- Chemical formula visualization.
- Optical properties, including:
  - Habit and cleavage.
  - Twinning.
  - Color and pleochroism.
  - Relief.
  - Refractive indices (Ng, Nm, Np).
  - Birefringence.
  - Interference colors and additional optical characteristics.
- Reference photomicrographs under:
  - Plane-Polarized Light (PPL).
  - Cross-Polarized Light (XPL).

### 📐 2. 3D Crystallographic Symmetry Visualizer

Interactive visualization of the seven crystal systems.

Supported systems:
- Cubic (Isometric).
- Tetragonal.
- Orthorhombic.
- Monoclinic.
- Triclinic.
- Trigonal (Rhombohedral).
- Hexagonal.

The module represents crystallographic axes and unit-cell geometry using interactive 3D graphics.

### 🧪 3. Geochemical and Thermodynamic Calculator

A thermodynamic calculation environment for evaluating mineral reactions and phase stability.

Features:
- Gibbs free energy calculation (ΔG).
- Hess's Law.
- Heat capacity integration (Cp).
- Temperature-dependent enthalpy (ΔH) and entropy (ΔS).
- Comparison of reactants and products.
- Polymorphic phase-transition calculations.
- Clapeyron equation integration.

### 🌋 4. P–T Phase Diagram Generator

Generates pressure–temperature phase boundaries using the Clapeyron equation:

\[
\frac{dP}{dT}=\frac{\Delta S}{\Delta V}
\]

Features:
- Calculation of phase boundaries.
- Temperature-dependent thermodynamic properties.
- Polymorphic transition visualization.
- Interactive pressure–temperature diagrams.
- Triple-point and phase-equilibrium exploration.
- Gibbs phase rule calculator:

\[
F=C-P+2
\]

### 🎮 5. Mineralogical Identification Quiz

An interactive learning module designed to reinforce optical mineral identification through microscope imagery.

### ⚙️ 6. Custom Database Import

Allows users to upload their own CSV databases and use them throughout the application.

Supported databases:
- Optical mineralogy database.
- Geochemical and thermodynamic database.

Uploaded datasets are managed through Streamlit session state.

---

## 2. Technology Stack

MinGeoChem is built using the following Python libraries:

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Interactive web application |
| Pandas | Database management and data processing |
| NumPy | Numerical operations |
| SciPy | Numerical integration and scientific calculations |
| Plotly | Interactive 3D visualization and phase diagrams |

---

## 3. Installation

### Requirements

- Python 3.10 or newer recommended.
- pip package manager.
- Git.

### Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/MinGeoChem.git

cd MinGeoChem
```

### Install dependencies

```bash
pip install streamlit pandas numpy scipy plotly
```

Alternatively, create a `requirements.txt` file containing:

```txt
streamlit
pandas
numpy
scipy
plotly
```

Then install:

```bash
pip install -r requirements.txt
```

### Run the application

```bash
streamlit run app.py
```

The application will be available locally at:

```text
http://localhost:8501
```

---

## 4. Database Structure

MinGeoChem uses two independent CSV databases.

### Optical Mineralogy Database

Default filename:

`minerales_ugr_FINAL.csv`

Required columns:

| Column | Description |
|---|---|
| Mineral | Mineral name |
| URL | Reference URL |
| Imagenes | Image references |
| Texto | Mineralogical and optical descriptions |

The application processes the mineral descriptions to extract individual optical properties.

**Data attribution:** University of Granada. Users should retain the original source attribution and verify the applicable image and database reuse permissions before redistribution.

### Thermodynamic Database

Default filename:

`database.csv`

Required columns:

| Column | Description |
|---|---|
| Phase | Mineral or thermodynamic phase |
| Formula | Chemical formula |
| DeltaH | Standard enthalpy |
| DeltaS | Standard entropy |
| Volume | Molar volume |
| a | Heat capacity coefficient |
| b | Heat capacity coefficient |
| c | Heat capacity coefficient |

Numerical fields are converted during database loading.

**Important:** The thermodynamic database must be supplied separately if it is not included in the repository. Its units and thermodynamic reference conditions must be documented to ensure physically consistent calculations.

---

## 5. Project Structure

Recommended repository organization:

```text
MinGeoChem/
│
├── app.py
│
├── minerales_ugr_FINAL.csv
├── database.csv
│
├── requirements.txt
│
├── README.md
│
├── assets/
│   └── images/
│
└── .gitignore
```

---

## 6. Scientific Scope and Limitations

MinGeoChem is primarily an educational and exploratory scientific tool.

Its calculations and visualizations should be interpreted considering the assumptions and limitations of the underlying thermodynamic database.

In particular:

- Thermodynamic calculations depend on the quality and completeness of the input data.
- Phase boundaries depend on the selected thermodynamic parameters and integration conditions.
- The application does not replace experimental measurements or validated thermodynamic modeling software.
- Results should be independently verified before being used in scientific publications or professional geological assessments.

---

## 7. Future Development

Potential improvements include:

- Expanded mineralogical and thermodynamic databases.
- Additional mineral groups and solid-solution models.
- Improved phase-equilibrium calculations.
- Advanced crystallographic visualization.
- Mineral assemblage stability analysis.
- Export of thermodynamic results and diagrams.
- Integration with external geological and geochemical datasets.
- Improved data validation and uncertainty analysis.

---

## 8. Contributing

Contributions, bug reports, scientific feedback, and feature suggestions are welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a feature branch.
3. Implement and test your changes.
4. Submit a pull request describing the modifications.

---

## 9. License

The project license has not yet been specified.

Before distributing the repository, a license should be selected for the application code. Database and image permissions should be handled separately.

---

## 10. Acknowledgements

MinGeoChem was developed as an independent scientific programming project combining concepts from mineralogy, optical petrography, crystallography, and geochemical thermodynamics.

Special acknowledgement to the University of Granada for the optical mineralogical reference database.

---

**MinGeoChem — Bridging Mineralogy, Crystallography and Geochemical Thermodynamics.**
