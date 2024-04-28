# C.A.R.L. 3D Texture Synthesis from 2D Exemplars Final Report
By: C.A.R.L. (Catherine Van Keuren, Anthony Salinas Suarez, Rohan Mathur, Longchao (Joy) Liu)

## Abstract
For this project, our overall goal was to implement a way to use 2D texture exemplars to synthesize 3D solid textures. We not only wanted to be able to map textures to the surface of solids, but we also took on the challenge to map the texture to the inside of the solid. The challenge with 3D texture mapping is that rather than just the surface texture aligning, we also need to make sure that each slice within the solid's texture aligns as well. We modeled our implementation off that of Johannes Kopf, et al. utilizing the methods described in their paper titled "Solid texture synthesis from 2D exemplars." The process used in their paper entails iterating over every cross section slice of voxels within the solid, and performing texture mapping to those slices. This process was implemented using two main phases: the Search Phase and the Optimization Phase. The Search Phase involves finding the patch of texture that best matches the solid slice, and the Optimization Phase involves iterively modifying specific voxels within the solid slices until it more closely matches the exemplar patch. We decided to implement this project using PyTorch to take advatage of its batching capabilities and hopefully yield a much faster rendering.

## Technical approach
As mentioned in the abstract, the 3d texture synthesis was done in two main stages: the Search Phase and the Optimization Phase. Both of these phases participated in determining the ideal mapping of the texture onto each voxel in the solid. Before starting the iterations of these phases, we had to do a bit of preprocessing. First, we needed to take our object file and voxelize it. This was done using a Python library Trimesh and it's built in function:

 `trimesh.voxel.creation.voxelize(mesh, pitch=pitch).fill()`.

After that, we assign each voxel within our solid a random color value from the exemplar, and then begin iterating through the two phases. 

### Search Phase
The first phase 

**Nearest Neighbors**

**Pyramid Search**

### Optimization Phase
After we have found the exemplar patch that best matches the patch in our synthesized solid, we move onto the optimize phase, where we modify voxels one by one until our energy function that measures the differences between the two converges to a desired point. This is done by using iteratively re-weighted least squares to minimize the energy function, and then improved upon by adding in Histogram Matching. 

**Optimization**

As mentioned 

**Histogram Matching**

Adding Histogram Matching allows us take global statistics into account to make sure that we are not converging to the wrong local exemplar patch in the previous step. In order to implement Histogram Matching, we add a step during the Optimization Phase that updates our previously calculated weight. This is done by first creating three 16 bin histograms (one for each R, G, and B channel) based on the original texture image using `torch.histc(...)`. For each solid patch, we also create the same histogram. Then, we update the weight using the given formula:

$
\omega'_{u,i,v} = \frac{\omega_{u,i,v}}{ \left(1 + \sum_{j=1}^{k} \max \left[0, H_{s,j}(b_{j}(e_{u,i,v})) - H_{e,j}(b_{j}(e_{u,i,v}))\right] \right)}
$

Here, Hs,j and He,j denote the j-th histogram of the solid and the exemplar, respectively, let H(b) denotes the value of bin b in a histogram H. Next, for a color c, let bj(c) specify the bin containing c in the histograms Hs,j and He,j. This allows us to adjust our weights with respect to the global and local color distribtuions.


### Visualization


A 1-2 page summary of your technical approach, techniques used, algorithms implemented, etc. (use references to papers or other resources for further detail).
Highlight how your approach varied from the references used (did you implement a subset, or did you change or enhance anything), the unique decisions you made and why.

### Problems We Encountered

### Lessons Learned

## Results
Your final images, animations, video of your system (whichever is relevant). You can include results that you think show off what you built but that you did not have time to go over on presentation day.

## References
Kopf, J., Fu, C.-W., Cohen-Or, D., Deussen, O., Lischinski, D., & Wong, T.-T. (2007). Solid texture synthesis from 2D exemplars. ACM Transactions on Graphics, 26(3), 2. https://doi.org/10.1145/1276377.1276380

## Contributions
Joy

Rohan

Anthony

Catherine


