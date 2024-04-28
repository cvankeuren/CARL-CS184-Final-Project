# C.A.R.L. 3D Texture Synthesis from 2D Exemplars Final Report
By: C.A.R.L. (Catherine Van Keuren, Anthony Salinas Suarez, Rohan Mathur, Longchao (Joy) Liu)

## Abstract
For this project, our overall goal was to implement a way to use 2D texture exemplars to synthesize 3D solid textures. We not only wanted to be able to map textures to the surface of solids, but we also took on the challenge to map the texture to the inside of the solid. The challenge with 3D texture mapping is that rather than just the surface texture aligning, we also need to make sure that each slice with in the solid's texture aligns as well. We modeled our implementation off that of Johannes Kopf, et al. utilizing the methods described in their paper titled "Solid texture synthesis from 2D exemplars." The process used in their paper entails iterating over every cross section slice of texels within the solid, and performing texture mapping to those slices. This process was implemented using two main phases: the Search Phase and the Optimization Phase. The Search Phase involves finding the patch of texture that best matches the solid slice, and the Optimization Phase involves iterively modifying specific texels within the solid slices until it more closely matches the exemplar patch.

## Technical approach
Overall, the 

### Search Phase
Nearest Neighbors

Pyramid Search

### Optimization Phase

Optimization

Histogram Matching

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


