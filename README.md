<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Object Detection and Size Measurement</h1>
    <p>This project enables real-time detection of objects and measurement of their sizes using a camera feed or images. It uses OpenCV for object detection based on Aruco markers and measurement based on a homogeneous background.</p>

  <h2>Installation</h2>
  <ol>
      <li>Clone the repository:</li>
      <pre><code>https://github.com/anandakumarak/Object-Size-Detection-Using-OpenCV.git</code></pre>
      <li>Install dependencies:</li>
      <pre><code>pip install opencv-python numpy</code></pre>
  </ol>

  <h2>Download Aruco Marker</h2>
  <p>To use Aruco markers as reference points for object size measurement, you can download them from the <a href="https://chev.me/arucogen/">Aruco Generator website</a>. Once downloaded, print the marker and place it in the view of the camera for measurement.</p>
  <img src="https://github.com/anandakumarak/OBJECT-SIZE-DETECTION-USING-OPENCV/blob/main/Images/aruco_demo.png" alt="Demo" width = "600">

  <h2>How It Works</h2>
  <p><li>Object Detection: The `HomogeneousBgDetector` class in `object_detector.py` is used to detect objects based on a homogeneous background. It converts images to grayscale, creates masks with adaptive thresholding, finds contours, and filters contours based on area to detect objects. Aruco markers are used as reference points for object size measurement. The markers are detected in the image or camera feed, and their perimeter is used to calculate a pixel to centimeter ratio.</p></li>

  <p><li>Object Size Measurement: For each detected object, the script calculates its width and height in centimeters using the pixel to centimeter ratio. It then draws bounding boxes around the objects with dimensions displayed.</li></p>
  <h2>Usage</h2>

  <h3>Live Object Detection (measure_object_size_camera.py)</h3>
  <ol>
      <li>Run the script:</li>
      <pre><code>python measure_object_size_camera.py</code></pre>
      <li>Position the camera:</li>
      <p>Point the camera towards the objects you want to measure. Ensure the objects are placed on a homogeneous background for accurate measurements.</p>
      <li>Use Aruco markers as reference points:</li>
      <p>The system uses Aruco markers as reference points for measuring object sizes. These markers should be visible in the camera frame along with the objects.</p>
      <li>View measurement results:</li>
      <p>The script will display the live camera feed with Aruco markers detected and object sizes measured in centimeters.</p>
  </ol>

  <h3>Image-Based Object Detection (measure_object_size.py)</h3>
  <ol>
      <li>Run the script:</li>
      <pre><code>python measure_object_size.py</code></pre>
      <li>Provide an image:</li>
      <p>Ensure you have an image (`phone_aruco_marker.jpg` in this example) with objects and Aruco markers visible.</p>
      <li>Detect objects and measure sizes:</li>
      <p>The script will load the image, detect objects, measure their sizes, and display the annotated image with object sizes.</p>
  </ol>

  <h2>Sample Output</h2>
  <p>Below is an example output image showing object detection and size measurement annotations:</p>
  <img src="https://github.com/anandakumarak/OBJECT-SIZE-DETECTION-USING-OPENCV/blob/main/Images/output_image.png" alt="Output Example" width = "900">



</body>
</html>

