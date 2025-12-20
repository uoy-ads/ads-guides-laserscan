---
authors:
  - name: null
---

# 2 Acquiring and Processing Laser Scan Data

## 2.1 Project Planning and Requirements

### 2.1.1 Define project goals. How much field time is available?

Before beginning a project, it is best to identify the scan objectives (what to scan and how many), a list of deliverables, and any project limitations (such as limited field time). While one may wish to scan an object or structure at the highest resolution possible, practical limitations of time and processing power make this unrealistic. Key considerations including project goals and deliverables, data resolution, RGB/intensity data collection, and the use of survey targets need to be determined before entering the field. These issues are discussed in greater detail below.

In general, and significantly where laser scan data is used as the basis for visualisation techniques, data creators should be aware of the principles outlined in The London Charter [-@london2009] and, in particular, Principles 4 to 6 dealing with documentation, sustainability and access.

### 2.1.2 What is the appropriate point density/data resolution for an object? How does resolution affect file size?

Point density is defined as the average distance between XYZ coordinates in a point cloud. Point density or spacing is also referred to as data resolution. There are two primary considerations when trying to determine the appropriate point density for scanning an object and these include the minimum feature size to detect on the object and the accuracy of the scan system. According to English Heritage, the following formula can be used to determine an appropriate data resolution based on a minimum feature size:   *Q = 1 – (m/s)*

Where *Q* is the quality of the data (% confidence the object will be detectable), *m* is the point density on the object and *s* is the minimum feature size. For example, for an object with a minimum feature size of 6 mm (*s*) a scan resolution of 12 mm would be unacceptable where 2mm resolution (*m*) would indicate a 66% confidence (*Q*) that the feature would be detectable. English Heritage suggests, as a good rule of thumb, that "the point density be at least half the size of the smallest feature". [@eh2007, 7.2.4].

An additional consideration is the inherent accuracy of the scan system being used. For example, if a sample long range scanner has a tested system accuracy of 6mm, while the scanner can scan at a resolution lower than 6mm, doing so only increases the noise in the data and does not result in a finer measurement.  For finer measurements less than 6mm, a system with higher accuracy would therefore be required.

A final consideration with regards to point density is file size and scan time. Again while maxing out data resolution might be tempting, doing so greatly increases data acquisition time and resulting file size. The image below (figure 9) illustrates a comparison of different data resolutions and associated scan times and file sizes for a scan with a sample long range scanner.  

```{figure} ../images/ls212-resolution_filesize.jpg
:alt: Figure 9

__Figure 9:__ Examples of scan time and filesize at various resolutions.
```

Given the factors of field time, data resolution and quantity or size of objects to scan, the best approach is to develop a priority list of objects and appropriate data resolutions that can be modified as circumstances may change in the field. For additional information on point density in laser scanning, please refer to Section 7.2.4 'Point Density and Measurement Precision' in English Heritage's *Metric Survey Specifications for Cultural Heritage* [@bryan2009].

### 2.1.3 Will the project include RGB/Color data acquisition? What methods will be used?

If RGB data is acquired in the field, then the methods used for acquisition need to be documented. In general, RGB acquisition and post processing is a very complex process. Many scanners provide the ability to capture RGB data internally while there are also numerous options that allow the user to acquire and map separate digital images onto data (external). In either case, if accurate color acquisition is a priority to the project, the use of an additional lighting system is recommended to provide uniform lighting across a scan scene or object.

```{figure} ../images/ls213-poor_color_example.jpg
:alt: Figure 10.

__Figure 10:__ Poor color example
```

This is particularly relevant to scanning smaller objects but the principles of controlled lighting can be applied to large scenes as well. While additional lighting can help in achieving overall good color, if additional lighting is not available, good results can often be achieved by modifying the color data in post processing though the processes can be very time consuming. Before going out into the field, one needs to consider all of the different methods for color acquisition and processing and determine which methods will best achieve the project goals and ensure delivery of the project deliverables. 

## 2.1.4 Will targets be acquired? Will the data be referenced to a local or global coordinate system?

Target acquisition and coordinate system considerations apply primarily to terrestrial scanning of large structures or entire sites. The acquisition of targets can assist in the registration of the scan data and can also be used to tie a point cloud to either a local or global coordinates system. If targets are used, then a sketch plan of the target locations with associated target names is recommended. If targets are used as control points, then the control point file needs to be documented and saved as part of the project. While the use of targets is advisable, they are not required for a scan project. For additional information on target use and survey control, please reference Section 7.2.10 -7.2.11 of the English Heritage document [@bryan2009]. 

