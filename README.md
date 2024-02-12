# 2024-URSI-NRSM-1265
Repository for code featured in "Machine Learning Assisted Optimization Methods for Automated Antenna Design" presented at the 2024 United States National Committee of URSI National Radio Science Meeting (USNC-URSI NRSM), Boulder, CO, USA. 

## Table of contents
* [Requirements](#requirements)
* [How to Use](#how-to-use)
* [Dataset](#dataset)
* [Tutorials](#tutorials)
    * [Tutorial 1: Google Colab and the Dataset](#tutorial-1)
    * [Tutorial 2: Manipulating the Dataset and Filtering](#tutorial-2)
    * [Tutorial 3: Support Vector Machines](#tutorial-3)
    * [Tutorial 4: Neural Networks](#tutorial-4)
    * [Tutorial 5: Fuzzy Logic and Rule-Based Approaches](#tutorial-5)
* [Related Publications](#future-work)
* [Resources](#resources)


## Requirements
* This project is designed to run in Google Colab with Jupyter Notebook. You must have a Google account to run these tutorials as-is. 


* Library requirements for each tutorial may vary. Refer to a tutorial for the specific requirements.


## How to Use
* To run, you will need to create a folder in your Google Drive, and add the dataset ('colab_dataset_microstrip') and all tutorials into the same folder.

## Dataset
There is one, cleaned dataset included in the repository. These data have been sampled from the larger AntennaCAT set for the purpose of demonstration of machine learning techniques. The set is unbalanced, with 2 classes having ~10k samples, and the third having ~7k.

Data in these sets are all simulated with copper ground planes, copper conductors, and with FR4 substrate (permitivity: 4.4). The first row in the csv file is the labels for each columns. Every row after that is data from one simulation.

In 'colab_dataset_microstrip', there are 27026 simulation entries with 13 columns. The microstrip width is held constant at 3 mm for a 50 ohm impedence match. The gap between the strip and the patch is held constant at 1 mm.

The thirteen columns in the .cvs are:
 1.   "target_freq": the target design frequency in Hz. There are 3 frequencies (classes): 1.5 GHz, 2.4 GHz, 5.8 GHz.
 2.   "$width": the width of the patch in mm.
 3.   "$length": the length of the patch in mm.
 4.   "$depth": the depth of the substrate in mm.
 5.   "$ground_plane": the value in mm for the length and width of the ground plane square.
 6.   "$x_0": the notch depth/feed point of the patch in mm.
 7.   "max_total_gain": maximum total simulated gain in dB.
 8.   "max_total_directivity": maximum total simulated directivity in dB.
 9.   "min_s11_f": the frequency for the lowest return loss value in dB (does not need to be the target frequency). This is not necessarily the target or local resonance.
 10.   "min_s11_dB": the lowest return loss value in dB for the frequency above.
 11.   "s11_at_target": the value of the return loss at the target frequency in dB.
 12.   "local_resonance_f": the frequency of the closest resonance to the target resonance in Hz.
 13.   "local_resonance_dB": the return loss of the local resonance in dB.


## Tutorials
#### Tutorial 1: Google Colab and the Dataset
This tutorial covers using Google Colab, Jupyter Notebook, and the dataset in Google drive. If you have not used Jupyter Notebook with Google Colab, then this will show you how to mount your Google Drive and open .csv files for data processing. References for Colab and Jupyter Notebook are included.

#### Tutorial 2: Manipulating the Dataset and Filtering
Building off the first tutorial, this will discuss how to manipulate and filter the dataset. The data collected is from >26k simulations that used a parameter sweep for the CAD file dimensions. Not all parameter combinations results in valid antenna designs.

#### Tutorial 3: Support Vector Machines
Using data filtered for valid designs, Support Vector Machines (SVMs) are used to classify the data into different categories.

#### Tutorial 4: Neural Networks
Using data filtered for valid designs, Neural Networks (NNs) are used to classify the data into different categories.

#### Tutorial 5: Fuzzy Logic and Rule-Based Approaches
This tutorial does not use the full dataset because it requires a simulation loop in the current process. However, several examples for fuzzy classification and a rules-based approach are shown.


## Related Publications

L. Linkous and E. Topsakal, "Machine Learning Assisted Optimization Methods for Automated Antenna Design," 2024 United States National Committee of URSI National Radio Science Meeting (USNC-URSI NRSM), Boulder, CO, USA, 2024.

L. Linkous, E. Karincic, J. Lundquist and E. Topsakal, "Automated Antenna Calculation, Design and Tuning Tool for HFSS," 2023 United States National Committee of URSI National Radio Science Meeting (USNC-URSI NRSM), Boulder, CO, USA, 2023, pp. 229-230, doi: 10.23919/USNC-URSINRSM57470.2023.10043119.

L. Linkous, J. Lundquist and E. Topsakal, "AntennaCAT: Automated Antenna Design and Tuning Tool," 2023 IEEE USNC-URSI Radio Science Meeting (Joint with AP-S Symposium), Portland, OR, USA, 2023, pp. 89-90, doi: 10.23919/USNC-URSI54200.2023.10289238.


## Resources

#### Tutorial 1: Google Colab and the Dataset
* https://jupyter.org/https://colab.research.google.com/?utm_source=scs-index
* https://jupyter.org/
* https://www.geeksforgeeks.org/how-to-use-gpu-in-google-colab/ 
* https://www.tutorialspoint.com/google_colab/google_colab_using_free_gpu.htm
* https://www.datacamp.com/tutorial/pandas-read-csv
* https://matplotlib.org/
* https://matplotlib.org/stable/plot_types/basic/scatter_plot.html#sphx-glr-plot-types-basic-scatter-plot-py 

#### Tutorial 2: Manipulating the Dataset

#### Tutorial 3: Support Vector Machines

#### Tutorial 4: Neural Networks

#### Tutorial 5: Fuzzy Logic and Rule-Based Approaches

