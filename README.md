# Euclidean-Distance-in-Forecasting-the-Nearest---Semiconductor-Manufacturing
Known as the most common used metric in computer science, physics and maths for determining the distance between two points, the Euclidean Distance has various applications in machine learning, computer vision, physics and geometry. Some popular use-cases include clustering algorithms such as K-means and NNC, measuring similarity among features, or finding the shortest paths.

Formula for Euclidean Distance:

Given two points  p = (p_1, p_2, \dots, p_n)  and  q = (q_1, q_2, \dots, q_n)  in  n -dimensional space, the Euclidean distance  d(p, q)  is calculated as:


d(p, q) = \sqrt{(q_1 - p_1)^2 + (q_2 - p_2)^2 + \dots + (q_n - p_n)^2}


Example in 2D Space:

If  p = (x_1, y_1)  and  q = (x_2, y_2) , the distance is:

d(p, q) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}


Example in 3D Space:

If  p = (x_1, y_1, z_1)  and  q = (x_2, y_2, z_2) , the distance is:

d(p, q) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}


![istockphoto-1167267132-612x612](https://github.com/user-attachments/assets/dcf62277-0fcf-44c7-9e57-86adf6416ca5)


Semiconductor manufacturing use 300mm diameter wafer, and chips (dies) are arranged on each wafer by grid pattern. Therefore, optimizing the space on a wafer can increase the number of dies and reducing waste. However, the shrinking of nodes lead to the very complicated die packages and fabrication processes. Which in turn increase the dies coordinates to million posibilities. Whenever a new demand signal arrives, new dies are added without the sizes. We only know the high level of what customer wants. Thus, finding correct die layouts is not only significant for downstream planning but also turns into time consuming and excel crashing without the help of tool such as Python.

Just two years ago, engineers still look into individual package to find the correct die sizes for any new chip - one by one. This process can take upto 7 days depending on how many new products are added. With this implementation of Euclidean Distance written any run on Python, the entire process drops to 2 hours from preparing the data to send out the report. The script itself only takes 2 minutes to run.

## Data Description
As mentioned above, the data is provdied as csv format individually for 33 packages technology. Combining of these files is the PLA data frame of 2,344,400 rows and 29 columns. 

	AnalysisDate	ProcessTag	SRROGD_um	SRRPGD_um	SRRDeviceX_um	SRRDeviceY_um	SRRDieArea_mm2	AspectRatio	LFU	DPFOGD	...	FractureWindowOGD_um	FractureWindowPGD_um	GrossDPW	EdgeExclusionPrimary_mm	EdgeExclusionFull_mm	FrameBuildConfidenceLevel	PLADot	PLAFab	PLADotDieArea	PLAFabDieArea
0	24-May-24	P1222.4-1	2000.16	2000.88	2000.16	2000.88	4	0.999640	0.900433	15	...	31073.86	24862.42	15633	3	3	medium	1222.4-1	1222	1222.4-1_4	1222_4
1	24-May-24	P1222.4-1	2100.60	2000.88	2100.60	2000.88	4	1.049838	0.944090	15	...	32580.46	24862.42	14902	3	3	medium	1222.4-1	1222	1222.4-1_4	1222_4
2	24-May-24	P1222.4-1	2201.04	2000.88	2201.04	2000.88	4	1.100036	0.922027	14	...	31819.06	24862.42	14240	3	3	medium	1222.4-1	1222	1222.4-1_4	1222_4
3	24-May-24	P1222.4-1	2300.40	2000.88	2300.40	2000.88	4	1.149694	0.893736	13	...	30842.74	24862.42	13638	3	3	medium	1222.4-1	1222	1222.4-1_4	1222_4
4	24-May-24	P1222.4-1	2400.84	2000.88	2400.84	2000.88	4	1.199892	0.931572	13	...	32148.46	24862.42	13075	3	3	medium	1222.4-1	1222	1222.4-1_4	1222_4
...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...	...
68361	13-Nov-23	P1280	25200.00	31200.48	25200.00	31200.48	786	0.807680	0.985427	1	...	25994.98	32525.38	66	5	5	NaN	1280	1280	1280_786	1280_786
68362	13-Nov-23	P1280	25200.00	31301.28	25200.00	31301.28	788	0.805079	0.988481	1	...	25994.98	32626.18	66	5	5	NaN	1280	1280	1280_788	1280_788
68363	13-Nov-23	P1280	25200.00	31400.64	25200.00	31400.64	791	0.802531	0.991492	1	...	25994.98	32725.54	65	5	5	NaN	1280	1280	1280_791	1280_791
68364	13-Nov-23	P1280	25200.00	31500.00	25200.00	31500.00	793	0.800000	0.994502	1	...	25994.98	32824.90	64	5	5	NaN	1280	1280	1280_793	1280_793
68365	13-Nov-23	P1280	25200.00	31600.80	25200.00	31600.80	796	0.797448	0.997556	1	...	25994.98	32925.70	64	5	5	NaN	1280	1280	1280_796	1280_796


Applying the Euclidean Distance formula, I 

## Visual Network Design

## Algorithm Implementation
