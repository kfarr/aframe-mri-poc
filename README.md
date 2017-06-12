# aframe-mri-poc
Proof of concept of showing MRI scans in 3D in WebVR using A-Frame

<img src="./assets/aframe-mri-poc.gif" />

This app is a very simple proof of concept showing sequential MRI scans of a friend's knee (thanks Tricky!) arranged in 3D space with low opacity to create an illusion of volume.

Use your mouse to <code>click</code> and <code>drag</code> to rotate the image. Use the <code>scrollwheel</code> to zoom in / out.

MRI scans are often provided in DICOM format. You can ask your doctor for your MRI scans and they'll usually provide it as a burned CD. There are many DICOM viewers out there, including a few web based JavaScript libraries for parsing DICOM format files:
* https://github.com/ivmartel/dwv
* https://github.com/chafey/dicomParser
* https://github.com/chafey/cornerstone

In theory it would be possible to make a "VR view" automatically from any DICOM compliant file. According to the web DICOM viewers, parsing images is tough because of variability between compression types on various MRI hardware, etc.

In this example I manually converted a series of 26 images from DICOM to JPEG images using <a href="http://www.microdicom.com/">MicroDicom</a> and simple copying them into Paint 3D and saving as a series of JPEGs.
