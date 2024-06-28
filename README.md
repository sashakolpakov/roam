# Robust Affine Matching via Grassmannians (RoAM)

Michael Werman (HUJI, Israel), Alexander Kolpakov (University of Austin, USA)

A new algorithm, RoAM (Robust Affine Matching via Grassmannians) to solve the problem of affine registration is proposed. The algorithm is based on the Grassmannian of $k$-dimensional planes in $\mathbb{R}^n$ and minimizing the Frobenius norm between the two elements of the Grassmannian. The results of the experiments show that the algorithm is more robust to noise and point discrepancy in point clouds than  previous approaches. Our main comparison is with GrassGraph that appears to be state-of-the-art [IEEE Trans. Image Proc., vol. 29, pp. 3374-3387, 2020, doi: 10.1109/TIP.2019.2959722]. 

Files included:

1) roam_tests.ipynb : RoAM algorithm realized in Python / SageMath, numerical experiments and statistcs for tests with different levels of noise and point discrepancy

2) (filename).csv : point cloud filename = (Teapot | Bunny | Cow)

3) roam_stats_(batch%size)_(filename).csv : test stats for RoAM saved in csv format (see the manuscript for description) for point cloud "filename" with batch size of "batch%size" per test

4) GrassGraph_comparison.ipynb : GrassGraph algorithm realized in Python / SageMath, numerical experiments and statistcs for tests with different levels of noise and point discrepancy

5) GrassGraph_stats_(filename).csv : test stats for the "standard" GrassGraph with 3 Laplacian eigenvectors for point cloud "filename"

6) GrassGraph_stats_mod_(filename).csv : test stats for the "modified" GrassGraph with 10 Laplacian eigenvectors for point cloud "filename"

7) roam_stats_plot_colormap.ipynb : plotting the test stats as colormaps (see the manuscript for description)

8) roam_partial_scan.ipynb : registering two scans of the same object 

9) roam_best_vs_weighted : comparison of two approaches to feature matching (best matching among a number of probabilistic trials vs a weighted sum projected to the nearest permutation)

10) Enfant_au_Chien-Broken.obj, Enfant_au_Chien.obj : meshes of the same statue, broken and restored 

11) roam_manuscript.pdf : manuscript describing the algorithm 

Using:

Caerbannog point clouds from https://data.nrel.gov/submissions/153 (unoccluded teapot, bunny, cow); Three D Scans from https://threedscans.com/ ("Enfant au Chien" statue before and after restoration).


Required:

SageMath (https://www.sagemath.org) installed to run the worksheets; Open3D (http://www.open3d.org), available via pip.
