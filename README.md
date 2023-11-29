# vid2frames3d

# Goals

* Try to actually finish this one.
* Take video files and produce frames sutable for photogrametry/gausian splat that are optomised for best 3d coverage.

# Methods

Use tools such as optical flow (and maybe quality tools such as sharpness) to pick the best frame set for 3D reconstruction. Slower movement requires fewer frames faster movement requires frames more regularly. We want to reject blured frames.

OpenCV under python seams a good place to start.

# Issues

* The more frames in a reconstruction, the longer proccessing takes.
* Too few frames will reduce the quality of the reconstruction.
* "decimation" does not take into account how sutable the frames are for 3d reconstruction. 
* Panning and movement during video creation is not constant. Particularly if useing legacy video not originally captured with 3D reconstruction in mind.