### 2.1.5 What are the intended deliverables for the project?

Finally, identifying a clear project objective and a set of deliverables is recommended at the onset of every project. Having a good idea of what you would like to accomplish can help in prioritizing scan objectives, determining appropriate data resolution, and resolving any conflicts that can arise in the field. Related to project objectives are the intended deliverables for the project. These can range anywhere from the raw point cloud to a completed 3D mesh to a series of CAD drawings represented as plans and elevations. For additional discussion on the different types of deliverables, please see Section 2.4 below.

__Minimum deliverables for archiving__

The standard deliverables listed by English Heritage [-@eh2007, Section 7.3.1] include the individual raw scans, the final registered point cloud, and all associated metadata elements including the project metadata, scan metadata, and registration metadata. These will continue to be the minimum requirements for archiving scan datasets. Providing that a site or object is surveyed correctly and completely, the original registered point cloud acts as digital replica to the original object and contains a wealth of information on its own. The registered point cloud can be used to extract precise measurements and for visualization purposes and it can also be used as a starting point in creating additional project deliverables.

__Additional Products__

If additional products are made from the original registered point cloud, it is also __strongly advised__ to archive the final product as well as the interim dataset used in its creation.

Creating deliverables beyond the original registered point cloud can involve a lot of complex processing. It is impossible to document and summarize every detail from processing operations and variations between software make it difficult to assign preset values for the most common processing operations. For example, a mesh smoothing algorithm in one software may allow the user to identify specific numeric values for smoothing radius and smoothing tolerance while the same operation in another software may offer low, medium, and high preset smoothing parameters. Therefore the metadata elements suggested for additional scan deliverables are minimal. Instead we emphasize that, for all products generated beyond the original registered point cloud, the 'interim level datasets' used to create the product also are archived.

* For a __polygonal mesh__ for example, the interim level dataset would be the original registered point cloud that has had additional editing (overlap reduction, etc.) to prepare the point cloud for meshing.
* For a set of __cross sections__, the interim level dataset could be the original registered point cloud or a polygonal mesh file.

The interim dataset is important because it is the essential link between the original registered point cloud and the derived product and completes the processing pipeline from beginning to end. This is important for assessing a product's validity and for understanding the processes used to create the final product and how these may or may not have deviated from the original dataset. If the coordinate system is also edited in processing, the user will need to archive any additional transformation matrices. These are important for guaranteeing that the final product, the interim dataset, and the original point cloud can all be overlain on to one another for comparability and assessment. 

## 2.2 File Naming Conventions
  
For a general discussion on file naming, please refer to the general section on *Planning for the Creation of Digital Data*. As a good rule of thumb, file names should be logical and should not contain special characters. In the metadata sections below, file names are suggested for each of the interim data sets generated from processing scan data. For example, it is suggested that all datasets be prefixed by the project name followed by a brief description or shorthand of what the dataset contains.

Registered point clouds for example should be called "*projectname_GR.txt*" to indicated that the file contains a point cloud data set that has been globally registered.

As another example, mesh files should be described as "*projectname_origmesh.obj*" to describe an original full resolution mesh or "*projectname_decimesh_50pcnt.obj*" to describe a decimated mesh and the amount of data reduction from the original. The file naming suggestions in this document are not required for archive but if used, can provide a good framework for structuring scanning projects.

## 2.3 Scan Data Lifecycle

Point cloud data sets produced by laser scanners are rarely used in raw, unedited form. Typically individual scans are registered to a common coordinate system and the unified point cloud is used to create any number of products. The products derived from scan data can vary across projects and can include polygonal models, extracted measurements and features, CAD models, videos, animations and more. Products can be derived at different stages in the processing pipeline and it is essential to document key processing steps that directly affect the quality of the final product. A summary of the processing work flow is provided here.

### 2.3.1 Collect Scans

* During data collection, it is advised to record the project and scan level metadata detailed in __Section 3.2__ below.

