# PETMAT: PET Image Preprocessing in MATLAB

![GitHub release (latest by tag)](https://img.shields.io/github/v/tag/taha-parsayan/PETMAT?label=Release)
![Static Badge](https://img.shields.io/badge/Neuroimaging%20software-FF0000)
![Static Badge](https://img.shields.io/badge/MATLAB-8A2BE2)
![Static Badge](https://img.shields.io/badge/SPM-8A2BE2)
![Static Badge](https://img.shields.io/badge/PET%20/%20MRI-4CAF50)

**PETMAT** is a MATLAB-based app designed to facilitate the preprocessing of Positron Emission Tomography (PET) images using the Statistical Parametric Mapping (SPM) toolbox. The app supports operations like smoothing, co-registration, and normalization of PET images and provides an intuitive interface to work with multiple subject datasets. 

![Toolbox](https://github.com/user-attachments/assets/89d34f3f-4425-418e-9d68-260dcc660526)


## Features

- **Smoothing**: Option to smooth the PET images with different Full Width Half Maximum (FWHM) kernels.
- **Co-registration**: Interpolation options for aligning PET images with anatomical scans.
- **Normalization**: Rescale images to standard space with interpolation options.
- **Multiple subjects**: Support for batch processing multiple subjects at once.
- **Progress tracking**: Real-time completion percentage indicator during the preprocessing.

![pipeline](https://github.com/user-attachments/assets/3eaf19bf-1c4c-4b85-8b69-b028a09a1275)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/taha-parsayan/PETMAT.git
    ```

2. Open MATLAB and navigate to the directory containing `PETMAT.m`.

3. Ensure that you have the SPM toolbox installed and added to the MATLAB path. You can download SPM from [SPM official website](https://www.fil.ion.ucl.ac.uk/spm/).

4. Run the app by executing:
    ```matlab
    app = PETMAT;
    ```

## Requirements

- MATLAB (R2018b or later recommended)
- SPM12 (must be installed and in the MATLAB path)
- NIfTI PET and anatomical image files

## Usage

1. **Input**: Specify the folder containing the subject PET image files and the subject IDs. PET files should be in NIfTI format (`.nii`) and the anatomical scan should be named `T1.nii`.

2. **Smoothing Options**: Choose the desired level of smoothing for the PET images from the list:
    - No smoothing
    - 5 FWHM
    - 8 FWHM
    - 10 FWHM

3. **Co-registration and Normalization**: Select the desired interpolation methods for co-registration and normalization processes.

4. **Analyze**: Click the "Analyze" button to start the preprocessing pipeline.

5. **Exit**: Close the app by clicking "Exit."

## Output

The processed images will be stored in the same subject directories, with names indicating the operation performed:
- `coregister_PET.nii`: Co-registered PET images
- `std_T1.nii`: Normalized anatomical scan
- `std_coregister_PET.nii`: Normalized PET image
- `SUV.nii`: Standard Uptake Value (SUV) image
- `SUV_GM.nii`: SUV image masked by gray matter

## Contributing

Contributions are welcome! If you encounter any bugs or have feature suggestions, feel free to open an issue or submit a pull request.

## Acknowledgments

This app utilizes the SPM toolbox, developed by the Wellcome Centre for Human Neuroimaging. For more information, visit the [SPM website](https://www.fil.ion.ucl.ac.uk/spm/).

## Citation

If you use this tool in your work, please cite it as:

Mohammadtaha Parsayan, Poul Flemming Høilund-Carlsen, Farzin Kamari, Abass Alavi, Sasan Andalib. PETMAT: A MATLAB-based PET Image Processing Tool. Version 2024-10. [cited (date)] . Available at: https://github.com.mcas.ms/taha-parsayan/PETMAT.
