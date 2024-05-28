# Lidar Obstacle Detection
The main goal of this project is to filter, segment, and cluster real point cloud data to detect obstacles in a driving environment.
## Steps of the project
1. Reading data(pcd files)
2. Filtering
3. Segmentation
4. Clustering
5. Bounding box
6. Rendering
## Filtering
In pcd files, there are approximately 250,000 point clouds. If you use all of them for the next steps, you'd be waiting for a while to get it done. To increase the speed we need to remove some targets.
* Downsampling: Points are converted to voxels. PCL function voxelGrid is used for this step.
* Crop: Remove the points outside the limitation. PCL fucntion CropBox is used for this step.
## Segmentation
Segmentation divides the targets plane and objects, that the car is able to decide which direction it is supposed to go. RANSAC Algorithm is used for this step.
## Clustering
In Clustering step, Euclidean Clustering mechanism is used. Now each object appears with different color. 
## Bounding box
For each cluster bouding box is fitted. If you have been through all the steps properly, the result appears on the screen like below.
<img src="bandicam 2024-05-28 21-30-08-196.gif" alt="simulation" style="width:600px;"/> 
