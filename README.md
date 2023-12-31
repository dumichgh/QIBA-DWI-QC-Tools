# QIBA-DWI-QC-Tools
This repository contains QC tools and sample DICOM for QIBA DWI phantom (QIDW collection backup)

“ADC_SNR_DRO_DICOM” folder contains simulated trace-DWI DICOM (magnitude image) series 
generated by mono-exponential diffusion model for a range of tissue-relevant ADC and 
SNR values to evaluate performance of quantitative DWI analysis SW against ground truth.

"PVP_Phantom_QCpcombo_R3" folder contains "p-code" combo-scripts with pre-compiled 
Matlab (R2019b+) libraries for QC analysis of QIBA/NIST polyvinylpirrolydone (PVP) 
multi-ADC phantom and DICOM (demo) samples. The manual has step-by-step instructions to 
generate QC stats (bias, precision and SNR) for phantom ADC.
