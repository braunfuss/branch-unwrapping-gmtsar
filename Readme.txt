

This script unwrappes GMTSAR outputs with the 2D Goldstein branch cut phase unwrapping algorithm in octave, with one sign direction only so far.
So a positive or negative change will be forced.


You will have to use octave v.4.0 (https://www.gnu.org/software/octave/) or better. 
Please install if not already installed the following octave packages:

image and netcdf

by using the following commands in octave:


pkg install -forge image

pkg install -forge netcdf




 References::
 1. R. M. Goldstein, H. A. Zebken, and C. L. Werner, �Satellite radar interferometry:
    Two-dimensional phase unwrapping,� Radio Sci., vol. 23, no. 4, pp. 713�720, 1988.
 2. D. C. Ghiglia and M. D. Pritt, Two-Dimensional Phase Unwrapping:
    Theory, Algorithms and Software. New York: Wiley-Interscience, 1998.

 Inputs: 1. Correlation threshold, e.g. 0.12
         2. Area to be unwrapped. A single 1 for the entire scene, e.g. unwrap_branchcut(0.12, 1)
         Else give the area as e.g. 1000:1500 for x and y directions. 
         e.g. unwrap_branchcut(0.12, 1000:1500, 1000:1500)
         3. Image input are assumed to be grds from GMTSAR and are converted. [Using a modified version of GRDREAD2 from Kelsey Jordahl]
                     
 Outputs: Figures: Unwrapped phase image, phase residues, wrapped phase and branch cuts
          

 Redone for use with InSAR (GMTSAR outputs) and octave by Andreas Steinberg, 27.6.2016 
 Unwrapping algorithms by Bruce Spottiswoode on 22 December 2008 (de.mathworks.com/matlabcentral/fileexchange/22504-2d-phase-unwrapping-algorithms)


