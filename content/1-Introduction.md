---
authors:
  - name: null
---


# 1 Introduction to the Laser Scanning Guide

## 1.1 Scope of this Guide

This document serves as a guide to good practice for the collection and archival of point cloud datasets and the additional derived products produced by terrestrial laser scanners in cultural heritage applications. It is recommended to read this guide in conjunction with Section 7 of the *Metric Survey Specifications for Cultural Heritage* [@bryan2009] titled *Standard Specification for the Collection and Archiving of Terrestrial Laser Scan Data* published by English Heritage. The *Metric Survey Specifications for Cultural Heritage* provides an excellent foundation for discussion of key project elements particularly project planning, data collection, and preliminary processing of terrestrial scan data and many of these points will be reiterated throughout this document. This guide builds upon the specifications provided by the *Metric Survey Specifications for Cultural Heritage* by broadening the scope to include such topics as accurate RGB/color acquisition and by also suggesting standards for archiving the derived products of point cloud datasets. Other key resources that were influential in the creation of this guide are *3D Laser Scanning for Heritage* [@eh2007] and *Theory and Practice on Terrestrial Laser Scanning* [@3driskmapping2008]. 

This guide is not a "How To" document that describes methods for collecting and processing scan data but rather a guide to inform individuals of key considerations and metadata elements to document in scanning projects that will allow them to easily archive and reuse their heritage datasets. The graphic below shows the key steps of data acquisition and processing, metadata documentation, and data archival for laser scan datasets. These key areas form the basis for discussion for Sections [2](2-AcquiringProcessing) and [3](3-Archiving) of this document; Section [1](1-Introduction) provides introductory material and Section [4](4-CSVirtualHampson) provides a case study and sample metadata. It is our hope that the metadata elements discussed here will easily integrate into most heritage scanning projects and will promote the ease in archiving and the long term preservation of these valuable datasets. 

```{figure} ../images/LaserScan_Fig1-small.png
:alt: Figure 1

__Figure 1:__ Scan Data Lifecycle with Metadata Elements and Archival Guidelines
```

## 1.2 What is Laser Scanning? 

Laser scanning is the process of recording precise three dimensional information of a real world object or environment. Terrestrial laser scanners are 'ground based devices' that can be used to scan at a range of scales from very small objects to very large monuments or entire sites. Laser scanners rapidly sample or scan an object's surface recording shape and often visual properties (intensity and/or RGB information). The information is returned to the unit as a dense collection of precisely measured XYZ points referred to as a point cloud.

```{figure} ../images/ls12-point_cloud_example.jpg
:alt: Figure 2.

__Figure 2:__ Pointcloud example
```


Point clouds produced by laser scanners contain a wealth of information on their own and can also be processed to create accurate 3D models of objects and environments as well as a host of other derivatives that are useful in a wide range of applications.  The three main types of terrestrial laser scanning technology are discussed below.

__What are the three principal types of scanning technology?__

The three principle types of scanning technology include Time of Flight (TOF), Phase Shift, and Triangulation-based systems.  Scanning technology is relative to other system factors including acquisition distance, acquisition rate and data resolution/accuracy.  Time of flight technology for example has the greatest acquisition range however TOF scanners often have slower acquisition rates and lower accuracy.  Phase shift scanners are often categorized as the "fastest" with some instruments scanning over 100,000 points/sec but most phase systems have a maximum range of 80 meters with some systems reaching up to 120 meters.  Both phase and time of flight systems can be used in terrestrial scanning applications where larger areas or structures of 5 meters up to multiple kilometers can be surveyed. Triangulation scanners, in contrast, typically have an operating range of less than 5 meters due to the limited field of view shared between the laser and camera.  Commonly, triangulation systems are referred to as short range systems and are most suited for scanning smaller objects ranging in size from 1 cm up to 2-3 meters (depending on the instrument).  Additional details on the individual scanning technologies are provided below.  


### 1.2.1 Time of flight

Long range laser scanning is typically performed by a Time of Flight scanner. In a TOF system a laser pulse is sent out and a portion of the pulse is reflected from a given surface and returns to the unit. The distance to the surface is calculated from the time of the flight of the pulse.  TOF systems can measure over great distances with some systems measuring objects over 1km away although a typical operating range for a TOF system is 5-300 meters. While TOF systems can measure over great distances, they typically have the slowest acquisition rates.  The accuracy of TOF technology is determined by the system’s ability to accurately measure the time of the returning signal. While accuracy specifications vary across different systems, typical accuracy for a TOF system is 4-10 mm.

More recent TOF systems include additional RGB capture options either through an internal camera or external camera option. The internal color capture is often ideal because the camera is mechanically or mathematically aligned with the laser scanning system so that the process of projecting the image data onto the point cloud is automatic and accurate.  However, the disadvantages of an internal system is that there are often fewer camera adjustment options for achieving consistent color across a group of scans.  An external camera option typically involves attaching a digital camera to or in place of a scanner, acquiring a set of images, and then mapping the images onto the data in processing software.  The image mapping process can be cumbersome, and if computed incorrectly, can result in subtle misalignments between the point cloud and image data.  However, external cameras offer more adjustment options and the images are more easily corrected in an image processing software if necessary.  External cameras typically also offer greater image resolution than most onboard systems. 

