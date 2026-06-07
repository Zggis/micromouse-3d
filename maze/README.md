# Building the Maze

MM3D is intended to be an 'add-on' to an already assembled Micromouse maze which serves as the base and first level. While the dimensions of walls and pillars are well established the base used for Micromouse mazes vary. Some mazes use sheets of plywood with a grid of holes and others use an entirely 3D printed structure.

If you do not have a Micromomouse maze, additional parts are provided in this repository to create one, you can find them [here](/base/).

All the 3D print files for MM3D are available in the subdirectories. Additional README files can be found in each directory explaining what the part is used for and the recommended print settings for it.

## What you need

In addition to parts you can 3D print, you will need to purchase the following:

| Part                                    | Retail Link                       | Description                                                                                                                                                                                            |
|-----------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 15/64" x 1-1/4" (6mm) Wooden Dowel Pins | [Amazon](https://a.co/d/0eMDBzNE) | I recommend the RHINO brand to ensure the tolerances are compatible with the 3D printed parts.                                                                                                         |
| Cyanoacrylate Glue (Super Glue)         | [Amazon](https://a.co/d/03UX3yRg) | Used to glue pegs into the 3D printed pillars.                                                                                                                                                         |
| 6"x6" 1/8" Thick Clear Acrylic Sheets   | [Amazon](https://a.co/d/02cTOcOn) | These are <strong>optional</strong>, they can be substituted with a 3D printed part. Using them is beneficial as it reduces 3D printing and allows you to see your robot traveling on the level below. |

## Printing Guidelines

### File Types

This repository includes STL and STEP format files for 3D parts. STEP format includes more detail and should be used over STL if your slicer supports them. Popular slicers such as Bamboo Studio, Prusa Slicer, and Orca Slicer support STEP files.

### Dowel Holes

Some parts require you to insert 6mm wooden dowels. The dowels mentioned above can vary in diameter, I have measured between 5.6mm - 5.85mm. To help accommodate this variation, all parts requiring dowels are available with three different size dowel holes. You can print the dowel test part in this directory to help you determine which size to use for which part.

| File Type Suffix | Dowel Hole Diameter |
|------------------|---------------------|
| _60              | 6.0mm               |
| _61              | 6.1mm               |
| _62              | 6.2mm               |

- For the pillars, I recommend starting with a loose fit. Dowels will be glued into them which should hold them securely.
- For Vertex and Ramp, I recommend a very snug fit.
- From my experience, a batch of dowels is pretty consistent. If you switch bathes, you should recheck the fit.

### Print Settings & Orientation

If using the STEP files, slicers will ignore any coordinate system included in the file, so you will need to orient them correctly using the recommended orientation included with the print settings. These settings can be found in the README files in the corresponding component directories. If you are confused about a part's print orientation, open the STL file which will be oriented correctly.

### Material

I printed all the parts in PLA. Other materials may cause parts to shrink and impact the tolerances. You can try to scale the parts up in your slicer to account for this, but I have not tested it.

Try to keep printed parts away from direct sunlight, the connectors in particular can droop if they are exposed to heat while assembled.

### Calibration

Some of the printed parts rely on tolerances of 0.1mm. I suggest printing a few interconnected parts to check the tolerances and make sure they fit together correctly before printing them in bulk. If you find the tolerances are too small or too large you can perform a skew calibration on your printer which should help bring it into alignment with the level of precision the parts are designed with. All of my printers have been calibrated using the free Calistar method you can find [here](https://github.com/dirtdigger/fleur_de_cali).

## Components

There are four main components to MM3D:

### Ramp

The MM3D ramp is divided into three printed sections which slide together. The ramp allows your robot to travel between levels. You generally only need one ramp per level, but some event types may require more.

### Supports

There are two ways you can support the lattice structure:
+ Using pillars with integrated support. This requires less printing and does not take up cell space. They can only be used on upper levels to support levels 3 and up since they require a 6mm anchor hole. If your base uses 6mm diameter holes, you can use these to support the second level.
+ Using the elevated cell which sits in an open cell. This requires more printing but is compatible with any maze that meets the standard Micromouse dimensions.

### Lattice Structure

The lattice is made from connectors and vertices which form the grid frame for cells on the upper levels. If you are using the elevated cell to support the lattice, you do not need to print the vertices since the connectors will connect directly to the elevated cell.

### Cell Inserts

For the cell inserts, you can use 6"x6" 1/8" thick plastic sheets such as the clear acrylic sheets mentioned above, or you can print the cell inserts provided in this repository. Cells that use the elevated cell do not need a cell insert.

## Assembly

Once you have all the components, the assembly is pretty straightforward.

The ramp pieces slide together and can be inserted into the maze sliding it up against a wall. The ramp edge should be right at the threshold of the cell.

If using the support pillars, I find it is easier to insert a pillar into the vertex before installing it.