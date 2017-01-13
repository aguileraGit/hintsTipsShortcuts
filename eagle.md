## Eagle

### Before ordering
* Run ERC
* ~~Run DRC with /eagle/dru/4pcb.dru~~ Needs to be updated!
* Run tools - Statistics. Check for unrouted wires
* Upload to [freeDRM](https://www.freedfm.com)
* Request checkplot from AC
* Check each layer (copper, soldermask, etc)
* Check copper pours

### Display all unrouted nets
`display none unrouted`

### Rip up only polygons
`rip @;`

### Combine GND and AGND
* Use shorts-old.lbr

### CAM file types
* cmp - Top copper
* sol - Bottom copper
* gbo - Bottom silk screen
* plc - Top silk screen
* stc - Top solder mask
* sts - Bottom solder mask
* drd - Drill file

### Board versioning
http://semver.org/

### Change Font
* [Change all font ratio](https://www.element14.com/community/thread/18176/l/how-do-i-change-all-fonts-to-vector-on-the-same-pcb-at-once?displayFullThread=true)
* change size 0.8 (>0 0)

### Advanced Circuits PCB Specs
* http://www.4pcb.com/pcb-design-specifications/

### User (Diego) created Short cuts
* `Ctrl + R` - Route
* `Ctrl + Shift + R` - Rip
* `Ctrl + M` - Move
* `Ctrl + V` - Via
* `Ctrl + W` - Show
* `Ctrl + L` - Ratsnet
* `Shift + Ctrl + L` - rip @;
* `Ctrl + D` - Delete
* `Ctrl + A` - Split
