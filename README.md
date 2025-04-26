# ifc2citygml
A FME workbench for transforming IFC to CityGML 2.0 as LoD 4 (however LoD 2 and 3 are possible, depending on different purposes)

# Requirement
* FME workspace essentially outlines how data is extracted, transformed, and loaded from one format to another. Workspaces are the core of FME, allowing users to automate data integration tasks. Expected version 2022 or higher.

* CityGML 2.0 is an open data model and XML-based format for the representation, storage, and exchange of virtual 3D city models. It supports multiple Levels of Detail (LODs) and enables semantic, geometric, topological, and appearance information to be integrated across various urban features. Refered in the [Open Geospatial Consortium Standard](https://www.ogc.org/standards/citygml/)

# Mapping of IFC to CityGML 2.0 entities 
|:-----------------------:|:--------------:|:---------------------:|:---------------:|:--------------------:|:-----------------------:|
|          IFC2x3         |                |                       | Temporary/Final |      CityGML2.0      |                         |
|:-----------------------:|:--------------:|:---------------------:|:---------------:|:--------------------:|:-----------------------:|
|        IfcEntity        | PredefinedType |        Category       |                 |       Base Name      |     CityGML tagName     |
|        IfcMember        |        *       | Curtain Wall Mullions |    Temporary    |        Member        |   BuildingInstallation  |
|   IfcWallStandardCase   |        *       |         Walls         |      Final      |         Wall         |       WallSurface       |
|         IfcWall         |        *       |         Walls         |      Final      |                      |                         |
|      IfcCurtainWall     |        *       |         Walls         |      Final      |                      |                         |
|         IfcBeam         |        *       |   Structural Framing  |    Temporary    |         Beam         |   BuildingInstallation  |
|        IfcWindow        |        *       |        Windows        |      Final      |        Window        |          Window         |
|         IfcSlab         |      FLOOR     |         Floors        |      Final      |         Floor        |       FloorSurface      |
|                         |    BASESLAB    |         Floors        |    Temporary    |       BaseSlab       |                         |
|                         |      ROOF      |         Roofs         |      Final      |         Roof         |       RoofSurface       |
|         IfcRoof         |        *       |         Roofs         |      Final      |                      |                         |
|         IfcPlate        |        *       |     Curtain Panels    |    Temporary    |         Plate        | IntBuildingInstallation |
|       IfcCovering       |     CEILING    |        Ceilings       |    Temporary    |       Covering       |                         |
|         IfcDoor         |        *       |         Doors         |      Final      |         Door         |           Door          |
| IfcBuildingElementProxy |        *       |     Generic Models    |    Temporary    | BuildingElementProxy |    BuildingFurniture    |
|        IfcRailing       |   NOTDEFINED   |        Railings       |      Final      |        Railing       |   BuildingInstallation  |
|      IfcStairFlight     |   NOTDEFINED   |      Stairs: Runs     |      Final      |      StairFlight     |                         |
|       IfcBuilding       |        *       |  Project Information  |      Final      |       Building       |         Building        |
|    IfcBuildingStorey    |        *       |         Levels        |      Final      |     Part (level)     |       BuildingPart      |
|         IfcSpace        |        *       |         Rooms         |      Final      |         Room         |           Room          |
|        IfcColumns       |        *       |        Columns        |    Temporary    |        Columns       |   BuildingInstallation  |
|:-----------------------:|:--------------:|:---------------------:|:---------------:|:--------------------:|:-----------------------:|

# Paper
* Lam, Phuoc-Dat, Bon-Hyeon Gu, Hoang-Khanh Lam, Soo-Yol Ok, and Suk-Hwan Lee. "Digital Twin Smart City: Integrating IFC and CityGML with Semantic Graph for Advanced 3D City Model Visualization." Sensors 24, no. 12 (2024): 3761. [https://doi.org/10.3390/s24123761](https://doi.org/10.3390/s24123761)

# References
* BIM to GIS (Intermediate) | IFC LOD 300 to LOD 4 CityGML [Link](https://support.safe.com/hc/en-us/articles/25407718003341-BIM-to-GIS-Intermediate-IFC-LOD-300-to-LOD-4-CityGML)
* Plateau Handbooks [Link](https://www.mlit.go.jp/plateau/libraries/handbooks/)