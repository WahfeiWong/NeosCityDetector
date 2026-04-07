NeosCityDetector is a Grasshopper plugin based on ONNX Runtime for semantic segmentation and object detection analysis of urban street view images. It supports loading pre‑trained deep learning models (e.g., SegFormer, YOLO in .onnx format), automatically extracting elements such as buildings, roads, vegetation, and pedestrians from images, and calculating a series of urban visual metrics (e.g., green view index, sky openness, color richness, etc.). The plugin outputs meshes, point clouds, and statistical results that can be directly used for Rhino geometry processing and Grasshopper dataflow analysis.

Users only need to provide an image path; the plugin automatically performs preprocessing, inference, and post‑processing, outputting pixel‑level classification results, object detection bounding boxes, and metrics such as Visible Green Index (VGI), Sky View Factor (SVF), Building View Factor (BVF), Road Area Index (RAI), Spatial Enclosure Index (SEI), pedestrian count, Color Richness Index (CRI), and Visual Entropy (VE), thereby supporting quantitative urban spatial analysis, urban design research, and practice.

Since configuring GPU‑accelerated inference is cumbersome for ordinary users, the first released version only supports CPU‑based inference. In actual tests, using CitySemSegFormer on a 16‑core, 24‑thread CPU, pixel‑level semantic segmentation of a 1820×1024 pixel street view image takes about 50 seconds, while object detection with YOLOv12 takes 1.7 seconds.

Note that the deep learning models (e.g., the semantic segmentation model CitySemSegFormer and the object detection model YOLOv12) need to be trained and converted to .onnx format by the user. The usage examples provide download links for two pre‑trained models.


Packages need：
Microsoft.Bcl.HashCode.6.0.0,
Microsoft.ML.OnnxRuntime.1.24.2,
Microsoft.ML.OnnxRuntime.Managed.1.24.2,
System.Buffers.4.6.1,
System.Collections.Immutable.10.0.3,
System.Formats.Nrbf.10.0.3,
System.Memory.4.6.3,
System.Numerics.Vectors.4.6.1,
System.Reflection.Metadata.10.0.3,
System.Resources.Extensions.10.0.3,
System.Runtime.CompilerServices.Unsafe.6.1.2,
System.ValueTuple.4.6.1

CitySemSegFormer Model link：
https://catalog.ngc.nvidia.com/orgs/nvidia/teams/tao/models/citysemsegformer?version=deployable_onnx_v1.0

YOLO Model link：
https://github.com/paulinavelasquez/YOLOv12-ONNX

As part of the Neos toolkit, after installation, the Category is Neos and the Subcategory is CityDetector. The developer completed testing on Rhino 8 SR27(Grasshopper1.8).

![describe](https://github.com/user-attachments/assets/63a83126-b7e0-44fb-9b3c-88c4506e0edc)

![sample1 2](https://github.com/user-attachments/assets/be83727b-ef97-473f-839b-ef88f7be55aa)

![0](https://github.com/user-attachments/assets/4abcb00f-2cf7-43a8-8c9b-32299d2b494b)

![1](https://github.com/user-attachments/assets/345213d4-62d8-4011-96a5-3d61f5cdacd3)

![2](https://github.com/user-attachments/assets/71c0c070-e71b-4a00-bfc4-ee29320a9146)

![3](https://github.com/user-attachments/assets/47484e68-ae10-4d39-8ab5-c6f28c0df5cb)

![4](https://github.com/user-attachments/assets/3c91d72b-79ab-4114-8f08-f95489e8667f)

![5](https://github.com/user-attachments/assets/f643eef6-05eb-4dc7-8298-e2c3a2c374c7)
