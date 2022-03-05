# Object_and_Grasp_Detection
**Working**<br/>
1. Import the libraries.
2. Set the frame width and height.
3. Read the image.
4. Convert the image to grayscale to apply Canny edge detection.
5. Introduce the trackbars for two thresholds. Arguments are:
    1. Name
    2. Window name
    3. Default value
    4. Maximum value
    5. 'empty' is the function that will be called whenever there will be a change in the value. As nothing is to be done, just pass it.
6. Apply Canny edge detection.
7. Apply Dilation function to remove the overlaps. To introduce the dilation function, define the kernel by a numpy array of ones.
8. Define the Contour function 'getCounters' with arguments as input image and output image.
9. Apply 'findContour' function. Arguments are:
    1. Image
    2. Retrieval method: These are of many types, but two of them are essential. The external retrieval method is used to retrieve only the extreme outer contours. The other is the tree method, which retrieves all contours and reconstructs a full hierarchy.
    3. Approximation: Get all stored contour points. But, if 'CHAIN_APPROX_SIMPLE' is used, it will compress the values, resulting in less number of points.
10. Apply a for loop, which loops through all the contours.
11. To remove the contours that are not of interest, find the area for each contour. The contours are drawn if the area is greater than the minimum specified area.
12. To define the shape of the contour, use 'approxPolyDP' to approximate the shape of polygonal curves to specified precision. It returns an array of points.
13. Draw the bounding box.
14. Introduce the trackbar to filter different areas.