```{figure} ../images/long_range_scanning_machu_picchu2.jpg
:alt: Figure 3.

__Figure 3:__ Long range scanning at Machu Picchu
```

### 1.2.2 Phase Shift

Phase shift scanners emit laser light at alternating frequencies and measure the difference between the emitted and reflected signals to determine the distance to an object.  Phase shift systems have a maximum unambiguous range equal to a phase delay of one complete sine wave. This limits the effective range of most phase systems to less than 80 meters or 120 meters for some systems with a typical operating range of  1-50 meters.  Phase shift systems are among the fastest laser scanners with many systems claiming a collection rate of up to 100,000 points/second.  Commonly these systems also include motorized controls that allow automatic acquisition of surfaces around and above the scanners. As such, these systems are ideal for the scanning of interior rooms or similarly constrained areas. Phase shift systems, like time of flight systems, also typically include internal or external color capture options.

### 1.2.3 Triangulation

Short range scanners are used to scan individual objects (e.g. pottery vessels, tools etc.), inscriptions and detailed architectural features such as elaborate column capitals. Most short range scanners operate on the principle of triangulation where a laser is emitted and returned to a specific location on a CCD array of an inboard camera.  Most triangulation systems come with a set of lenses that alter the field of view of the system.  White light or fringe projection systems also employ the principle of triangulation.  Triangulation systems typically have an operating range of 0.5-2 meters and can collect data with micron-level accuracy. Most triangulation systems also come with an internal RGB capture option and, for accurate color capture during object scanning, a professional lighting setup must be used. 

A useful overview of laser scanning techniques and capabilities can be found in *3D Laser Scanning for Heritage* [@eh2007, 7, table 1].

### 1.2.4 Laser Classes and Safety

