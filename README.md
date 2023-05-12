# How to clone this project?

```
$ git clone git@github.com:eYs3D/eys3d_unity_release.git --recurse-submodules
```

# How to import eYs3D Unity wrapper?

- Plug in eYs3D module to computer
- Open Unity Editor 2019
- Import eYs3D_UnitySDK.unitypackage to the current project assets
- Open Color_Depth scene demonstrates image stream from eYs3D modules, and PointCloud scene shows point cloud demo.

![Screenshot from 2021-06-16 03-32-08](https://user-images.githubusercontent.com/70574111/122177319-7e35e200-ce53-11eb-9d3c-b95a344661a2.png)

![Screenshot from 2021-06-16 03-33-39](https://user-images.githubusercontent.com/70574111/122177522-b50bf800-ce53-11eb-9cd0-40f6efda358d.png)

- Copy the eYs3D folder to your project root. If developer did not download the submodule in that folder.
- Please re-run the following command, and copy the eYs3D folder to your project root. The folder structure would be similar to the following image.
```
$ git submodule update --init --recursive
```

![unity-helper](https://github.com/eYs3D/eys3d_unity_release/assets/70574111/0997e645-ac6b-418d-bf9a-f4442196e1cc)


# Overview of eYs3D Unity wrapper

![UnityBlockDiagram](https://user-images.githubusercontent.com/70574111/122187338-f228b800-ce5c-11eb-9f97-bd1959db4106.png)

# Import this project using Unity Editor 2019

[https://unity3d.com/get-unity/download](https://unity3d.com/get-unity/download)

# Integrated development environment JetBrian Rider

[https://www.jetbrains.com/rider/](https://www.jetbrains.com/rider/)

Build Script:
build.bat
or
build.bat [path to Unity.exe]

Run Script:
run_color_depth.bat
run_point_cloud.bat

Unity WIN32 Command Line Build:
1. Use DLL: Assets\Plugins: eSPDI_DM.dll, turbojpeg.dll, eys3d.dll (confirm created by build_unity.bat)
2. Use build.bat: modify UNITY_PATH  
ex: build.bat "C:\Program Files\Unity\Hub\Editor\2019.4.25f1\Editor\Unity.exe"  
3. Select Scene:  
      -executeMethod BuildScript.Color_Depth (for Color_Depth.unity)  
      -executeMethod BuildScript.PointCloud (for PointCloud.unity)  
4. Run: cd Release
        Color_Depth.exe
        PointCloud.exe

Unity Editor WIN32 Settings:
1. Select Scene Icon-> Color_Depth
2. Scene Resolution->Standalone (1024x768)
3. Build Settings->Player Settings->Other Settings->Configuration->Script Define Symbols: add WIN32
4. DLL: Assets\Plugins: eSPDI_DM.dll, turbojpeg.dll, eys3d.dll
