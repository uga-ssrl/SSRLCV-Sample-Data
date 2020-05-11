# SSRLCV Sample Data

The sample data here is a part of a dataset that was used in Caleb Adams' Thesis, [High Performance Computation with Small Satellites and Small Satellite Swarms for 3D Reconstruction](http://piepieninja.github.io/research-papers/thesis.pdf). The datasets here are used to test the SSRLCV software library, the SSRLCV is maintained at [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV). Additional test data is generated with the aid of the utility scripts in the [SSRLCV-Utilities gitlab repo](https://gitlab.smallsat.uga.edu/payload_software/ssrlcv-utilities), mirrored on github as [SSRLCV-Util](https://github.com/uga-ssrl/SSRLCV-Util). If you use these test sets in future research, or the methods described below to generate more test data, please cite my thesis:

```
@mastersthesis{CalebAdamsMSThesis,
  author={Caleb Ashmore Adams},
  title={High Performance Computation with Small Satellites and Small Satellite Swarms for 3D Reconstruction},
  school={The University of Georgia},
  url={http://piepieninja.github.io/research-papers/thesis.pdf},
  year=2020,
  month=may
}
```

## Included Sample Data

Some existing sample data is located within this repository, but this does not include all of the available test data. The included data is as follows:


* `everest1024`: These test sets contain simulated 1024 x 1024 images of everest
  * `everest1024/2view`: A 2-view reconstruction of everest at 400km. Each Image is 10 degrees off nadir. One image is directly nadir.
    * `1.png`: Nadir facing image
    * `2.png`: 10 degrees off nadir image
    * `params.csv`: ASCII encoded camera parameters. These parameters are defined on [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV).
  * `everest1024/3view`:
    * `1.png`: Nadir facing image
    * `2.png`: 10 degrees off nadir image
    * `3.png`: -10 degrees off nadir image
    * `params.csv`: ASCII encoded camera parameters. These parameters are defined on [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV).
  * `everest1024/5view`:
    * `1.png`: Nadir facing image
    * `2.png`: 10 degrees off nadir image
    * `3.png`: -10 degrees off nadir image
    * `4.png`: 20 degrees off nadir image
    * `5.png`: -20 degrees off nadir image
    * `params.csv`: ASCII encoded camera parameters. These parameters are defined on [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV).
* `everest4096`: A test set containing simulated 4096 x 4096 imagery of everest
  * `everest4096/2view`: 4096 x 4096 MOCI-like resolution images simulated at 400km.
    * `1.png`: Nadir facing image
    * `2.png`: 10 degrees off nadir image
    * `params.csv`: ASCII encoded camera parameters. These parameters are defined on [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV).
* `seeds`: various seed images used for feature matching thresholds in SSRLCV

## Tests used in my Thesis

These tests are by far the **most comprehensive** and **most useful** SSRLCV tests done thus far (May 2020). The [datasets used in my thesis](http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis/) are freely available online and [compressed in a traball here](http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis.tar.gz). These tests include ground truth models for comparison, the output model produced by the test, an `ssrlcv.log` file with states and power usage over the pipeline, and the output of VSFM for comparison.

#### Downloading Additional Data

To download these datasets use `wget` or `curl` on your favorite unix-like machine or [download from the link directly](http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis.tar.gz):

```
wget http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis.tar.gz
```

or

```
curl -O http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis.tar.gz
```

#### Additional Data

The tests used in my thesis include the following additional data:

