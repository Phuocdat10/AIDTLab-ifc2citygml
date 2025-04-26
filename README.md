# ifc2citygml
A FME workbench for transforming IFC to CityGML 2.0 as LoD 4 (however LoD 2 and 3 are possible, depending on different purposes)

# Requirement
FME workspace essentially outlines how data is extracted, transformed, and loaded from one format to another. Workspaces are the core of FME, allowing users to automate data integration tasks. Expected version 2022 or higher.

CityGML 2.0 is an open data model and XML-based format for the representation, storage, and exchange of virtual 3D city models. It supports multiple Levels of Detail (LODs) and enables semantic, geometric, topological, and appearance information to be integrated across various urban features. Refered in the [Open Geospatial Consortium Standard](https://www.ogc.org/standards/citygml/)

# Test dataset
Due to Smart City Lab data is private data that we can not publish. We gather some open data from :
* [ifc Wiki](https://www.ifcwiki.org/index.php?title=KIT_IFC_Examples)
* [DigitalHub](https://github.com/RWTH-E3D/DigitalHub)

# Mapping of IFC to CityGML 2.0 entities 

| IFC 2x3                 | CityGML 2.0             |
|-------------------------|-------------------------|
| IfcMember               | BuildingInstallation    |
| IfcWallStandardCase     | WallSurface             |
| IfcWall                 |                         |
| IfcCurtainWall          |                         |
| IfcBeam                 | BuildingInstallation    |
| IfcWindow               | Window                  |
| IfcSlab                 | FloorSurface            |
|                         | RoofSurface             |
| IfcRoof                 |                         |
| IfcPlate                | IntBuildingInstallation |
| IfcCovering             |                         |
| IfcDoor                 | Door                    |
| IfcBuildingElementProxy | BuildingFurniture       |
| IfcRailing              | BuildingInstallation    |
| IfcStairFlight          |                         |
| IfcBuilding             | Building                |
| IfcBuildingStorey       | BuildingPart            |
| IfcSpace                | Room                    |
| IfcColumns              | BuildingInstallation    |

# Result
* The below screenshot results dataset via FME Inspector 2025

Smart City Lab
<figure>
    <img src="./images/smartcitylab-citygml.png" width="600">
</figure>
<figure>
    <img src="./images/smartcitylab-citygml2.png" width="600">
</figure>

DigitalHub
<figure>
    <img src="./images/digitalhub-arcv2-1.png" width="600">
</figure>
<figure>
    <img src="./images/digitalhub-arcv2-2.png" width="600">
</figure>

AC20-FZK-Haus
<figure>
    <img src="./images/AC20-FZK-Haus.png" width="600">
</figure>

# Paper
* Lam, Phuoc-Dat, Bon-Hyeon Gu, Hoang-Khanh Lam, Soo-Yol Ok, and Suk-Hwan Lee. "Digital Twin Smart City: Integrating IFC and CityGML with Semantic Graph for Advanced 3D City Model Visualization." Sensors 24, no. 12 (2024): 3761. [https://doi.org/10.3390/s24123761](https://doi.org/10.3390/s24123761)

# References
* BIM to GIS (Intermediate) | IFC LOD 300 to LOD 4 CityGML [Link](https://support.safe.com/hc/en-us/articles/25407718003341-BIM-to-GIS-Intermediate-IFC-LOD-300-to-LOD-4-CityGML)
* Plateau Handbooks [Link](https://www.mlit.go.jp/plateau/libraries/handbooks/)