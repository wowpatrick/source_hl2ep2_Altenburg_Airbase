# Export form Blender to Source Engine

1. Get Blender source tools and install http://steamreview.org/BlenderSourceTools/
2. In Blender, Join all objects to single one to export
3. Rename the object name (in the outliner scene tree)
4. Under `Scene`, got to `Source Engine Export` and choose `SMD` and `Export`

# Compile SMD to MDL

1. Create a qc file for the model https://developer.valvesoftware.com/wiki/Qc
    - `$cdmaterials` is the path to to the models VMT file relative to `<game>\materials\`
    - The actual file name for the VMT the model will look for is defined by the Blender model name (the one set as described above)
2. Compile the model via the `studiomdl.exe` with the Crowbar tool (http://steamcommunity.com/groups/CrowbarTool)

# Create the texture
1. Take the texture file from blender and convert it to the VTF format via VTFEdit (http://nemesis.thewavelength.net/index.php?c=238#p238)
2. Create a VMT (Valve Material Type) file https://developer.valvesoftware.com/wiki/Material
    - `$basetexture coast\filename` is the path relative to `<game>\materials\>` with the filename without extension (without .vtf)

## User model

Open the MDL + texture in the model viewer via Crowbar

## Debugging:
- In the Crowbar tool view tab, check for console output on VMT loading errors

## Links
- Blender Modelling Walkthrough: https://developer.valvesoftware.com/wiki/Blender_Modelling_Walkthrough
- Creating a Material: https://developer.valvesoftware.com/wiki/Creating_a_Material
- http://steamcommunity.com/app/1840/discussions/0/558747922882123231/#c558747922890334988