A set of [Mount Rainier](https://en.wikipedia.org/wiki/Mount_Rainier) test sets is provided with incremental image offsets of 5 degrees off nadir:

  * `rainier1024-2view`
    * `1.png` nadir facing image
    * `2.png` 5 degree off nadir image
    * `results` a folder containing prior results of a 3D reconstruction
    * `vsfm` a folder containing reconstruction results from the [VSFM](http://ccwu.me/vsfm/) software package
  * `rainier1024-3view`
    * `1.png` nadir facing image
    * `2.png` 5 degree off nadir image
    * `3.png` -5 degree off nadir image
    * `results` a folder containing prior results of a 3D reconstruction
    * `vsfm` a folder containing reconstruction results from the [VSFM](http://ccwu.me/vsfm/) software package
  * `rainier1024-5view`
    * `1.png` nadir facing image
    * `2.png` 5 degree off nadir image
    * `3.png` -5 degree off nadir image
    * `4.png` 10 degree off nadir image
    * `5.png` -10 degree off nadir image
    * `results` a folder containing prior results of a 3D reconstruction
    * `vsfm` a folder containing reconstruction results from the [VSFM](http://ccwu.me/vsfm/) software package
  * `rainier4096-2view`
    * `1.png` nadir facing image
    * `2.png` 5 degree off nadir image
    * `results` a folder containing prior results of a 3D reconstruction
    * `vsfm` a folder containing reconstruction results from the [VSFM](http://ccwu.me/vsfm/) software package
  * `rainier4096-3view`
    * `1.png` nadir facing image
    * `2.png` 5 degree off nadir image
    * `3.png` -5 degree off nadir image
    * `results` a folder containing prior results of a 3D reconstruction
    * `vsfm` a folder containing reconstruction results from the [VSFM](http://ccwu.me/vsfm/) software package

The everest datasets included here also have `results` and `vsfm` folders provided.

The ground truth models, raw blender files, and STRM data are provided as follows:

  * `rainier-blender`
    * `Rainier.blend` the blender file used to simulate the imagery
    * `Rainier_ground_truth.ply` the PLY file used as a ground truth measurement
    * `srtm.tif` the associated STRM terrain data
  * `everest-blender`
    * `Everest.blend` the blender file used to simulate the imagery
    * `Everest_ground_truth.ply` the PLY file used as a ground truth measurement
    * `srtm.tif` the associated STRM terrain data

#### Test Data Optical Properties

The optical properties of the camera used to generate the simulated images are derived from Blender's Pinhole camera model. This model is limited and some issues occur with the field of view and the focal length. Because the two of these are tied together in Blender's camera model, the FOC is chosen to be correct while the FOV is incorrect so that the resultant GSD of the system is as accurate as possible.

#### Correcting for Erroneous Field of View

The issue is that, when choosing a given focal length `foc`, an erroneous field of view `fov_e` is generated. Due to the way Blender camera modeling works, this `fov_e` is always larger than reality. The general idea is to caclulate the needed pixel density to crop the image later and generate the correct `fov`.

Let's say that the desired resolution of our image is `res`. The blender camera model will produce an erronous `foc_e` that generates an image with a resolution of `pix`. We seek to caclulate the value of `pix` so that we can generate an image at that resolution and crop it to our desired `res`.

using the tangent we can use the two following equations to find the desired `pix` value for rendering:

```
tan(fov_e) = pix / ( 2 * f )
```

and

```
tan(fov) = res / ( 2 * f )
```

Substitution results in (I multiply by 2 to get the full length):

```
pix = ( res * tan(fov_e) ) / ( 2 * tan(fov) )
```

Just plug in the desired final `res`, the erronously generated feild of view `fov_e`, and the true feild of view `fov` to get the render value `pix`. round `pix` to the nearest integer. The resultant images sjpi;d ne cropped from the center down to the `res` value. This keeps the GSD, field of view, and focal length of the desired optic.

## Generating New Sample Data

To generate new sample data you must have a Blender install that is capable of using the [BlenderGIS addon](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage). Follow the [BlenderGIS Install and Usage](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage) instructions before continuing.

Then, follow the instructions on the [BlenderGIS quickstart guide](https://github.com/domlysz/BlenderGIS/wiki/Quick-start) to generate a 3D model of a given area on earth from [Shuttle Radar Topography Mission (STRM)](https://www2.jpl.nasa.gov/srtm/) data.

#### BlenderGIS setup

The following steps can be used to generate semi-realistic imagery:

1. Add a light source with `Add > Light > Sun`. Then, under **Object Properties** set the `z` location to `500000` m
2. Add the Camera with `Add > Camera`, you can set the `z` location to `400000` m (`400` km) under **Object Properties** to start.
3. Under the **Object Data Properties** of the camera select a focal length of `270` mm, this is the effective focal of the RUDA camera systems as of May 2020. **Always** use the effective focal length and not the measured distance. The field of view will be automatically adjusted to ~ `7.63` degree. This is unavoidable due to blender constraints. See the section above on *Test Data Optical Properties* and *Correcting Erroneous Field of View* for a description of needed future work.
4. Under the same **Object Data Properties** of the camera, change the render ending distance (called the clip distance) End to `500000` m.
5. Under **Scene** change the the `X` and `Y` render resolutions of `4096` for a realistic case or `1024` for a simple test case. For the adjusted case, where the image is cropped post rendering, set the resolution to the value of `pix` cacluated in the *Correcting for Erroneous Field of View* section.
6. Remove the glossiness of the mesh by turning `Specular` to `0.0` under the **Material Properties** of the exported `EXPORT_GOOGLE_SAT_WM` mesh object.

#### Satellite Orientation, Position, and Slew

After those steps above you should save your blender file. Now you will now generate the orbital position and orientation data for the renderings. I have provided a script in the [SSRLCV-Utilities gitlab repo](https://gitlab.smallsat.uga.edu/payload_software/ssrlcv-utilities), which is [mirrored on github](https://github.com/uga-ssrl/SSRLCV), that contains a script to do this automatically for you. The details of this are covered in my thesis in the [SSRLCV Simulations with Blender section under the Experements and Results chapter](http://piepieninja.github.io/research-papers/thesis.pdf); it basically boils down to solving a quadratic.

The `track_orbit_camera_gen.py` script contained in the [SSRLCV-Utilities gitlab repo](https://gitlab.smallsat.uga.edu/payload_software/ssrlcv-utilities), which is [mirrored on github](https://github.com/uga-ssrl/SSRLCV), will generate 7 images with off-nadir angles of 3 degrees each with the following example:

```
python3 io/track_orbit_camera_gen.py 400 3 7
```

The program will output slew information, camera parameter information, and blender rendering information. Example slew information is of the form:

```
-----------------------------------------------------------
  orbit angle (rad): 0.003092571033663451
  input angle (rad): 0.05235987755982989
  orbit arclen (km): 20.96144646617087
   grnd arclen (km): 19.72441805270549
    velocity (km/s): 7.66863623504974
      slew time (s): 2.733399502034785
Tracking Slews:
    slew rate (rad/s): 0.019155589046113596
    slew rate (deg/s): 1.0975344064293395
Nadir Slews:
    slew rate (rad/s): 0.0011314010379241282
    slew rate (deg/s): 0.06482450440977335
-----------------------------------------------------------
```

Camera parameters are printed off next and should be copied into a `params.csv` file. The `params.csv` file should be placed into an empty folder titled `example-data` or some other name. The output of the program at this stage is of the form:

```
     ---- Copy to params.csv ----
1.png,0.0,0.0,400000.0,0.0,0.0,0.0,
2.png,20.96141305365656,0.0,399.9675876447502,0.0,0.05235987755982996,0.0,
3.png,-20.96141305365656,0.0,399.9675876447502,0.0,-0.05235987755982996,0.0,
4.png,42.02799884713057,0.0,399.86969831324694,0.0,0.1047197551196597,0.0,
5.png,-42.02799884713057,0.0,399.86969831324694,0.0,-0.1047197551196597,0.0,
6.png,63.30694946788028,0.0,399.7043480922854,0.0,0.15707963267948966,0.0,
7.png,-63.30694946788028,0.0,399.7043480922854,0.0,-0.15707963267948966,0.0,
```

Lastly, the blender parameters are generated. These parameters should be manually copied into blender and are output in the form:

```
     ----   Copy to Blender  ----
0.0,0.0,0.0, y rotate: 0.0
20961.41305365656,0.0,399967.5876447502, y rotate: 3.0 deg
-20961.41305365656,0.0,399967.5876447502, y rotate: -3.0 deg
42027.99884713057,0.0,399869.69831324695, y rotate: 6.0 deg
-42027.99884713057,0.0,399869.69831324695, y rotate: -6.0 deg
63306.94946788028,0.0,399704.3480922854, y rotate: 9.0 deg
-63306.94946788028,0.0,399704.3480922854, y rotate: -9.0 deg
```

The values above are generated in the form `X,Y,Z, Y rotation`. The first should have a `z` altitude of your desired orbit and all `0` elements for each other item. The following steps should be taken for each image exluding the first:

1. Under the Camera's **Object Properties** set the `X` value to the generated value
2. Under the Camera's **Object Properties** set the `Y` value to `0.0`
3. Under the Camera's **Object Properties** set the `Z` value to the generated value
4. Under the Camera's **Object Properties** set the `Y rotation` value to the generated value
5. Select `Render > Render Image`
6. Select `Image > Save As`. Save the image in the same folder as the `params.csv` file and name the image `#.png` where `#` is an integer matching the values in the `params.csv`. Each time you save an image you should increase the integer `#`.
7. If using the adjusted value of `pix` (described in the *Correcting for Erroneous Field of View* section), crop the image back down to the correct resolution `res`

#### Scripting Sample Data Generation

With the steps and tools provided, scripting data generation is possible. This should be considered future work


<!--  -->
