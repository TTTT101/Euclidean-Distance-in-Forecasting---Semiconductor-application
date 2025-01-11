# Euclidean-Distance-in-Forecasting-the-Nearest---Semiconductor-Manufacturing
Known as the most common used metric in computer science, physics and maths for determining the distance between two points, the Euclidean Distance has various applications in machine learning, computer vision, physics and geometry. Some popular use-cases include clustering algorithms such as K-means and NNC, measuring similarity among features, or finding the shortest paths.

Formula for Euclidean Distance:
Given two points \( p = (p_1, p_2, \dots, p_n) \) and \( q = (q_1, q_2, \dots, q_n) \) in \( n \)-dimensional space, the Euclidean distance \( d(p, q) \) is calculated as:

\[ d(p, q) = \sqrt{(q_1 - p_1)^2 + (q_2 - p_2)^2 + \dots + (q_n - p_n)^2} \]

**Example in 2D Space:**

If \( p = (x_1, y_1) \) and \( q = (x_2, y_2) \), the distance is:

\[ d(p, q) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2} \]

**Example in 3D Space:**

If \( p = (x_1, y_1, z_1) \) and \( q = (x_2, y_2, z_2) \), the distance is:

\[ d(p, q) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2} \]


<div align="center">
  <img src="![istockphoto-1167267132-612x612](https://github.com/user-attachments/assets/dcf62277-0fcf-44c7-9e57-86adf6416ca5)" alt="Example Image" width="500">
</div>


![istockphoto-1167267132-612x612](https://github.com/user-attachments/assets/dcf62277-0fcf-44c7-9e57-86adf6416ca5)




Semiconductor manufacturing use 300mm diameter wafer, and chips (dies) are arranged on each wafer by grid pattern. Therefore, optimizing the space on a wafer can increase the number of dies and reducing waste. However, the shrinking of nodes lead to the very complicated die packages and fabrication processes. Which in turn increase the dies coordinates to million posibilities. Whenever a new demand signal arrives, new dies are added without the sizes. We only know the high level of what customer wants. Thus, finding correct die layouts is not only significant for downstream planning but also turns into time consuming and excel crashing without the help of tool such as Python.

Just two years ago, engineers still look into individual package to find the correct die sizes for any new chip - one by one. This process can take upto 7 days depending on how many new products are added. With this implementation of Euclidean Distance written any run on Python, the entire process drops to 2 hours from preparing the data to send out the report. The script itself only takes 2 minutes to run.

## Data Description
The data has two parts. The first one is provdied in csv format individually for 33 packages technology. I then combine them into the "PLA" dataframe which has 2,344,400 rows and 29 columns. The second part is the new dies in our demand signal called "Items". Items' size is varied from 200-300 rows and 26 columns.

In reality, raw data often requires a lot of clean up. So, the first parts of my script is to get them in the right format for later logic. Below is the definition of columns that have been used in later algorthim.

#From PLA dataframe:

SRROGD_um: Die size in X direction

SRRPGD_um: Die size in Y direction

PLADot: Dot Technology

ProcessTag: Fabrication Technology

SRRDieArea_mm2: Die Area in mm2

PLAFabDieArea: Combination of Fabrication Technology and Die Area in mm2

OGDWidthOfPGDScribe_um: Die Space in X direction (return value)

PGDWidthOfOGDScribe_um: Die Space in Y direction (return value)


#From Items dataframe:

Die X (um): Die size in X direction

Die Y(um): Die size in Y direction

DotProcess: Dot Technology

FabProcess: Fabrication Technology

DotDieArea: Combination of Dot Technology and Die Area in mm2

FabDieArea: Combination of Fabrication Technology and Die Area in mm2


## Visual Network Design

## Algorithm Implementation
