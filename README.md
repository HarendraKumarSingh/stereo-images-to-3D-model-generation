# stereo-images-to-3D-model-generation
2D stereo image to 3D model generation

### Methodology:

1. Take multi-view stereo image of an object from multiple angles.
<img src="https://user-images.githubusercontent.com/12294956/46274658-d0395b00-c577-11e8-99a7-0880e346d6c7.png">

2. Increasing the resolution of these stereo images (using OpenCV set() method with defined CAP_PROP_FRAME_WIDTH and CAP_PROP_FRAME_HEIGHT values).
3. Calibrating all the cameras individually
4. Calculating a depth map - load the claiberations and undistort the images (Computes the ideal point coordinates from the observed point coordinates).
<img src="https://user-images.githubusercontent.com/12294956/46274657-d0395b00-c577-11e8-976f-b6e8e88d6d64.png">

5. From depth map, generate point cloud
<img src="https://user-images.githubusercontent.com/12294956/46274656-cfa0c480-c577-11e8-90d6-d453f0930e2c.png">
6. From point cloud generate 3D model
7. Optimise and clean the generated 3D model manually with 3D model editing tools.


### Terminology used:

#### Stereo images-
When we take an image using pin-hole camera, we lose an important information, ie depth of the image. Or how far is each point in the image from the camera because it is a 3D-to-2D conversion. So it is an important question whether we can find the depth information using these cameras. And the answer is to use more than one camera. Our eyes works in similar way where we use two cameras (two eyes) which is called stereo vision.
#### Photogrammetry-
Photogrammetry is the science of making measurements from photographs. The input to photogrammetry is photographs, and the output is typically a map, a drawing, a measurement, or a 3D model of some real-world object or scene.
#### Reality capture-
RealityCapture is a software solution which can be used to edit 3D models generated from point cloud.
#### Point cloud-
A point cloud is a set of data points in space. Point clouds are generally  large number of points on the external surfaces of objects around them.

### Implementations
Independently implementation examples are provided for your reference.



