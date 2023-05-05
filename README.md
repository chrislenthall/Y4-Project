# Y4-Project

## Machine Learning Applications in Radio Astronomy Surveys - Christopher Lenthall, University of Birmingham

***

**Note:** all of the code for this project is in the form of Jupyter Notebooks, since it is convenient both for display purposes (the outputs have been saved) and for my own purposes (use of markdown cells to record methods/future plans).

***

## **Description of Notebooks (semester 1):**

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

## **Description of Notebooks (semester 2):**

### 4b. Investigating more of the properties of the Aegean Source Tables

*Code:* 4b. Source Table Properties.ipynb

This notebook is the completed version of notebook 4. The distributions of all sources and MSIs are plotted individually, showing that both simple and complex sources are more abundant further from the galactic centre.

### 5. Combining the source catalogues

*Code:* 5. Combined MSI Catalogue.ipynb

This notebook contains a method for combining the 58 individual MSI source catalogues. It also adds a column for frame name, sorts all sources by longitude, and assigns a MeerACS ID number to every MSI.

### 6. Producing MSI cutouts from the whole survey

*Code:* 6. Creating a Full Training Set.ipynb

This notebook contains the method through which the complete set of cutouts was produced. This entailed extracting a list of MSI coordinates for a particular frame from the overall source table, reading in the relevant FITS file, converting from galactic coordinates to matrix coordinates, and looping the cutout routine through these coordinates. The method for normalising these images is also shown.

### 7. Search for object coordinates via MeerACS ID

*Code:* 7. Source Search Function.ipynb

This notebook contains a concise method for finding the coordinates of a particular source by its MeerACS ID, from the overall MSI table. This was used extensively throughout the analysis stage of the project.

***

## Other code:

Saved locally (i.e. **not** in this repository) are other notebooks, created mostly to help aid my understanding of the basic processes involved, such as FITS file manipulation. These were not uploaded due to the fact that most of the results from these are used elsewhere in the aforementioned notebooks. 
