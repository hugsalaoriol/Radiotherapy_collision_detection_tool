# Radiotherapy Collision Detection Tool

This repository contains a Python-based Jupyter Notebook tool developed during my internship at **Hospital Clínic de Barcelona**. It is designed to help radiophysicists detect and prevent collisions between the **gantry**, **patient**, and **immobilization equipment** during external radiotherapy treatments.

---

## 🏥 Background

During external beam radiotherapy, especially in treatments involving complex positions (e.g. raised arms or inclined torso), **collisions** between the rotating gantry and the patient or couch can occur. These incidents can:
- Interrupt treatment,
- Require a complete replanning of fields and isocenter,
- Delay the patient’s session and use of the LINAC.

Despite existing commercial solutions, this hospital lacked an integrated tool. This notebook-based tool was developed in collaboration with the Radiophysics Department to anticipate and avoid such collisions during the **planning phase**.

---

## 🎯 Objectives

- Load CT scans and associated structure contours (RTSTRUCT DICOMs).
- Create masks for relevant structures: **body**, **couch**, **immobilizers**, etc.
- Simulate the gantry’s rotational path based on user-defined parameters (isocenter position, couch angle, gantry radius).
- **Detect collisions** by checking overlaps between the gantry path and anatomical structures.
- Highlight the collision zones directly on the CT slices.
- Offer **three analysis modes**:
  1. **Full-volume mask check**
  2. **Slice-by-slice layered analysis**
  3. **Single-slice zoomed collision inspection**

---

## 📂 Contents

```
Radiotherapy_Collision_Detection/
├── collision_analysis.ipynb              # General-purpose notebook for loading and analyzing any patient case
├── requirements.txt                      # Python dependencies
├── results/
│   └── report.pdf                        # Final internship report with visuals
└── data/                                 # DICOM and patient-specific notebooks
    ├── 0000/                             # CT slices for patient 0000
    ├── 0001/                             # CT slices for patient 0001
    ├── 0003/                             # CT slices for patient 0003
    ├── 0004/                             # CT slices for patient 0004
    ├── RS0000.dcm                        # RTSTRUCT file for patient 0000
    ├── RS0001.dcm                        # RTSTRUCT file for patient 0001
    ├── RS0003.dcm                        # RTSTRUCT file for patient 0003
    ├── RS0004.dcm                        # RTSTRUCT file for patient 0004
    ├── pacient_collision_0000.ipynb      # Individual analysis for patient 0000
    ├── pacient_collision_0001.ipynb      # Individual analysis for patient 0001
    ├── pacient_collision_0003.ipynb      # Individual analysis for patient 0003
    └── pacient_collision_0004.ipynb      # Individual analysis for patient 0004 
                           
```

---

## ▶️ How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/hugsalaoriol/radiotherapy-collision-detection.git
   cd radiotherapy-collision-detection
   ```

2. (Optional) Create and activate a virtual environment:

   ```bash
   python3 -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. Install required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch the general notebook or a patient-specific notebook:

   ```bash
   jupyter notebook collision_analysis.ipynb
   # or
   jupyter notebook data/pacient_collision_0000.ipynb
   ```

---

## 📌 Notes

- This repository provides an overview and documentation of the tool, but **the source code is private**.
- This is due to the use of **real patient DICOM data** and the fact that the application was developed **exclusively for internal use at Hospital Clínic de Barcelona**.
- For academic or institutional collaboration inquiries, feel free to contact me.

---

## 👨‍⚕️ Developed During Internship

- **Institution:** Hospital Clínic de Barcelona — Radiophysics Department  
- **Duration:** September to December 2024  
- **Tutor:** Cristian Candela Juan  
- **Student:** Hug Sala Oriol  
- **Degree:** BSc in Physics (University of Barcelona)  

---

## 📫 Contact

**Hug Sala Oriol**  
📧 hsalaoriol@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/hug-sala-oriol-b31280268)

---

*This project contributes to improving patient safety and planning efficiency in clinical radiotherapy.*