The process of collecting scan data is often fairly straight forward providing that key project elements such as project objectives, data resolution, and scan time have been evaluated. The scan operator will typically position the scanner and capture data at multiple locations around a subject while ensuring adequate overlap in the data between scans. According to the *Metric Survey Specifications for Cultural Heritage* [@bryan2009, 7.2.6] data overlap is important for the data registration process and also ensures complete documentation of the object or environment. Also, in the process of ensuring data overlap, the scan operator should try and minimize data voids or holes in the data (see ibid. section 7.2.7 for a discussion on data voids).

For terrestrial laser scanning of large objects or sites, it is also advised to collect a series of overview and detail scans to provide an accurate picture or context for the entire dataset [@bryan2009, 7.2.5]. If targets are acquired, it is necessary to obtain high resolution scans of each individual target face to ensure that the data density is sufficient for target recognition by the system software. A map of all scan locations as well as target locations is also advised and required for data archiving. Project planners should also employ suitable methods for accessing hard to reach places or high areas within a site (see @bryan2009, section 7.2.8 for a discussion of High Level Coverage). In instances where RGB acquisition is included, additional care may be required in setting up and maintaining a uniform and well-lit environment.

For scanning smaller objects, the use of a turntable is advised (if feasible) and will greatly facilitate data acquisition. Many scan systems are integrated with turntables and processing software such that the scan data enters the software roughly co-registered based on the identification of the central vertical axis of the turntable. If a turntable is not feasible or if an object is too large to be placed on a turntable, then the process of collection is similar to that used for scanning large objects where the scanner is repositioned manually around the object with efforts made to ensure adequate overlap between scans and to minimize data voids. If RGB acquisition is a priority, then it is advised to set up and maintain a uniform and well-lit scanning environment.                

### 2.3.2 Register scans to common coordinate system

* During data registration, it is advised to record the registration metadata detailed in __Section 3.3__ below as well as save the individual transformation matrices for each scan.

Registration is the digital reassembly of the scanned object or structure from a series of individual scans. The process of registration involves combining multiple scans into a single coordinate system. Registration is performed by identifying common features or tie points between scans. The tie points can either be targets that were acquired and identified in the field or a series of manual pick points identified by the user in the software. Once all scans have been registered then a final global registration is performed to fine-tune the quality of the overall registration. The overall quality of the registration is reflected in the standard deviation value for the global registration which in all projects should ideally be less than the accuracy of the laser scan system that was used.

Registration can also involve georeferencing the point cloud to a real world local or global coordinate system. If a series of control points were collected in the field, these control points are typically entered into the processing software and the point cloud is then registered to the control. The process of georeferencing a point cloud is not required although most traditional structure or site surveys will include it as part of their workflow.

For more information on the different registration methods, please see Section 7.3.2 of the *Metric Survey Specifications for Cultural Heritage* [@bryan2009].

## 2.4 Scan Data Deliverables

Once a point cloud dataset has been co-registered then it can be used to generate any number of different products. Point cloud datasets are typically only viewable in the software used to process them so an emphasis is placed on creating or extracting products from the point cloud that are useful in other applications. For smaller artifacts or objects, the most typical product is a polygonal mesh [@eh2007, 12]. A polygonal mesh is created by connecting neighboring points to create a surface representation of an object. The process of creating and refining a mesh is very complex and is detailed more in the meshing section below. For larger structures and entire sites, the processing workflow is a bit more varied [@eh2007, 13]. Different deliverables can include a polygonal mesh, 2D CAD drawings (plans, elevations, and sections), 3D CAD drawings (complete surface models), digital elevation models (DEMs), cross sections, or an animation/flythrough of the dataset. Either the registered point cloud or a meshed product can be used to generate the different deliverables listed above.

### 2.4.1 Create and edit polygonal mesh

__Preparing the point cloud for meshing__

* During pre-mesh editing, it is advised to record the premeshing metadata detailed in __Section 3.4__ below.

The process of creating a complete polygonal mesh for an object involves numerous steps including data cleaning, resampling, meshing/triangulation, hole filling, and mesh optimization [@3driskmapping2008, 57]. To prepare the registered point cloud for meshing, the point cloud will often have to be cleaned to remove extraneous data points and overlapping or redundant data. Overlap reduction is available in most processing software as an automatic operation that computes the best data for an area based on either distance to the scanner (the points that are closer are given priority) or viewing angle (points more orthogonal to the scanner are given priority). Some software also provide the option to average all overlapping scans. Overlap reduction is used to remove redundant data and to also decrease the size of the point cloud to optimize it for meshing. In addition to overlap reduction, users may wish to smooth or subsample the dataset. Subsampling also reduces the size of the point cloud and smoothing the point cloud can filter out noise caused by the scanner though smoothing can also remove fine details and should be used cautiously.

