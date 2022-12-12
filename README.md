# Y4-Project

## Machine Learning Applications in Radio Astronomy Surveys - Christopher Lenthall, University of Birmingham

***

**Note:** all of the code for this project is in the form of Jupyter Notebooks, since it is convenient both for display purposes (the outputs have been saved) and for my own purposes (use of markdown cells to record methods/future plans).

***

## **Description of Notebooks:**

### 1. Preliminary assessment of the Aegean Source Tables

*Code:* 1. Aegean Dataset Properties, Combination of Sources.ipynb

This notebook contains an initial assessment into the structure of the source tables produced using the Aegean source detection algorithm. It comprises two main analyses: an investigation into the areas of the sources, and a short exercise in source table manipulation, where the island with the most sources is selected from the overall table. It uses an example source table chosen arbitrarily. 

### 2. Isolating the multi-source islands (MSIs)

*Code:* 2. Flattening the source tables.ipynb

This notebook contains a method for removing all of the single-source islands from an arbitrarily chosen source table (operating under the assumption that the most interesting sources such as radio galaxies will be represented as islands with >1 source). It includes two methods, one which preserves a single coordinate per island (selected randomly), and a second improved method which computes the average coordinate value for each multi-source island (MSI), allowing for better cutouts around the centroid of each island (see notebook 3).

### 3. Creating an initial training set

*Code:* 3. Creating Preliminary Training Set from MeerKAT.ipynb

This notebook contains an initial attempt to use the source tables containing only MSIs produced by the above method to create cutouts from the MeerKAT FITS files for a training set for our neural networks, with an example MSI chosen arbitrarily.

### 4. Investigating more of the properties of the Aegean Source Tables

*Code:* 4. Source Table Properties.ipynb

This incomplete notebook contains the initial groundwork for an ongoing investigation into more of the properties of the source tables, specifically data such as the overall distribution of MSIs. This is to help to interrogate the earlier assumption that the most interesting sources are MSIs (see notebook 2).

***

## Other code:

Saved locally (i.e. **not** in this repository) are other notebooks, created mostly to help aid my understanding of the basic processes involved, such as FITS file manipulation. These were not uploaded due to the fact that most of the results from these are used elsewhere in the aforementioned notebooks. 
