# QCW_half_bridge_PCB
Half bridge PCB for TO-247 IGBTs, intended for DRSSTC or general use, includes optional PCB mounted CT

Design notes:
- Intended for use with "QCW_MMC_PCB" and "GDT_PCB" located in my other repositories
- Have included a lot of different holes for various mounting requirements. Hole placement is intended to allow connection to the MMC PCB via brass standoff.
- Two solder locations are provided for connecting via the CT (with jumper wire through the middle of CT). This is for flexibility when stacking 2 PCBs - can pass a connection through using a standoff through the unusued hole.
- Electrolytic cap footprints provided for 3x 25mm dia. capaciors or 2x 35mm. These are only relevant when not using a buck modulator to control bus voltage.
- Footprints provided for various different DC bus capactiors - up to 8x high voltage ceramic, up to 2x 27.5mm leg spacing film, 2x 15/22.5mm leg spacing film 
- Various Fischer Elektronik SK 481 heatsinks can be used (with clips to hold IGBTs), either 2 separate heatsinks (suggest 37.5mm length) to avoid isolation requirements, or larger 50-84mm with isolation pads behind IGBTs. In all cases use an insulated washer for heatsink mounting screw, and consider adding kapton tape or similar to top layer to add isolation between heatsink and top layer tracks.
- Option to use 2 IGBTs in parallel for each position - if this is done then care should be taken chosing gate drive sharing resistors or suitable ferrite beads to try and match switching characteristics as closely as possible (footprints provided).
- Clearance/Creepage distances (~1mm, occasionally slightly less) are marginal for running at 400-600V. Would suggest taking care with flux residue etc, and use at own risk.

Changes intended for future revisions:
- Increase clearance as possible
- Strengthen holes around IGBT gate legs with reinforcing vias

Output notes:
- 3 different "PCB Variants" have been defined and output files generated as examples:
  - Single IGBT in each of upper and lower half bridge position, no CT, 2x 37.5mm SK481 heatsinks, no electrolytic caps
  - Single IGBTs in each of upper and lower half bridge position, CT mounted, 2x 37.5mm SK481 heatsinks, 2x 35mm dia. electrolytic caps fitted
  - Dual IGBTs in each of upper and lower half bridge position, CT mounted, 2x 37.5mm SK481 heatsinks, 3x 25mm dia. electrolytic caps fitted
- The "schematic" PDFs are located under "Reference outputs" and include a 3D model for viewing in compatible software (Adobe reader works, Foxit does not, unsure about others)
- BoM outputs have been provided but are of low quality, as I did not spend time fixing up the component parameters. The schematic should give whatever information is misssing.
