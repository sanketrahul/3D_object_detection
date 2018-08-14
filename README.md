# 3D_object_detection

This repository is to integrate 3D object detection via correspondance grouping PCL code (http://www.pointclouds.org/documentation/tutorials/correspondence_grouping.php#correspondence-grouping) to ROS. 

We have breakdown this work in 3 parts:

1. Replacing input scene of corespondence grouping with kinect output point cloud in order to perform real-time 3D object detection. Also, we can build more models of 3D object from https://www.sketchup.com or some other online available 3D object model in pcd format.

2. The core algorithm integration with ROS.

3. The output highlighting the detected object on the input point cloud. Current PCL code work on offline with .pcd files and PCL viewer. Through this repository we are trying to detect 3D objects in real-time.

Similar work to step 1 and 3 has been done in euclidean clustering integration code of PCL to ROS (https://github.com/jsk-ros-pkg/jsk_recognition/blob/master/jsk_pcl_ros/src/euclidean_cluster_extraction_nodelet.cpp). So, we focused first on the step 2 in this GSoC work.

Later, we will integrate step 1 and 3. Also, we will create the 3D object detection as a nodelet to be integrated with jsk_pcl_ros.

Credits: This work has been carried out for Google Summer of Code 2018 under mentorship of Prof. Kei Okada (@k-okada)
