# Milestone
4-16-2024
## What We Have Accomplished
Search Phase
- We have a fully implemented Nearest Neighbors algorithm for the search phase of our texture syntehsis. This allows us to find the exemplar patch that best aligns with our solid voxel slice. This process is sped up by applying a PCA projection to the neighborhood vectors in the exemplar and by searching a sparser grid than every voxel. An image of this proccess on a 2D voxel slice is shown below.

Optimize Phase
- We are currently in the process of debugging our Optimization Phase implementation. 

## Preliminary Results
Results of the Nearest Neighbors Search on a 2D patch of solid pixels.
![Search Phase](/assets/search_phase.jpg)

## Progress Relative to Our Plan

According to our original plan, we are actually right on schedule. By this week, we were wanting to be in progress with our optimization phase, and hopefully finishing it up by the end of this week (4/14 - 4/20). We ideally wanted to have our optimization phase fully implemented by the milestone, however we have run into a few issues while implementing such as getting used to writing in Pytorch and verifying that the math were are performing is accurate. With a few more days of debugging, we should be set to begin writing up the histogram matching code and testing on 3D solids.

## Updated Work Plan
Week 3: 4/14 - 4/20
- Finish solid optimization, specifically debugging our optimization phase
- Start histogram matching

Week 4: 4/21 - 4/27
- Finish histogram matching
- Investigate into further optimization techniques for speed up
- Begin on final deliverables

Week 5: 4/28 - 4/30
- Finish up final deliverables
- Add any finishing touches

## Additional Links

[Milestone Slides](https://docs.google.com/presentation/d/1-W9nknMRB0o4Y1pjfMG802zc2aoa4MWge1_fWNJRdns/edit#slide=id.p)

[Milestone Video] (https://www.youtube.com/watch?v=HBS5tmbgtsw)
