# Steel Plate Defect Prediction
* Kaggle Playground Series - Season 4, Episode 3
* https://www.kaggle.com/competitions/playground-series-s4e3/overview

# Introduction
* Objective: Predict the probability of various defects on steel plates.
* Evaluation Metrics: Area Under the ROC Curve
  
# Dataset introduction
* The dataset is related to Steel Plates Faults (https://archive.ics.uci.edu/dataset/198/steel+plates+faults)
* It is reported being donated to public in 2010 but with no reference papers and no much information.
* The dataset consists 27 variables, and steel plates' faults classified into seven different types. (Detailed description is in the dataset features description section)
* Some research papers have used this dataset for studies related to fault diagnosis / fault detection in steel plates using data mining models (Source: https://scholar.google.com/scholar?hl=en&as_sdt=0%2C5&q=%22Steel+Plates+Faults%22&btnG=)

# Dataset Features Description
* The competition dataset consists of 26 variables and 7 defects. (https://archive.ics.uci.edu/dataset/198/steel+plates+faults)
* The description is from https://www.kaggle.com/competitions/playground-series-s4e3/discussion/481006 .
1. X_Minimum: The minimum x-coordinate of a bounding box around a defect or feature on the steel plate.
2. X_Maximum: The maximum x-coordinate of a bounding box around a defect or feature on the steel plate.
3. Y_Minimum: The minimum y-coordinate of a bounding box around a defect or feature on the steel plate.
4. Y_Maximum: The maximum y-coordinate of a bounding box around a defect or feature on the steel plate.
5. Pixels_Areas: The total number of pixels within a defect or feature region.
6. X_Perimeter: The perimeter (boundary length) of a defect or feature along the x-axis.
7. Y_Perimeter: The perimeter (boundary length) of a defect or feature along the y-axis.
Sum_of_Luminosity: The sum of the luminosity (brightness) values of pixels within a defect or feature region.
8. Minimum_of_Luminosity: The minimum luminosity value within a defect or feature region.
9. Maximum_of_Luminosity: The maximum luminosity value within a defect or feature region.
10. Length_of_Conveyer: Length of the conveyor belt or platform on which the steel plates are transported.
11. TypeOfSteel_A300: Binary feature indicating whether the steel plate is of type A300.
12. TypeOfSteel_A400: Binary feature indicating whether the steel plate is of type A400.
13. Steel_Plate_Thickness: Thickness of the steel plate.
14. Edges_Index: Index indicating the ratio of the length of edges to the total length of the defect or feature boundary.
15. Empty_Index: Index indicating the ratio of empty spaces (background) to the total area of the defect or feature.
16. Square_Index: Index indicating the ratio of the area of the defect or feature to the area of the smallest square that encloses it.
17. Outside_X_Index: Index indicating the ratio of the pixels outside the defect or feature along the x-axis to the total area.
18. Edges_X_Index: Index indicating the ratio of edge pixels along the x-axis to the total number of edge pixels.
19. Edges_Y_Index: Index indicating the ratio of edge pixels along the y-axis to the total number of edge pixels.
20. Outside_Global_Index: Index indicating the ratio of the pixels outside the defect or feature to the total number of pixels in the image.
21. LogOfAreas: The logarithm of the area of the defect or feature.
22. Log_X_Index: Index indicating the logarithm of the ratio of the length of edges along the x-axis to the total length of edges.
23. Log_Y_Index: Index indicating the logarithm of the ratio of the length of edges along the y-axis to the total length of edges.
24. Orientation_Index: Index indicating the orientation of the defect or feature within the image.
25. Luminosity_Index: Index indicating the luminosity contrast between the defect or feature and its background.
26. SigmoidOfAreas: Sigmoid transformation of the area of the defect or feature.

* The prediction targets are as follows.
1. Pastry: A type of defect characterized by a pattern resembling the surface of pastry, often indicating irregularities in the steel plate surface.
2. Z_Scratch: A scratch or mark on the steel plate surface that appears in a Z shape.
3. K_Scratch: A scratch or mark on the steel plate surface that appears in a K shape.
4. Stains: Discolorations or blemishes on the steel plate surface caused by various substances.
5. Dirtiness: Presence of dirt or foreign particles on the steel plate surface.
6. Bumps: Raised areas or protrusions on the steel plate surface.
7. Other_Faults: A category representing any other types of faults or defects not covered by the previous labels.