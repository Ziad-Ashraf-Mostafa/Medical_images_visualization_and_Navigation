# Medical_images_visualization_and_Navigation
A unity App for medical images Visualization and navigation Techniques

# Organ Visualization and Navigation

## Overview
This project provides an interactive 3D visualization and navigation tool for biomedical imaging data, built using Unity.  
It is designed to handle NIfTI (`.nii` / `.nii.gz`) datasets and visualize anatomical structures such as organs or limbs through slice-based planes and camera navigation techniques.

The goal is to create an efficient, user-friendly environment for exploring volumetric medical data, suitable for both educational and research purposes.

This a student's project in Biomedical Engineering Department, Cairo University.
It is not intended for clinical diagnostic use.

---

## Features
- Load and visualize 3D NIfTI medical volumes (CT or MRI)
- Interactive control of axial, coronal, and sagittal planes using UI sliders
- Adjustable clipping through normalized slice indices
- Switchable camera perspectives for free navigation and focused exploration
- Modular architecture for extending to curved MPR or segmentation overlays

---

## System Requirements
- **Unity Version:** 2022.3 LTS or newer  
- **Scripting Backend:** C# (.NET 6)  
- **Packages Used:**
  - UnityEngine.UI  
  - Unity Splines (for camera paths)  
  - Custom NIfTI Loader (Python or C# integration)  
  - Optional: Cinemachine (for camera control)

---

## Folder Structure



---

## How It Works
1. **Volume Loading**  
   The `NiftiLoader` script reads a 3D NIfTI file and converts it into a Unity `Texture3D` or a stack of 2D slices.

2. **Slice Visualization**  
   Each plane (axial, coronal, sagittal) uses a shader or material with a `_NormalizedPosition` property.  
   The `PlaneSliceController` script updates this property according to the value of the corresponding UI slider.

3. **Camera Switching and Navigation**  
   The `CameraSwitcher` script toggles between two predefined cameras (e.g., overview and fly-through) based on UI checkboxes or buttons.

---

## Usage
1. Open the Unity project and load the **MainScene**.  
2. Assign the NIfTI file path in the `NiftiLoader` script or drag the preprocessed `Texture3D` into the inspector.  
3. Run the scene and use the sliders to navigate through slices on each anatomical plane.  
4. Use the camera toggle to switch between different perspectives.

---

## Future Enhancements
- Curved MPR (Multi-Planar Reconstruction)
- 3D volume rendering using shaders
- Region-of-interest (ROI) selection and annotation tools
- Integration with PyVista or ITK for external processing

---

# Contributors and Contact
Hakeem Mohammed	Taha  -  hakeem.taha06@eng-st.cu.edu.eg

Ahmed Mamdouh Anan   -   ahmedmamdouhenan18@gmail.com

Ziad Ashraf Mostafa   -  ziad.abd-elawad06@eng-st.cu.edu.eg

Yahya Ismail      -      yahya.ismail06@eng-st.cu.edu.eg


***Supervised by*** Prof. Tamer Basha - tamer.basha@eng1.cu.edu.eg

Feel free to suggest any code enhancements or features addition or suggest contribution to make it real-world for clinical use app

---

## License
This project is developed for academic and research purposes within the Biomedical Engineering Department, Cairo University.  
It is not intended for clinical diagnostic use.
