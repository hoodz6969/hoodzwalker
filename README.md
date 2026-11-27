# HoodzWalker

3D modelling for GTA V and FiveM, by Hoodrat Productions. Version 1.9.0.

Unzip the folder, run `hoodzwalker.exe`, and point the app at your own GTA V install. Nothing else has to be installed. This package does not include the game.

A short French start guide is in `LISEZ-MOI.txt`.

## Start

1. Unzip the folder somewhere other than Program Files.
2. Run `hoodzwalker.exe`.
3. Open **GTA > Game files browser (GTA V)...** and choose the folder that contains `GTA5.exe` or `GTA5_Enhanced.exe`.
4. The first load reads the game keys. That step is slow once.

You need Windows 10 or 11, 64-bit, and a graphics card with DirectX 11.

Scenes save as `.mmx` files (**File > Save**, Ctrl+S). Older Polymorph and MoloMax scene files still open.

## The window

- **MODEL** and **MAP** are the two modes at the top. MODEL is for props and interiors you build. MAP is the real GTA V map.
- The left side is the scene list. The right side is the object: transform, modifiers, material, and GTA settings. Extra panels are behind the **···** button.
- **More** on the toolbar holds view options, paint, sculpt, and the wall-opening tool.
- **GTA** opens the export, MLO, collision, and checks panel (F10).
- **Search** finds any command by name.

**Edit > Look** switches Standard (one big view) and Classic (four views).

## Look around

In Standard:

- Middle mouse: orbit
- Shift + middle mouse: pan
- Ctrl + middle mouse: zoom
- Hold the right mouse button and move: fly. WASD moves while you fly.

The cube in the corner of the view snaps the camera to a side. The sun slider on the toolbar sets the time of day.

## Select and move

Click an object to select it. **Select**, **Move**, **Rotate**, and **Scale** are on the top bar.

The move handle has three parts:

- The **arrows** move on one axis. Red is X, green is Y, blue is Z. Each arrow has a dark edge so it stays visible on the grid.
- The **squares** between the arrows move on that plane (ground, or a side wall).
- The **white square in the centre** moves the object with the screen, including up and down.

With an object selected, **X Y Z** are on their own row at the bottom of the window. Drag a number or type one. **World / Local** next to the tools chooses the axes.

**Ctrl+Z** undoes. **Ctrl+C**, **Ctrl+X**, and **Ctrl+V** copy, cut, and paste objects.

## Make a prop

1. **Create** adds a box, a door, stairs, a light, or a line. New objects appear at the 3D cursor.
2. Move, rotate, and scale it.
3. The right panel edits the mesh (modifiers such as Edit Poly and Unwrap UVW), the material, and the GTA type.
4. **GTA > Checks** looks for problems that would break in game. **Fix all** corrects what it can.
5. **GTA > Export FiveM resource...** writes a resource (`fxmanifest.lua` plus `stream`) into the folder you pick.

**File > Import model** reads GLB, glTF, and OBJ. **File > Export models** writes `.ydr` and `.yft`.

## Make an MLO

Two ways to start an interior.

**Draw the rooms.** **GTA > MLO Room Builder (floor plan)...** Draw the plan. The rooms, portals, and door frames are built in 3D. Leave a small gap between rooms and cut a doorway in both walls. HoodzWalker finds the portals from those openings.

**Start from a GTA building and cut the doors.**

1. Switch to **MAP** and click the building so it is selected.
2. Press **Cut a door or window in this building**. The same command is on the right-click menu, under **More > Wall opening**, and in the GTA panel.
3. HoodzWalker copies that building. The original in the game files is not changed.
4. Drag on a wall.
   - **D** makes a door down to the floor.
   - **W** makes a window.
   - **R** rectangle, **A** arch, **G** gothic, **C** round.
5. Pull the sides, then press **Enter**. The hole stays in the Modifiers tab, so you can edit it or remove it later.

Then add the interior rooms, run **Checks**, and export.

## Edit the map

1. Open **MAP**. The map is shown as distant models.
2. Click an area. Its `.ymap` files load so you can edit them.
3. Move or delete objects, or drop props from **Place props** on the map panel.
4. **Edit this interior** brings an existing MLO's rooms into the scene.
5. **SAVE MAP RESOURCE** writes the FiveM resource. Put that folder in your server's `resources` and add `ensure` plus the resource name.
6. If you were already on the server, reconnect to see new models.

What you model on the map (new objects, a copied building, rooms) is saved with the map as new models. The game's original files stay on your PC.

## Paint, vehicles, weapons, peds

- **GTA > Hoodz Paint** paints textures on the model: layers, brushes, and export to DDS, PNG, or TGA.
- **GTA > Hoodz Materials** is the GTA texture library.
- The GTA panel also has Vehicle Forge, Weapon Forge, and Ped Forge: a game vehicle, weapon, or ped lends its skeleton and HoodzWalker fits your model and writes the files.

## Put it on a server

The export folder is a normal FiveM resource. Copy it into `resources`, add `ensure your_resource_name` to the server config, and restart or reconnect.

## If something looks wrong

- The building is still loading: wait until the model appears, then cut the door again.
- A move arrow is hard to see: use the white centre square, or the X Y Z numbers at the bottom.
- Export fails the checks: open **GTA > Checks** and use **Fix all**, then export again.
- The app asks for .NET: you are running a developer build. The customer zip already contains the runtime. Use `hoodzwalker.exe` from this folder.

Grand Theft Auto V belongs to Rockstar Games. HoodzWalker reads your install and does not ship any game file.
