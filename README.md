# IslandMaker

This was a collaborative effort with [Grady Peck](https://github.com/GradyPeck), done largely for coding practice. The code uses Perlin noise to create a semi-random 2d heightmap array and then creates additional arrays simulating water flow and pooling to generate streams and ponds. The result is a fairly realistic semi-random "island."

## Guide to Files

IslandMaker currently consists of four .ipynb files (Jupyter Notebooks) and a folder (TestIslands) containing three .png files. The Jupyter Notebooks include the current version of the code and three previous versions which were created before I was using Git properly. Full descriptions of the files are as follows:
- PerlinGroundwork.ipynb: this is the initial version of the code for the Perlin noise and layering on a dome to create the basic island shape, saved as a backup reference. Code is not commented and should not be run. 
- PerlinPandas.ipynb: this is a previous start on the code using Pandas; clearly not the best tool for the job but I needed Pandas practice. The difficulty of modeling water flow in this version led to it quickly being abandoned. Kept only as a monument to hubris. 
- PerlinObjects.ipynb: this file represents the initial rewrite after Pandas was abandoned and the code was entirely rebuilt to make better use of custom classes. This version got much further than PerlinPandas.ipynb but was plagued by long-running, difficult to isolate bugs. Kept as a backup reference and should not be run unless you want to see some really weird, bugged-out water flows. 
- PerlinFunctional.ipynb: this is the current, fully-functional version of the code. Previously named PerlinCursed, this version was exported as a .py file and debugged line by line in VS Code until issues were isolated and solved, at which point changes were brought back into Jupyter and it received its "blessed" sobriquet. The last few cells are an incomplete attempt to make high-volume rivers widen, and are currently uncommented. 
- The TestIslands files can be read in after the island creation stage of the code to test specific functionality in a controlled environment. To use them, uncomment the test cell (cell 12) in PerlinFunctional.ipynb and comment out the following inundation cell (cell 13). Change the test file used by altering the "test_island" assignment at the top of the test cell. The default test file is TestIsland3.png. 

## Requirements

For the current version of the code (PerlinFunctional.ipynb) to run properly, it requires Python 3 and the following modules:
- JupyterLab or Jupyter Notebook
- matplotlib.pyplot
- numpy
- noise
- skimage.io
- skimage.morphology
- skimage.filters