If RGB data is a priority, then the color between the scans will need to be adjusted in the pre-meshing stage. Color editing tools including brightness, contrast, and hue adjustment are available in some processing software. An effort should be made to balance these three parameters across a series of scans so that no artifacts or 'seams' can be observed in the RGB data for the entire object. 

In addition to the edits described above, the user will also often manually delete erroneous data that was not automatically removed by one of the processes described above. These manual deletions can include random or irrelevant data points, remnant data from the overlap reduction process, or data that is of poor color quality. All operations including overlap reduction, subsampling, smoothing, RGB editing, and manual edits should be summarized in the metadata section. 

__Creating and editing a polygonal mesh__

* During mesh creation and editing, it is advised to record the meshing metadata detailed in __Section 3.5.1__ below.

Meshing is the process of connecting points to create a surface representation of an object and typically involves combining multiple scans over a given object or area. Different algorithms exist to create meshes from point clouds, one of the most common is Delaunay Triangulation [@3driskmapping2008, 57]. While it is not essential to know the exact meshing technique used in a software, it is good to have a basic understanding of the input parameters that can affect the result of a meshing operation. These parameters can include a distance criterion used to connect points, optional smoothing, subsampling, and optimization techniques. The most important of these is the distance criterion used to connect points. If set to large, then points can erroneously be connected giving the data a 'stretched' appearance while if set to small, then not enough points are connected causing the data to look to 'sparse'. A good rule of thumb is for the distance value to roughly be 10 times the interpolation step (resolution of the data set). Additional parameters to adjust can include smoothing and subsampling. A low level smoothing filter can help reduce scanner noise in the data however if minute details are important in the final mesh product it is generally advised to not smooth the data during the meshing process. It is generally advised to reserve all smoothing, subsampling, and mesh optimization operations for post mesh processing where the results can be directly observed. 

Mesh editing can be a very complex process. Mesh editing can include a number of operations including hole filling, smoothing, despiking, color editing and/or texture mapping and others. The purpose of mesh editing is to create a final mesh product that best represents the original scanned object. The primary operation is hole filling where holes or voids in the dataset are 'filled in' using either flat or curvature based filling algorithms. Scanning from multiple positions and angles should minimize holes in the data however complex object shapes can be a challenge. Hole filling is often available in processing software as both automated and manual processes.

Despiking is generally recommended for removing spikes in the data caused by extraneous data points and is also typically an automated process. Smoothing is also very important for removing scanner noise and other artifacts that can occur as part of scan acquisition and data processing. Smoothing is typically an automated process where the user can specify the strength of the smoothing filter and additional manual or interactive smoothing is often available for smoothing a specific area of an object. Additional mesh optimization operations can include retriangulate/remesh operations where the mesh is literally remeshed to remove imperfections that have occurred as part of the mesh editing process. Additional optimization can include decimation where the number of triangles in a mesh are reduced to optimize data handle-ability or to create lower resolution deliverables.

Finally RGB editing and or texture mapping is an important part of the mesh editing process in projects where a creating a 'photo realistic' model is important. For models where RGB data has been collected as part of the point cloud, the colors of the individual scans should ideally be adjusted to match one another in the premeshing stage. Once a mesh has been created from individual scans then the overall color of the meshed model can be adjusted for the whole object. Alternately, users may wish to apply color data by mapping a series of photos onto the meshed product. The process of texture mapping in a given software typically allows the user to identify common points or identifiable features between the 3D dataset and the image. For the most accurate color, texture mapping also requires for individual photos to be color balanced to one another to ensure consistent color across the entire 3D project.

### 2.4.2 Create 2D CAD models (Cross Sections, Plans and Elevations)

* During 2D CAD Creation, it is advised to record the metadata detailed in __Section 3.5.2__ below.

