============================================
            SHOT PEENING SIMULATION
============================================

Project Title:
--------------
Shot Peening

Author:
-------
YENNI ANIRVIN

Objective:
----------
To simulate the mechanical effects of shot peening through:
1. Single shot – target interaction.
2. Multiple shots – target interaction.

Software Used:
--------------
- Abaqus/CAE

Materials Used:
---------------
- Shot: Mild Steel
- Target: Inconel 718 Alloy

Key Simulation Features:
------------------------
- Shot size
- Shot velocity
- Impact angle

File Contents:
--------------
The main project directory 'SP' contains the following subfolders:

1. **Single shot - target interaction**
   - Contains Abaqus input files (.inp) for single shot simulations.
   - Simulations vary by:
     - Shot size (sp_r0_25_v62_5.inp, sp_r0_5_v62_5.inp, sp_r1_v62_5.inp, sp_r1_25_v62_5.inp, size on s11_peeq.xlsx)
     - Shot velocity (sp_r1_v35.inp, sp_r1_v62_5.inp, sp_r1_v125.inp, abnormal_v600.inp, velocity on s11_peeq.xlsx)
     - Angle of impact (sp_A0.inp, sp_A45.inp, sp_A90.inp, Angle_of_impact on stress_peeq.xlsx)

2. **Multiple shots - target interaction**
   - Includes setups for:
     - `multi_9.inp` – simulation with 9 uniformly arranged shots
     - `multi_13.inp` – simulation with 13 shots
     -  S11_xedge_ydepth.xlsx (s11 and equivalent plastic strain along side edge and depth of the target)
   - Designed to evaluate residual stress and plastic strain from cumulative impacts.

3. **Results**
   - Contains output data (Power point presentation, .avi files, report plots, images, and CSVs) for both single and multiple shot simulations.

Usage Instructions:
-------------------
1. Open the desired subfolder (e.g., "Single shot - target interaction").
2. Ensure Abaqus working directory is set to the folder containing the `.inp` file.
3. Run the simulation using Abaqus/CAE:
   - From the command line:  
     `abaqus job=<filename> input=<filename>.inp`
   - Or, load the file in Abaqus/CAE GUI and submit the job.

Notes:
------
- Ensure your Abaqus environment is correctly configured before running.
- Results can be viewed in Abaqus/Viewer from the respective ODB files.
- Simulations were performed using explicit dynamics for impact accuracy.

============================================
