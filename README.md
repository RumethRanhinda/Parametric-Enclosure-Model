# Parametric-Enclosure-Model

An adaptable, equation-driven 3D enclosure model built in SOLIDWORKS. By simply adjusting a small set of global variables, this single model can generate a practically infinite number of enclosure variations without breaking the geometry or requiring a complete redesign.

##  Key Features
* **Fully Parametric:** The entire design is driven by global variables and a network of equations.

## Prerequisites
* **Software:** SOLIDWORKS 2020 or newer.

##  How to Use / Modify
To generate a new variation of the enclosure, you only need to modify the Global Variables.

1. Open the `Full_Assem.SLDASM` file in SOLIDWORKS.
2. In the FeatureManager Design Tree, expand the **Equations** folder.
3. Right-click **Equations** and select **Manage Equations**.
4. In the Global Variables section, adjust the `Value / Equation` column for the desired parameters.
5. Click **OK** and rebuild the model if necessary.


###  Primary Global Variables
*Here is a list of the main variables you can tweak:*

| Variable Name | Default Value / Equation (mm)| Description |
| :--- | :--- | :--- |
| `"PCB_LEN"` | `70` | Length of the PCB |
| `"PCB_WIDTH"` | `35` | Width of the PCB |
| `"PCB_THICKNESS"` | `1.6` | Thickness of the PCB |
| `"MOUNTING_DIR"` | `3` | Diameter of the screw holes of the PCB |
| `"CLEARANCE"` | `0.4` | Clearance accounting for 3D printing errors |
| `"WALL_THICKNESS"` | `1.5` | Enclosure wall thickness |
| `"PCB_SIDE_CLEARANCE"` | `3` | Clearance between the PCB and the wall |
| `"BOTTOM_CLEARANCE"` | `2.5` | Clearance between the PCB and the bottom of the enclosure |
| `"TOP_CLEARANCE"` | `5` | Clearance between the midpoint of the USB connector to the top of the enclosure |
| `"COMMON_FILLET"` | `"WALL_THICKNESS"` | Fillet value that is commonly used |
| `"PCB_MOUNT_CLEARANCE"` | `3` | Clearance from the edge of the PCB to the centre of mounting hole of the PCB |

## Limitations & Constraints
Due to the complexity of equations, extreme values may cause certain fillets, cuts, or internal features to intersect or fail. It is recommended to stay within reasonable constraints of the base geometry. 



