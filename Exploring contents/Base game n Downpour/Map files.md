Map image
consists of 3 layers with same size.

### Map_xx.txt
Starts with region name: 
*Identifies position of said room.*
- `x, y` positions of room in canon view (region map image rendering is based on it) of map tab in Dev Tools
- `x, y`  positions of room in dev view of map tab in Dev Tools
- number of layer, 0-2
- subregion name

Starting with `Connection:` line
*Determines a connection between 2 rooms.*
- name of 1st room
- name of 2nd room 
- `x, y` positions of 1nd room
- `x, y` positions of 2nd room
- direction of 1st room
- direction of 2nd room