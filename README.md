# NavMeshSurface2DBaker
About
---
NavMeshSurface2DBaker is a Unity Package that provides functionality to bake 2D colliders into NavMeshSurfaces, which are part of the [Unity NavMeshComponents](https://github.com/Unity-Technologies/NavMeshComponents) .

Usage
---
1. Put Surface2DBaker script on same GameObject as your NavMeshSurface.
2. Add all components that contain 2D colliders you want to bake to "Objects Containing Obstacles". It is enough to add the root object, the script will automatically also search for colliders in children
3. Set the NavMesh agent selected in your NavMesh surface to an appropriate size and check if all the baking settings on the Surface2DBaker component are as you want them. Check the tooltip if it's not clear what a setting does.
4. Press the "Bake 2D" button. Your NavMesh will now be generated

FAQ
---
### What collider types are being supported?
* BoxCollider2D
* CircleCollider2D
* PolygonCollider2D
* CompositeCollider2D
* TilemapCollider2D (For those to work, you have to make them part of a CompositeCollider2D, though!)

### Why didn't you implement a new NavMeshSurface script? Why do we have to use 2 components?
While the NavMeshSurface script and its editor counterpart are open source, they contain a lot of code and they have been changed many times in the past. If I modified this code, I would have to update my project every time Unity changes any of those components.
By writing my own component and only using public methods of the NavMeshComponents project, I hope to keep a high level of compatibility with future versions and the need for changes on my side to a minimum.

Compatibility
---
Current version tested with:
* Unity 2018.3.0f2
* Unity NavMeshComponents 2018.3.0f2

3rd party components provided with project
---
* [Unity NavMeshComponents](https://github.com/Unity-Technologies/NavMeshComponents) (MIT license, for full license details see subfolder *NavMeshComponents*
