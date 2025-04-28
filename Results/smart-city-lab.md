# Smart City Lab

## Overview
Smart City Lab (SCL) dataset

## Quantity Checking Table
| Element                   | IFC Quantity | → CityGML Mapping          | CityGML Quantity | Mapping Match |
|:--------------------------|:------------:|:---------------------------|:----------------:|:-------------:|
| **IfcBuilding**           | 1            | **Building**               | 1                | ✅ Yes       |
| IfcFlowTerminal           | 14           | **Building Installation**  | 1078             | ❌ No        |
| IfcBuildingElementProxy   | 932                                                                          |
| IfcBeam                   | 94                                                                           |
| IfcRailing                | 2                                                                            |
| IfcStairFlight            | 2                                                                            |
| IfcStair                  | 2                                                                            |
| IfcMember                 | 0                                                                            |
| IfcPipeSegment            | 39                                                                           |
| **IfcBuildingStorey**     | 5            | **BuildingPart**           | 5                | ✅ Yes       |
| **IfcDoor**               | 33           | **Door**                   | 33               | ✅ Yes       |
| **IfcSlab [Floor]**       | 169          | **FloorSurface**           | 169              | ✅ Yes       |
| **IfcSlab [BaseSlab]**    | 6            | **OuterFloorSurface**      | 6                | ✅ Yes       |
| IfcCovering               | 13           |                            |                  |               |
| **IfcColumn**             | 105          | **IntBuildingInstallation**| 118              | ✅ Yes       |
| **IfcSite**               | 1            | **LandUse**                | 1                | ✅ Yes       |
| **IfcSlab [Roof]**        | 0            | **RoofSurface**            | 0                | ✅ Yes       |
| IfcRoof                   | 0            |                            |                  |               |
| **IfcRoad**               | 1            | **Road**                   | 3                | ✅ Yes       |
| IfcRoadPart               | 2            |                            |                  |               |
| **IfcSpace**              | 0            | **Room**                   | 0                | ✅ Yes       |
| IfcWallStandardCase       | 0            |                            |                  |               |
| **IfcWall**               | 665          | **WallSurface**            | 665              | ✅ Yes       |
| IfcCurtainWall            | 0            |                            |                  |               |
| **IfcWindow**             | 28           | **Window**                 | 28               | ✅ Yes       |



[!NOTE]
> Mapping is provisional for some complex classes (e.g., BuildingInstallation). <br>
> Future updates will improve ontology accuracy.

## Visualization Overview

SCL represented in CityGML 2.0
![SmartCityLab-Overview](/Images/smartcitylab-citygml.png "SmartCityLab")

SCL - BuildingInstallation, Doors, Windows
![SmartCityLab-Overview](/Images/smartcitylab-bldgInstallation-window-door.png "SmartCityLab")

SCL - FloorSurface, OuterFloorSurface
![SmartCityLab-Overview](/Images/smartcitylab-floor-outerfloor.png "SmartCityLab")

SCL - Unity <br>
![SmartCityLab-Overview](/Images/smartcitylab-unity.png "SmartCityLab")
