---
title: Algorithms
weight: 1
---
# Algorithms

The implementations of the algorithms can be found at the following repository: https://github.com/tue-aga/TreemapComparison .

This repository contains the source code and data used for the paper: "Quantitative Comparison of Time-Dependent Treemaps". It heavily borrows from the source code from the paper "Stable Treemaps via Local Moves".

Algorithms implemented:

| Algorithms                         | Reference                                                                                                                                                                                                             |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Local Moves                        | M. Sondag, B. Speckmann, and K. Verbeek. Stable treemaps via local moves. IEEE Transactions on Visualization and Computer Graphics, 24(1):729–738, 2018.                                                              |
| Slice and Dice                     | B. Shneiderman. Tree visualization with tree-maps: a 2D space-filling approach. ACM Transactions on Graphics, 11(1):92–99, 1992                                                                                       |
| Squarified                         | Perceptual guidelines for creating rectangular treemaps. IEEE Transactions on Visualization and Computer Graphics, 16(6):990–998, 2010.                                                                               |
| Approximation                      | An approximation algorithm for dissecting a rectangle into rectangles with specified areas. Discrete Applied Mathematics, 155(4):523–537, 2007                                                                        |
| Strip                              | B. B. Bederson, B. Shneiderman, and M. Wattenberg. Ordered and quantum treemaps: Making effective use of 2D space to display hierarchies. ACM Trans. Graph., 21(4):833–854, 2002.                                     |
| Pivot-by-(Middle,Split,Split-Size) | B. Shneiderman and M. Wattenberg. Ordered treemap layouts. In Proc. IEEE Symp. on Information Visualization (InfoVis), pp. 73–78, 2001.                                                                               |
| Split                              | B. Engdahl. Ordered and unordered treemap algorithms and their applications on handheld devices, 2005. MSc thesis, Tech. Report TRITA-NA-E05033, Dept. of Comp. Sci., Stockholm Royal Institute of Technology,Sweden. |
| Spiral                             | Y. Tu and H.-W. Shen. Visualizing changes of hierarchical data using treemaps. IEEE TVCG, 13(6):1286–1293, 2007.                                                                                                      |
| Hilbert                            | S. Tak and A. Cockburn. Enhanced spatial stability with Hilbert and Moore treemaps. IEEE Transactions on Visualization and Computer Graphics,19(1):141–148, 2013.                                                     |
| Moore                              | S. Tak and A. Cockburn. Enhanced spatial stability with Hilbert and Moore treemaps. IEEE Transactions on Visualization and Computer Graphics,19(1):141–148, 2013.                                                     |
| Git                                | Vernier E., Comba J., Telea A. A stable greedy insertion treemap algorithm for software evolution visualization. IEEE Conference on Graphics, Patterns and Images: 158-165, 2018                                      |

Very brief explanation of Main classes.

`Visualiser`: Use to gain a visual interface showing a treemap for the datasets for all algorithms.
Can specify additional treemaps in gui.java

`DataSetClassifier`: Use to classify additional datasets.

`StatisticalParser`: Use to generate the matrix table for all processed datasets.

`BaseLineGenerator`: Use to manually generate baselines for the specified folders.

`Simulator`: Use to generated treemaps for a folder of datasets.

`IpeImporter`: Use to visualise a .rect file as outputed from Simulator.


Pipeline for experiments:
1. Use `Simulator` to generate treemaps with -baseline enabled for baselines.
2. Use `DataSetClassifier` to classify the datasets.
3. Use `StatisticalParse` to generate the matrix plots and statistics.

<!--
The implemented techniques are:

- [Slice and Dice](https://dl.acm.org/citation.cfm?id=115768)
- [Squarified Treemap](https://link.springer.com/chapter/10.1007/978-3-7091-6783-0_4)
- [Ordered Treemap Pivot-by-Middle](https://dl.acm.org/citation.cfm?id=857710)
- [Ordered Treemap Pivot-by-Size](https://dl.acm.org/citation.cfm?id=857710)
- [Strip Treemap](https://dl.acm.org/citation.cfm?id=857710)
- [Nmap Alternate Cut](http://ieeexplore.ieee.org/document/6876012/)
- [Nmap Equal Weights](http://ieeexplore.ieee.org/document/6876012/)
- [Spiral Treemap](http://ieeexplore.ieee.org/document/4376152/)
- [Moore Treemap](http://ieeexplore.ieee.org/document/6185545/?reload=true)
- [Hilbert Treemap](http://ieeexplore.ieee.org/document/6185545/?reload=true)
- [No moves](https://www.scopus.com/record/display.uri?eid=2-s2.0-85028715864&origin=inward&txGid=79d555d432fb4591ed03215553ac3a72)
- [Local Moves Treemap](https://www.scopus.com/record/display.uri?eid=2-s2.0-85028715864&origin=inward&txGid=79d555d432fb4591ed03215553ac3a72)
- [Approximation Treemap]()
- [Insertion Treemap](https://github.com/EduardoVernier/insertion-treemap)


# TreemapStability
This project contains the implementation of 14 treemap techniques. Our study focuses on the behavior of these methods in the context of dynamic hierarchies.

### Compiling
To compile the Java code, simply run  `./compile`  from the repository's root.

### Running
This application outputs the rectangles generated by the treemapping techniques. Initially, it does not allow for visual inspection, for that see section [Visualizing](#visualizing).

The generation takes four arguments:
- `input_dir` - path where the dataset is located
- `width` - width of the base rectangle
- `height` - height of the base rectangle
- `output_dir` - path where the outputted rectangles will be saved.

`./treemaps.sh input_dir width height output_dir`

Example: `./treemaps.sh dataset/exo 1000 1000 output`

To do batch testing for all datasets in `./dataset/`, run

`for dataset in $(find dataset/* -maxdepth 0 -type d); do ./treemaps.sh $dataset 1000 1000 output; done`   -->
