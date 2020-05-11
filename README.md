# SSRLCV Sample Data

The sample data here is a part of a dataset that was used in Caleb Adams' Thesis, [High Performance Computation with Small Satellites and Small Satellite Swarms for 3D Reconstruction](http://piepieninja.github.io/research-papers/thesis.pdf). The datasets here are used to test the SSRLCV software library, the SSRLCV is maintained at [the SSRLCV gitlab page](https://gitlab.smallsat.uga.edu/payload_software/SSRLCV) and [mirrored on github](https://github.com/uga-ssrl/SSRLCV). Additional test data is generated with the aid of the utility scripts in the [SSRLCV-Utilities gitlab repo](https://gitlab.smallsat.uga.edu/payload_software/ssrlcv-utilities), mirrored on githuib as [SSRLCV-Util](https://github.com/uga-ssrl/SSRLCV-Util). If you use these test sets in future research, or the methods described below to generate more test data, please cite my thesis:

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

Some existing sample data is located within this repository, but this does not include all of the availible test data. The included data is as follows:


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
* `seeds`: various seed images used for feature matching threasholds in SSRLCV

## Tests used in my Thesis

These tests are by far the **most comprihensive** and **most useful** SSRLCV tests done thus far (May 2020). The [datasets used in my thesis](http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis/) are freely availible online and [compressed in a traball here](http://104.236.14.11/CalebAdams-Tests-Used-In-Thesis.tar.gz). These tests include ground truth models for comparison, the output model produced by the test, an `ssrlcv.log` file with states and power usage over the pipeline, and the output of VSFM for comparison.

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

The optical properties of the camera used to generate the simulated images are derived from Blender's Pinhole caemra model. This model is limited and some issue occur with the feild of view and the focal length. Because the two of these are tied together in Blender's camera model, the FOC is chosen to be correct while the FOV is incorrect so that the resultant GSD of the system is as accurate as possible.

#### Correcting for erronious Feild of View


## Generating New Sample Data

To generate new sample data you must you must have a Blender install that is capible of using the [BlenderGIS addon](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage). Follow the [BlenderGIS Install and Usage](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage) instructions before continuing.

Then, follow the instructions on the [BlenderGIS quickstart guide](https://github.com/domlysz/BlenderGIS/wiki/Quick-start) to gererate a 3D model of a given area on earth from [Shuttle Radar Topography Mission (STRM)](https://www2.jpl.nasa.gov/srtm/) data. Find the area you desire to generate a 3D reconstruction of

The following steps can be used to generate semi-realistic imagery:

1. Add a light source with `Add > Light > Sun`. Then, under **Object Properties** set the `z` location to `500000` m
2. Add the Camera with `Add > Camera`, you can set the `z` location to `400000` m (`400` km) under **Object Properties** to start.
3. Under the **Object Data Properties** of the camera select a focal length of `270` mm, this is the effective focal of the RUDA camera systems as of May 2020. **Always** use the effective focal length and not the measured distance. The feild of view will be automatically adjusted to ~ `7.63` degree. This is unavoidable due to blender constraints. See the section above on *Test Data Optical Properties* and *Correcting Erronious Feild of View* for a discription of needed future work.
4. Under the same **Object Data Properties** of the camera, change the render ending distance (called the clip distance) End to `500000` m.
5. Under **Scene** change the the `X` and `Y` render resolutions of `4096` for a realistic case or `1024` for a simple test case
6. Remove the glossiness of the mesh by turning `Specular` to `0.0` under the **Material Properties** of the exported `EXPORT_GOOGLE_SAT_WM` mesh object.

After those steps above you should save your blender file. Now you will 










<!--  -->
