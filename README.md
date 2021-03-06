Voxelman
========
Voxelman by fengxiaorui

Original project by keijiro: https://github.com/keijiro/Voxelman

Try to modify it to fit the lastest Entities 0.0.12-preview.24

Error Fixed Log
---------------------------------------------
#### Entities package import error: Assembly has reference to non-existent assembly 'Unity.PerformanceTesting'
Manually add it to the manifest.json::"com.unity.test-framework.performance": "0.1.49-preview"

#### error CS0234: The type or namespace name 'Rendering' does not exist in the namespace 'Unity'
Add 'Hybird Renderer package' in the Unity Package Manager, it will automatically generate the dll files

#### error CS0115: 'VoxelBufferSystem.OnCreateManager(int)': no suitable method found to override
Just remove the input params and the error is gone

#### error CS0246: The type or namespace name 'MeshInstanceRenderer' could not be found
Replace all 'MeshInstanceRenderer' with 'RenderMesh' will fix it

#### error CS0246: The type or namespace name 'TransformMatrix' could not be found
Replace 'TransformMatrix' with 'Position' and 'Scale' component

#### several interface update to lastest form
See the git change log for detail infomations


---------------------------------------------

![gif](https://i.imgur.com/NxsT4AK.gif)
![gif](https://i.imgur.com/yrpIhfk.gif)

**Voxelman** is an example that shows how to use the new **[Entity Component
System]** with Unity in an extreme way. Each voxel in the scene is instantiated
as an entity, and controlled by component systems. It also utilizes the **C#
Job System**, the **Burst Compiler** and the **asynchronous raycast** to hit
the maximum efficiency of multi-core processors.

[Entity Component System]: https://github.com/Unity-Technologies/EntityComponentSystemSamples

System requirements
-------------------

- Unity 2018.2 or later

How to play with this project
-----------------------------

### Submodules

This repository uses [Git submodules] to manage UPM (Unity Package Manager)
packages. **If you know Git well and how to deal with submodules,** simply
clone this repository and do `submodule init` & `submodule update` in it.

**If you're not sure what Git submodule is,** download the contents of this
repository from [zip download link]. After extracting the zip file, download
and extract the following packages into the `Packages` directory.

- [jp.keijiro.cmu-mocap](https://github.com/keijiro/CMUMocap/archive/upm.zip)
- [jp.keijiro.klak](https://github.com/keijiro/Klak/archive/upm.zip)
- [jp.keijiro.neolowman](https://github.com/keijiro/NeoLowMan/archive/upm.zip)
- [jp.keijiro.test-assets](https://github.com/keijiro/jp.keijiro.test-assets/archive/master.zip)

[ECS repository]: https://github.com/Unity-Technologies/EntityComponentSystemSamples
[zip download link]: https://github.com/keijiro/Voxelman/archive/master.zip
[Git submodules]: https://git-scm.com/book/en/v2/Git-Tools-Submodules
