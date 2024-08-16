# stereo_vision
The code uploaded consists of a pipeline for creating a stereo vision system to end up a depth map. Following steps are followed to create the required depth maps
1. The pair of images is loaded for processing. Initially some code is used to find the matches between the two images using the FLANN based matcher and the result is later used to find the fundamental matrix.
2. The fundamental matrix is then used to compute the essential matrix which is later used to compute the rotation and translation matrices.
3. This data is then used to rectify images through the function cv2.warpPerspective.
4. The rectified images are used to compute the disparity maps and then they are later used to compute the depth maps.
Consider the following images that are example images used to compute depth images.

<img width="596" alt="dataset_images_paired" src="https://github.com/user-attachments/assets/a58808ce-ae78-4a7b-a3b5-81492ea23611">

Following is the disparity map computed through the above images.


<img width="400" alt="disparity_map" src="https://github.com/user-attachments/assets/afa04c64-2169-442f-b504-2a00ef4f1e5a">


Following is the depth map computed.



<img width="400" alt="depth_map" src="https://github.com/user-attachments/assets/386e6fd6-e093-4a14-87d0-85778daf5043">
