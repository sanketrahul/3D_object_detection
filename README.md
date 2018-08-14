# 3D_object_detection

This repository is to integrate 3D object detection via correspondance grouping PCL code (http://www.pointclouds.org/documentation/tutorials/correspondence_grouping.php#correspondence-grouping) to ROS. 

We have breakdown this work in 3 parts:

1. Replacing input scene of corespondence grouping with kinect output point cloud in order to perform real-time 3D object detection. Also, we can build more models of 3D object from https://www.sketchup.com or some other online available 3D object model in pcd format.

2. The core algorithm integration with ROS.

3. The output highlighting the detected object on the input point cloud. Current PCL code work on offline with .pcd files and PCL viewer. Through this repository we are trying to detect 3D objects in real-time.

Similar work to step 1 and 3 has been done in euclidean clustering integration code of PCL to ROS (https://github.com/jsk-ros-pkg/jsk_recognition/blob/master/jsk_pcl_ros/src/euclidean_cluster_extraction_nodelet.cpp). So, we focused first on the step 2 in this GSoC work.

Later, we will integrate step 1 and 3. Also, we will create the 3D object detection as a nodelet to be integrated with jsk_pcl_ros.

Dependencies:

PCL 1.8.1 (Must and should have any trace of PCL 1.7 in you workstation)

ROS Kinetic 

Ubuntu

Running of Code:

First, git clone this code in you ros workstation.

Then run catkin build to run the code.

Also, download sample model(milk.pcd) and scene(milk_cartoon_all_small_clorox.pcd) pcd files from http://www.pointclouds.org/documentation/tutorials/correspondence_grouping.php#correspondence-grouping. Save these file at ros workstation. 

Further, run command: roslaunch openni_launch openni.launch

Then on new terminal run command: rosrun 3D_object_detection 3D_object_detection input:=/camera/depth/points

It should output of the model and scene correspondence text output as:
![3D_object_detection_output](https://github.com/sanketrahul/3D_object_detection/blob/master/image/3D_object_detection_success.png)

Note: The code also contains PCL 1.7.2 code also. It is still under progress.

Credits: This work has been carried out for Google Summer of Code 2018 under mentorship of Prof. Kei Okada (@k-okada)
