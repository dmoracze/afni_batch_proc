# TCSH shell scripts for batch processing in AFNI

These scripts were inspired by [afni_proc.py](https://afni.nimh.nih.gov/pub/dist/doc/program_help/afni_proc.py.html) and written with the intention of batch processing dataset within the DSCN lab. See the full documentation in the lab's documentation folder.

Below is an outline of the purpose of each script in chronological order. Each script has many options, see the documentation and individual script's help to see full functionality options.

* s0.updates.txt

List of updates for all scripts.


* s.update

Download the master versions of the preprocessing scripts into your study's directory


* dl.data

Download the raw DICOM data from the fmri.umd.edu data server.


* s1.dataset

Convert the raw DICOM data into AFNI-readable datasets (currently .HEAD/.BRIK) and begin the preprocessing file structure


* s2.make_spec

Between s1.dataset and s2.make_spec, those who wish to run Freesurfer should. This script converts the final recon-all data into SUMA surface mesh for the potential of surface-based analysis.



* s3.*preproc_script*

Four preprocessing pipelines to choose your own adventure! Processing supported for resting state (e.g., with tissue nuisance regression), task, surface-, and volume-based analysis.


* s4.motion

A multifaceted script for head motion analysis that will make your life *much* easier. This script will generate regressors for 1st-level regression, a log file with head motion info, or use my favorite option: the .csv option to get head motion information in batch to read into your favorite spreadsheet or analysis software.


* s5.decon

*This is a template script for 1st level regression analysis. Because each study is unique, this script is not meant to be a plug and play tool*