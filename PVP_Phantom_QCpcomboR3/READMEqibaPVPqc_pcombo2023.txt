The "p-code" combo-scripts contain pre-compiled Matlab libraries for QC
analysis of QIBA/NIST PVP/ADC phantom in Matlab R2019+ versions.

!! NEW 2023 (_R3): the script requires input of phantom temeprature (in oC) 
		  for ambient temeprature runs.  For ice-water, use "0" for input.

The "qiba_build_combo" and "run_PVP_qc_combo" p-functions can be directly 
utilized by Matlb users (wo/installation of Matlab runtime libraries).

USAGE:  (1) copy the p-functions in the directory in your Matlab "userpath"
	(2) Change extention of "masterDNA.." to ".mat" (from "tam") and 
	    copy anywhere close to DICOM directory that you intend to process.
            NOTE: "masterDNA...mat" is used for protocol compliance check.
	(3) run "qiba_build" from Matlab workspace following instructions 
	    from the the "qiba_build_USAGE" manual in place of the "exe" routine.
	    NOTE: it will create “SD*scan-date*DataStructsBin” folder with scan 
	          DWI and ADC mat-structures for the QC analysis
	(4a) (skip "qiba_proc") directly run "run_PVP_qc" (!!) from within (!!)
	    “SD*DataStructsBin” folder. It will ask to select slice ranges to QC
	    and save the PDF reports “*_QC_Summary.pdf” and “*_DWI_SNR.pdf”
	    with performance metrics to use for QIBA DWI profile "device checklist".
	    NOTE: 2023 update enabled !!room-temperature!! PVP-ADC bias analysis with respect
	    	  to NIST ADC values using universal Temperature-Concentration calibration
	    	  (Med.Phys.2022; p:3325-3332 (Amouzandeh, et al))
	(4b) For single-tube ice-water phantom or arbitrary geometry, run "qiba_proc" 
	     according to PDF-manual and use "master...IceWater.mat" for protocol QC.
	     NOTE: only CSV output stats (for individual ROI) will be generated, 
	           and no summary report available.
	 
