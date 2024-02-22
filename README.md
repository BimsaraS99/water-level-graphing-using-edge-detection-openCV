#Water Level Monitoring Computer Vision Task

This repository contains a Python script that processes a video of a liquid level sensor and calculates the water level over time. The script uses OpenCV for image processing and matplotlib for plotting.

The script first loads the video and extracts information such as the number of frames, duration, and resolution. It then defines two functions: `process_frame` and `find_mean_point`.

The `process_frame` function takes a single frame of the video as input and returns a mask of the liquid, a dilated mask, and the edges of the liquid.

The `find_mean_point` function takes a binary image as input and returns the average y-coordinate of the white pixels. This corresponds to the water level.

The script then iterates over each frame of the video, processing it with the `process_frame` and `find_mean_point` functions. The water level is stored in a list.

Finally, the script maps the water level to a percentage of the container's height and plots the water level over time.
