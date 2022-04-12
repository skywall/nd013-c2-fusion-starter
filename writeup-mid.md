# Writeup: Midterm project

## Point cloud images & features analysis
<p align="center"><img src="img/point_cloud/point_cloud_drive.gif" /></p>


All the point cloud images are taken from `training_segment-1005081002024129653_5313_150_5333_150_with_camera_labels.tfrecord`.
Possible features (recognizable car parts and characteristics) are mentioned within title of each image.

### Images

#### 01 - Wheels, front bumper, front window (windshield), side windows
![](img/point_cloud/point_cloud_01.png)
#### 02 - Wheels (especially good in side view), front bumper, front window (windshield), side windows, hood
![](img/point_cloud/point_cloud_02.png)
#### 03 - Wheels, rear bumper, side windows, boot (trunk)
![](img/point_cloud/point_cloud_03.png)
#### 04 - Wheels, rear bumper, side windows, tail lights, outside mirrors, rear window
![](img/point_cloud/point_cloud_04.png)
#### 05 - Outside mirrors, wheels, trunk (pickup truck on the right)
![](img/point_cloud/point_cloud_05.png)
#### 06 - Wheels, side silhouette 
![](img/point_cloud/point_cloud_06.png)
#### 07 - Wheels, rear bumper, windows, 
![](img/point_cloud/point_cloud_07.png)
#### 08 - Outside mirrors, wheels, front bumper 
![](img/point_cloud/point_cloud_08.png)
#### 09 - Wheels, hood, windows (car in the back), front fender
![](img/point_cloud/point_cloud_09.png)
#### 10 - Wheels, rear window, boot (trunk), rear fender, front fender
I would like to mention, there is car in image where only front wheel visible so tracking system should definitely deal also with scenarios like this. 
![](img/point_cloud/point_cloud_10.png)
#### 11 - Wheels
![](img/point_cloud/point_cloud_11.png)
#### 12 - Hood, wheels of the trailer
![](img/point_cloud/point_cloud_12.png)
#### 13 - High truck in the middle of the image - clearly visible wheels and large tailgate
![](img/point_cloud/point_cloud_13.png)
#### 14 - Rear bumper, wheels, boot (trunk)
![](img/point_cloud/point_cloud_14.png)
#### 15 - Rear window, side windows, outside mirrors
![](img/point_cloud/point_cloud_15.png)

## Range image
- `top` - distance to the point
- `bottom` - intensity of the reflection

![](img/range_image.png)

## BEV (bird's eye view) of the aggregated points from the point cloud
Image description:
- `red` - density of the points
- `blue` - maximum intensity within pack of points
- `green` - maximum height within pack of points
- `RGB` - RGB combination of all the above

![](img/bev_map.png)

## Metrics

Specification of used data:
- `data_filename = 'training_segment-1005081002024129653_5313_150_5333_150_with_camera_labels.tfrecord`
- `show_only_frames = [50, 150]`

### Computed metrics
- `precision = 0.9376237623762375`
- `recall = 0.9496699669966996`

![](img/metrics.png)