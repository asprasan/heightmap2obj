# heightmap2obj
A small and simple C++ CLI tool that converts greyscale heightmaps to 3D OBJ models. Uses [lodepng](https://github.com/lvandeve/lodepng) and [obj](https://github.com/rlk/obj).

## Usage
`./hmap2obj <pngpath> <width> <height> <objpath> <extentX> <extentZ> <maxY>`

* pngpath - Absolute path to the input png file.
* width   - Width of the input png file in pixels.
* height  -	Height of the input png file in pixels.
* objpath -	Absolute path to the output obj file.
* extentX - Resulting model extent on the X-axis.
* extentZ -	Resulting model extent on the Z-axis.
* maxY    -	White pixels will be mapped to this Y value. All other pixels will be mapped to a value between [0; maxY] according to their greyscale value. A black pixel will always map to Y = 0.

## Adding Cmake files for easier usage
Cmake files have been added to compile and use this library
### Usage instructions
```sh
mkdir build
cd build
cmake ..
make
```

A shell script file `run.sh` has also been included with a sample code. To use it:
```sh
sh run.sh 
```

The `run.sh` file looks like this:
```sh
./build/hmap2obj/hmap2obj \
./example_screenshots/input.png \
1081 \
1081 \
./output.obj \
2 \
2 \
10
```

Further you can use an [online viewer](https://3dviewer.net/) to view the generated obj file.


## Example
### Input PNG
![Height map of the Grand Canyon](https://raw.githubusercontent.com/emberflare/heightmap2obj/master/example_screenshots/input.png)
### Output OBJ (opened in Blender)
![3D model of the Grand Canyon](https://raw.githubusercontent.com/emberflare/heightmap2obj/master/example_screenshots/output.png)
