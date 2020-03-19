# DigitalTwinsPublic
While doing research in the Structures and Composites Lab at Stanford University, we created a UAV-Based Hardware/Software platform in Python that accomplished the following:

- Scans a concrete specimen while the UAV is in-flight, thereby generating a 3D point cloud and a series of 2-D images of the specimen from varying perspectives.
- Wirelessly transmits the point cloud, images and 3D position data from the aircraft to the ground station for post-scan processing
- Uses a Convolutional Neural Network to detect the cracks in the 2-D images
- Uses the intrinsic camera matrix and 3D position/euler angles to map each pixel in the image to a voxel in the point cloud.
  - This creates what is called a "Digital Twin" of the concrete structure, hence the name of the project.

Unfortunately, I am not allowed to upload our codebase to my github due to the Non-Disclosure Agreement to which I am bound. However, you can read our paper that we submitted to the 12th Edition International Workshop on Structural Health monitoring here:
https://michaelmarshjr.files.wordpress.com/2020/01/561.pdf

Some notes about the paper:

- At the time the manuscripts for the paper were due, the program was still under development and was only about 20% accuracy (pixels highlighted that were actually cracks vs. total highlighted). By the time we presented our demo at the International Workshop, we increased the mean accuracy to about 70%.
- We intended to add a feature that would then use the modified point cloud data to generate a finite element model of the structure. This failed as we could not standardize the orientation of the Y and Z axes in Open3D. As a result, a predetermined model was used during the demo at the conference. 
