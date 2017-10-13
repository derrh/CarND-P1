## Finding Lane Lines on the Road

_Goals_

- Make a pipeline that finds lane lines and annotates video footage of a vehicle driving.
- Gain a better understanding of how Computer Vision is used to provide guidance data to a self-driving car.

My pipeline consisted of the following steps:

- Convert the image to grayscale
- Blur the image to improve the performance of the edge detection
- Employ a Canny Edge Detection algorithm to detect visible edges
- Mask the input image to the region where lane lines are expected to be found
- Use a Hough Line Transform function to detect straight lines in the input image
- From the set of detected lines, compute 2 lane marker lines which could be used to guide a self-driving car

My solution will fail in less-than ideal lighting/contrast situations. It is also restricted to a very specific masked area. Lane lines on steep roads, or roads with sharp curves may not be ideally detected.

One obvious improvement that could be made would be to use color selection or possibly converting the input image to other color spaces to improve the performance of the edge detection. In addition, dynamically masking the content, or employing some other solution to remove noise from the input image would make the detection algorithm more robust.