A brief outline of laser classes is provided below however for complete laser specifications, refer to the appropriate US (ANSIZ136) and/or international ([IEC 60825](https://webstore.iec.ch/en/publication/62424)) guidelines on laser safety.   In short, never stare directly at ANY laser regardless of laser class.

* Class 1:  Class 1 lasers are considered safe under all conditions of normal use. 
* Class 1M:  Class 1M lasers are considered safe under all conditions except for when the beam passes through magnifying optics.
* Class 2:  Class 2 lasers are considered safe because they typically cause a 'blink reflex' which protects the eye.
* Class 2M:  Class 2M lasers are considered safe because of the 'blink reflex' unless the beam passes through magnifying optics.  
* Class 3R:  Class 3R are considered safe if handled carefully and with restricted beam viewing.   Class 3R lasers can be hazardous where direct beam viewing is involved. 
*  Classes 1 – 3R are considered safe for survey in both the U.S. and in Europe.
* Class 3B:  Class 3B lasers are hazardous when direct beam viewing occurs though diffuse reflections of the laser are considered non-hazardous.  Class 3B lasers are generally not suited for survey applications.
* Class 4:  Class 4 lasers cause eye or skin damage as a result of direct beam exposure.  Class 4 lasers are also not suited for survey applications.

## 1.3 Applications of Laser Scanning: How is Laser Scanning used in Archaeology 

Given the fragile and temporal nature of archaeological sites, heritage monuments, and associated material goods, laser scanning offers amazing potential for digital recording and analysis in archaeology and heritage preservation. Simply scanning an historic monument in its current state or a collection of artifacts ensures that even if the physical structure or objects disappear, a digital copy is there for future observation and analysis. Numerous projects in archaeology have used scanning as a means of digital documentation and to also promote archaeology to the general public. Scan datasets have an obvious visual appeal that engages audiences. By scanning an object or site, the digital version of the object can easily be revisited, viewed from any angle or direction, and easily shared or disseminated to others. The [Virtual Hampson Museum](https://hampsonmuseum.cast.uark.edu/), for example, is an online repository of 3D scanned pottery from a museum in Northeast Arkansas. The online museum is a wonderful tool for the public because it provides worldwide access to an astounding collection of Native American pottery that most would not be able to see. The Virtual Hampson Museum is also great for researchers and archaeologists because it allows them to remotely study and analyze the collection using 3D processing software without physically having to travel to the museum. 

Apart from digital recording and data dissemination, the analytical potential of laser scanning in archaeology is being explored in more projects. Point cloud datasets can contain a wealth of information and the software used to process these datasets provide precise measurement tools for measuring point to point distances, volume, perimeter, and surface area calculations [@simon2009, 2].

Light raking and curvature mapping tools additionally provide the ability to accentuate features on an object that may not be easily observed by the naked eye or in photographs.

```{figure} ../images/ls13-colorstripping_curvature_mapping.jpg
:alt: Figure 4

__Figure 4:__ (Left) Object shown in full color (Middle) Object shown with color data removed to accentuate surface features (Right) Object with curvature map used to accentuate features and areas of high curvature
```

For example, in the [Stonehenge laser scanning project](https://stonehenge.archaeoptics.co.uk/scans.html), new carvings on some of the stones were revealed in the scan data that had not been observed in previous studies. Characteristic features in datasets such as pottery motifs can more easily, objectively, and repeatedly be extracted on the digital version of the object as compared to the physical version of the object. If used effectively, these types of measures can be automated across multiple datasets [@simon2009, 2].

```{figure} ../images/ls13-feature_extraction.jpg
:alt: Figure 5

__Figure 5:__ An example of feature extraction
```

While laser scanning is still relatively new in archaeology, archaeologists are finally beginning to see past the "eye candy" aspect of the data to discover the true analytical potential in applying this technology to past and future research directions in archaeology and heritage. 

## 1.4 Current issues or concerns 

### 1.4.1 Limitations of technology

The advantages of laser scanning are well known and have been cited in numerous publications. Laser scanning provides the ability to quickly, accurately, and remotely take thousands of measurements on any surface or landscape. The results from scanning produce a digital, scaled replica of the original object that can be observed and analyzed. As mentioned, some scanners also acquire RGB information which adds an additional photorealistic quality to scan models, and many also record intensity data, which can aid in the interpretation of materials. While laser scan data is initially handled as a point cloud, numerous products can be derived from the data including polygonal meshes, cross sections, and high precision measurements. In addition, scan processing software provides additional analyses and measurement options that are often not possible on the physical object such as extracting or accentuating features or subsections of an object or removing the color information from an objects surface to reveal subtle details in surface topography. In short, laser scan data, if acquired and processed correctly, can provide a digital copy of an object or environment that can be viewed and analyzed remotely.

While laser scanning has numerous advantages, there are also limitations to the technology that should be considered when evaluating whether or not scanning is suitable for a specific application. For example, certain surfaces such as or black and highly reflective surfaces can be very difficult to scan. Black materials absorb the laser energy while reflective surfaces tend to scatter the laser causing any data returned to be noisy. Translucent materials such as marble or bone are also problematic as the laser can actually penetrate these surfaces causing noisy data results for smooth surface areas.

Two additional considerations are beam divergence and data shadowing. Beam divergence is the expansion of the laser beam (in diameter) as it moves outward from the instrument. The graphic below (Figure 6) shows the effect of beam divergence (indicated by laser spot size in the graphic) at different ranges. The location of the measured point returned to the sensor can be anywhere within the bounds of the laser spot size. Therefore the data at greater distance can be less reliable and less accurate. There are ways to minimize the effects of beam divergence such as focusing the laser at greater distances but beam divergence is still an important consideration in projects.

```{figure} ../images/Lscan-fig2.jpg
:alt: Figure 6

__Figure 6:__ The effect of beam divergence at different ranges.
```

Data shadowing or laser shadowing is also common with terrestrial laser scanning. The laser beam essentially acts as a light source which will cause objects to shadow one another and holes or voids to appear in the data.

```{figure} ../images/ls141-laser_shadow.jpg
:alt: Figure 7

__Figure 7:__ Example of Laser Shadowing
```

The effects of laser shadowing can be minimized by acquiring multiple scans from multiple angles. However, in some cases, for example when trees or vegetation grow very close to a structure, data shadowing is unavoidable. Data shadowing can also occur when you have limited vantage points for scanning. For example when trying to acquire scans of roof features on a building from the ground, there are portions of the roof that will always be in shadow unless a high vantage point is available. While data shadowing is not completely unavoidable, the effects of shadowing (data voids) should be minimized in a project.

Finally, in addition to collecting surface measurements for an object, many laser scan systems include the option to collect intensity as well as color/RGB information. Intensity data is a measure of the reflective value of a surface and is typically displayed as grayscale whereas RGB data is full color.

```{figure} ../images/ls114-grayscale_intensity_RGB_data.jpg
:alt: Figure 8.

__Figure 8:__ Examples of Intensity and RGB data
```

While RGB collection adds a photo-realistic quality to scans, it can be difficult to collect accurate color information for an object. RGB color captured internally or externally to the scan system is subject to the lighting environment in which a scan is taken. If the lighting changes or fluctuates during the acquisition process, individual scans will vary in brightness and contrast across the object and can result in color artifacts if not properly adjusted during data processing. In short, when combining multiple scans across an object or structure, it can be a challenge to get uniform and consistent color across the object. 

### 1.4.2 Sources for error

While some common sources for error in laser scanning were briefly touched upon in the section above, there is an excellent, comprehensive discussion of error generation in Section 2.6 of the 'Theory and Practice on Terrestrial Laser Scanning' [@3driskmapping2008]. In this section, you will find detailed explanations concerning the effects of beam divergence, surface reflectivity, and environmental conditions.