2D CAD drawings including cross sections, plans, and elevations can be created from the original registered point cloud or a meshed product. While numerous algorithms are available to automatically identify and extract features of interest from a 3d dataset, all automatic feature extraction requires some amount of manual editing and human interpretation [@3driskmapping2008, 56]. Cross sections can automatically be generated or 'fitted' to an object often requiring the user to specify the axis direction, number of desired sections, and fit tolerance. Automatically fitting cross sections is most successful when applied to small meshed objects that are completely enclosed otherwise additional editing is often required. A manual method for creating sections involves slicing a dataset along a specific direction using clipping planes to isolate a section of points and then manually tracing the perimeter of the points.

Creating plans and elevations is a similar process that involves the extraction and/or manual tracing of features of interest directly on the point cloud or mesh and then projecting those line tracings onto a plane to create the final plan or elevation product. The process of manual feature tracing can be a difficult, time consuming task that requires a lot of skill [@3driskmapping2008, 56]. During the process, the user will make assumptions and decisions about how to handle data voids, how to reconstruct sharp edges, whether or not to constrain geometries to 90&#xB0;, and more. The user's skill set and understanding of the data and the scanned object influences the decisions that are made and therefore directly affects the results of the end product. Here, we reiterate again to compare the derived product to the original dataset and/or provide fit statistics in order to be able to assess the validity of a final product.

### 2.4.3 Create 3D CAD Model

* During 3D CAD Creation, it is advised to record the metadata detailed in __Section 3.5.3__ below.

A 3D CAD model is a collection of 3D primitives that are fitted to a point cloud. 3D CAD models do not typically include all of the subtle details of the original dataset but instead are understood as models or representations of the data. Standard 3D primitives can include planes, cylinders, cubes, and spheres and can also include more complex 3D shapes that have been extracted from 2D lines or curves. Fitting standard 3D primitives typically involves selecting a portion of the data that is a generic 3D shape and then invoking a command that 'fits' the predefined shape to the selected area. Numerous statistics that show the size, volume, and fitting error of the shape inform the user how well the shape actually approximates the selected area. Additionally 2D profiles of 3 dimensional shapes can be traced on a dataset using the methods described above in the 2D Modelling Section and then extruded to create 3D geometries. Methods used for creating 3D geometries from 2D lines/curves include extruding, lofting, and revolution around an axis. 3D CAD models, like meshes, can also have image texture maps.

```{figure} ../images/ls233-CAD_Example.jpg
:alt: Figure 11.

__Figure 11:__ 3D CAD example
```

Both 2D and 3D CAD modeling require a lot of skill and are often very time consuming. All 2D/3D CAD models should be checked against the original dataset to verify the quality of the final CAD product. 

### 2.4.4 Create Digital Elevation Model

* During DEM Creation, it is advised to record the metadata detailed in __Section 3.5.4__ below.

Digital elevation models (DEMs) are typically created from airborne laser scanning datasets but can also be created from terrestrial datasets as well. DEMs are a digital representation of a surface usually in a raster or image based format where each square or pixel has a height or elevation value. DEMs are best suited for terrestrial point cloud datasets that are 2.5D in nature. A 2.5D dataset can be fitted to a plane where for every X,Y position there is only one Z value. Converting point cloud data to a DEM can be very useful for employing GIS raster analyses to accentuate or extract features from a dataset. For example, one could use curvature or slope based analyses to accentuate engravings on a flat stone surface. Spatial filtering to determine data patterns and trends is another useful tool in GIS software. DEMs can be created from exporting a point cloud dataset to a GIS package and then generating either a TIN (Triangulated Irregular Network) surface or a DEM raster. The resolution of the DEM is a key consideration because a DEM employs uniform point spacing and most terrestrial datasets, unless acquired exactly perpendicular to a surface, are not. So, if the resolution is too course, important details may be lost or if it is too fine than details will be retained from some areas and data artificially generated in others. For more information on DEMs, please refer to the DEM section in the GIS Guide to Good Practice. 

### 2.4.5 Create video/animation of dataset

* During video creation, it is advised to record the metadata detailed in __Section 3.5.5__ below.

Videos or animations are often the most effective manner in which to illustrate the true 3D quality of a dataset in a 2D medium. Most software offer simple animation wizards that allow the user to record simple object rotations or to fly around in a 3D scene. Videos can typically be recorded for most data types including point clouds, meshes, and 2D/3D CAD models. Technical considerations for creating videos include video resolution, codec selection and compression, file size, and dissemination. For more information see the separate Digital Video guide.