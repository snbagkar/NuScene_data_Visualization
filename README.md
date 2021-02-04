# NuScene_data_Visualization
This project enables to visualize NuScene data such as Point Cloud data for Radar, Lidar and Images captures using various sensors
# Requirements and Dependencies

  - Download NuScene mini dataset https://www.nuscenes.org/data/v1.0-mini.tgz
  - Download Lidarseg file https://www.nuscenes.org/data/nuScenes-lidarseg-mini-v1.0.tar.bz2
  - Download NuScene Develop kit https://github.com/nutonomy/nuscenes-devkit
  - Ubuntu 18.04
  - Jupyter notebook
  - pip3
  - python3
  - opencv
 
# Setup Nuscenes develop kit locally  
You may need to install jupyter notebook for Visualization locally
Install Juypter Notebook 
```sh
$ pip3 install notebook
```
Install NuScene-devkit 
```sh
$ pip3 install nuscene-devkit
```
Launch Jupyternotebook
```sh
$ python -m notebook
```

# Visualize dataset using NuScenes dev-kit
run the file Visualize_data_using_NuScenes sile and give the correct path of sample folder which you want to visualize <br />
Input the correct token of the data for visualization
![Visualizing a random image from CAM_FRONT](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/visualize_image.jpg)

![Visualizing a random image from CAM_FRONT](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/visualize_image2.jpg)

# Visualize Lidar PCD from the dataset using python OpenCV
The Lidar PCD is a nx4 matric that stores x y z intensity

![Visualizing Lidar PCD]()

You can colorize the points based on the following 3 Parameters
- Height of the points
- Intesity of the points
- Semantic label of the points

We will visualize each one of them below
- Heights of the points
To get this plot run the file lidarpcd_height
![Visualizing Lidar PCD_colorize_height](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/lidarpcd_height.jpg)
- Intensity of the points
To get this plot run the file lidarpcd_intensity
![Visualizing Lidar PCD_colorize_intensity](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/lidarpcd_intensity.jpg)
- Semantic label of the points
To get this plot run the file lidarpcd_semantic
![Visualizing Lidar PCD_colorize_semantic](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/lidarpcd_semantic.jpg)

# Visualize Radar PCD from the dataset
The Radar PCD is a nx18 matric that stores x y z dyn_prop id rcs vx vy vx_comp vy_comp is_quality_valid ambig_state x_rms y_rms invalid_state pdh0 vx_rms vy_rms <br />
To know more visit https://github.com/nutonomy/nuscenes-devkit/blob/5325d1b400950f777cd701bdd5e30a9d57d2eaa8/python-sdk/nuscenes/utils/data_classes.py#L259:1

You can colorize the points based on various parameter. We will explore the following
- height of the points
- velocity of the points
We will visualize each one of them below
- Heights of the points
![Visualizing_Radar_pcd_height](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/radarpcd_height.jpg)

- Velocity of the points
for this we will first calculate the resultant velocity of the point

![Visualizing](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/radarpcd_velocity.jpg)

# Ploting Lidar PCD and Radar PCD on an image
For this we will use the NuScene Devkit. <br /> Run the file Plot_PCD_to_Image.

-Ploting Lidar PCD to an image
![Visualizing](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/lidar_image.jpg)

-Ploting Radar PCD to an image
![Visualizing](https://github.com/ankitcivic/Visualize_NuScene_dataset/blob/main/images/lidar_image.jpg)
