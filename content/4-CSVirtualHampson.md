---
authors:
  - name: null
---

# 4 Case Study: Virtual Hampson Museum

## 4.1 Project Background

The [Virtual Hampson Museum](https://hampsonmuseum.cast.uark.edu/) showcases over 400 3D digital artifacts from the collections at the Hampson Archeological Museum State Park in Northeast Arkansas. Within the online museum, visitors can browse the 3D artifacts, read artifact descriptions and using the 3D viewer can manipulate and perform basic measurements on the objects directly within their browser interface using Adobe 3D PDF technology.  If interested in additional analyses, users can download the high resolution artifact models and freely provided 3D software for more robust 3D analysis.  Users also can view a series of 3D rendered images that show what the Native American village of Upper Nodena may have looked like.  The Upper Nodena village was where a lot of the original artifacts were found.
    
The Virtual Hampson museum project began in 2007 with the intent to digitally document and disseminate the amazing collection of Native American pottery vessels housed at Hampson Archeological Museum State Park.  The Konica Minolta VIVID 9i laser scanner was used to scan the artifacts.  The VIVID 9i also collects RGB color so all artifacts are documented in full color.   Over 500 artifacts were scanned over a period of 10 weeks split between two summer field seasons. A team of 3-4 individuals processed the artifacts over a period of two years.  

## 4.2 Description of Final Deliverables and Archival Preparation

For each digital artifact, a high resolution, full color polygonal mesh was created and published in the OBJ format.  Additional low resolution meshes (25000 triangles) were created and published in three standard formats: OBJ, VRML and PDF.   A digital video was also created showcasing the 3D artifact from multiple directions.  Additional digital images and descriptions are also provided.   All of the datasets and information described here are available on the Virtual Hampson Museum website. 

```{figure} ../images/LScan-fig3.jpg
:alt: Figure 15

__Figure 15__: The Virtual Hampson Museum website
```

For each artifact, the following datasets were selected for archival:

* Original scans with Project and Scan Level Metadata
* Registered dataset with Registration Metadata
* PreMesh dataset with PreMesh Metadata
* Mesh dataset with Mesh Metadata
* Decimated mesh dataset with decimated mesh metadata

## 4.3 Archival Metadata Example 

One of the digital artifacts, Ark_HM_Headpot, has been selected to show an example project metadata set below.

### 4.3.1 Acquisitional Metadata

The project level metadata below would be completed once for the entire project.
```{list-table}
:header-rows: 1
* - Project Level Metadata
  - Sample Entry
* - Project Name
  - Virtual Hampson Museum Project
* - Name of monument, survey area, or object
  - Ark_HM_Headpot
* - Monument/Object Number
  - NA
* - Survey Location
  - Hampson Archeological Museum State Park; Wilson, AR
* - Survey Date(s) of survey (Month/day/year)
  - 6-APR-2008
* - Survey Conditions
  - Indoors
* - Scanner Details
  - Konica Minolta VIVID 9i;  mm
* - Company/Operator Name
  - Center for Advanced Spatial Technologies, Christopher Goodmaster
* - Control data collected?
  - N
* - Turntable used?
  - Y
* - RGB Data Capture
  - Y. The VIVID 9i uses internal RGB capture.  A three point lighting system was used to illuminate the object from the top and from both sides; this minimized shadows on the object.  Each light in the system had 1-3 white light (5000k) flicker free fluorescent bulbs.  The number of bulbs that were used to illuminate each artifact varied depending on ambient light conditions and object color. 
* - Estimated Data Resolution
  - 0.35mm
* - Total Number of Scans in Project
  - 18
* - Archived Datasets
  - Original scans, registered dataset, premesh dataset, Mesh dataset, Decimated mesh dataset
* - Planimetric map of scan coverage areas
  - N
* - Additional project notes
  - NA
* - Images from survey
  - Y. Ark_HM_Headpot_001.jpg, Ark_HM_Headpot_003, Ark_HM_Headpot_004.jpg, Arka_HM_006.jpg, Ark_HM_Headpot_009.jpg, Ark_HM_headpot_010.jpg
```

The information in the scan level metadata table below would be completed for every scan in the project. This information could easily be created in a spreadsheet using the metadata elements as column headings and a row per scan.

```{list-table}
:header-rows: 1
* - Scan Level Metadata
  - Sample Entry
* - Scan Filename
  - Ark_HM_Headpot_scan1.txt
* - Scan Transformation Matrix
  - Ark_HM_Headpot_scan1_matrix.txt
* - Name of monument/object area
  - Ark_HM_Headpot
* - Survey Date
  - 6-APR-2008
* - Scan Number
  - 1 of 18
* - Number of Points in Scan
  - 160909
* - Additional Scan Notes
  - NA
* - Scanner Technology
  - Triangulation
* - Data resolution
  - 0.37
* - Lense or FOV Details
  - Tele lense
```

### 4.3.2 Registration Metadata

```{list-table}
:header-rows: 1
* - Registration Metadata
  - Sample Entry
* - Name of Registered Dataset
  - Ark_HM_Headpot_GR.txt
* - Total number of scans used in Registration/Total number acquired
  - 18 of 18
* - Global Registration Error in units (2 units precision)
  - 0.06
* - Total number of points in final registration
  - 3156822
```

### 4.3.3 Additional Products Metadata

```{list-table}
:header-rows: 1
* - Pre-Mesh Metadata
  - Sample Entry
* - Name of Pre-Mesh Dataset
  - Ark_HM_Headpot_GRE.txt
* - Number of points in file
  - 995742
* - Point Deletion Summary
  - Overlap reduction was computed in Polyworks software.  Following overlap reduction, floating data points were also deleted.   Data remnants from overlap reduction were also deleted. 
* - Overlap Reduction (Y/N) (optional)
  - Y
* - Smoothing (Y/N) (optional)
  - N
* - Subsampling (Y/N) (optional)
  - N
* - Color Editions (Y/N) (optional)
  - N
```

```{list-table}
:header-rows: 1
* - Mesh Creation and Editing Metadata
  - Sample Entry
* - Name of Mesh Dataset
  - Ark_HM_Headpot.obj
* - Estimated mesh spacing
  - .8
* - Holes Filled (Y/N)
  - Y
* - Smoothing (Y/N)
  - Y
* - Color Editions (Y/N) (optional)
  - N
* - Healing/despiking (Y/N) (optional)
  - Y
* - Total Triangle count (post editing)
  - 647169
* - RGB Color Included (Y/N)
  - Y
* - Data Reduction (Y/N)
  - N
* - Coordinate System Adjustment (Y/N)
  - N
* - Additional processing notes
  - NA
```

```{list-table}
:header-rows: 1
* - Decimated Mesh Metadata
  - Sample Entry
* - Name of decimated mesh dataset
  - Ark_HM_Headpot_25k.obj
* - Total Original Triangle Count
  - 647169
* - Decimated Triangle Count
  - 25000
* - RGB Color preserved from original dataset
  - Y
```