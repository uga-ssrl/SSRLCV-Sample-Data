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

The datasets used in my thesis are found at [link TBD]().

## Included Existing Sample Data

Some existing sample data is located within this repository, but this does not include all of the availible test data. The included data is as follows:


* `everest1024`: These test sets contain simulated 1024 x 1024 images of everest
  * `everest1024/2view`:
  * `everest1024/3view`:
  * `everest1024/5view`:
* `everest4096`: A test set containing simulated 4096 x 4096 imagery of everest
  * `everest4096/2view`:

## Downloading Additional Existing Data



## Generating Sample Data

To generate new sample data you must you must have a Blender install that is capible of using the [BlenderGIS addon](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage). Follow the [BlenderGIS Install and Usage](https://github.com/domlysz/BlenderGIS/wiki/Install-and-usage) instructions before continuing.
