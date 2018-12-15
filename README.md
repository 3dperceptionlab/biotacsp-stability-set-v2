# BioTacSp Stability Set (BTS3) V2

This dataset is an extended version of the previously introduced [BioTacSp Images](https://github.com/yayaneath/biotac-sp-images) by Zapata-Impata et. al.


The aforementioned [BioTacSp Images](#) contains grasp samples performed over 41 objects with different geometries (i.e. cylinders, spheres, boxes), materials (i.e. wood, plastic, aluminum), stiffness levels (i.e. solid, soft) as well as sizes and weights. This extended version adds a test set of 10 new objects with similar materials but different geometries and stiffness levels. The original 41 were left for the training and validation purposes. Here we show a group photo of both sets.

<p align="center">
  <img src="http://www.fillmurray.com/460/300">
</p>

Both sets, training and test, were recorded following these steps:

1) Grasp the test object: the hand performed a three-fingered grasp that contacted the object with each of the fingers equipped with a tactile sensor.
2) Read the sensors: a single reading was recorded then from each of the sensors at the same time.
3) Lift the object: the hand was raised in order to lift the object and check the outcome.
4) Label the trial: the previously recorded tactile readings were labeled according to the outcome of the lifting with two classes (stable, i.e., it is completely static, or slip, i.e., either fell from the hand or it moves within it).

We have performed grasps using a Shadow Dexterous hand equipped with three BioTac SP tactile sensors in its index finger (ff), middle finger (mf) and thumb (th). The dataset stores 24 values for each of the tactile sensors, the grasped object and whether the object slipped or not from the hand. There are two hand configurations in the original dataset: palm down grasps were performed pointing the palm of the hand downwards while palm side grasps were recorded pointing it to one side, with the thumb upwards. In this work, we have added a new configuration: palm 45 which is in between the other two configurations at an angle of 45 degrees. Pictures below show examples for each orientation.

The dataset is split into six files, three for the training set and three for the test set with one individual file for each orientation. Here is the list of the provided CSV files.

- bts3v2_palm_down.csv (Training set for the palm down orientation)
- bts3v2_palm_side.csv (Training set for the palm side orientation)
- **NEW** bts3v2_palm_45.csv (Training set for the palm 45 orientation)
- **NEW** bts3v2_palm_down_test.csv (Test set for the palm down orientation)
- **NEW** bts3v2_palm_side_test.csv (Test set for the palm side orientation)
- **NEW** bts3v2_palm_45_test.csv (Test set for the palm 45 orientation)

See the next table for a summary of the whole dataset and its splits:

|               | Training Set |          | Test Set |          |
|---------------|--------------|----------|----------|----------|
| **Configuration** | **Stable**       | **Slippery** | **Stable**   | **Slippery** |
| Palm Down     | 667          | 609      | 153      | 163      |
| Palm Side     | 603          | 670      | 157      | 165      |
| Palm 45       | 1058         | 1075     | 250      | 261      |
| *All*           | *2328*         | *2354*     | *560*      | *589*      |

## Citation

If you use this dataset, please cite:

```
@article{BTS3V2_2018,
  author    = {Alberto Garcia{-}Garcia and
               Brayan S. Zapata{-}Impata and
               Sergio Orts{-}Escolano and
               Jose Garcia Rodriguez and
               Pablo Gil},
  title     = {TactileGCN},
  journal   = {CoRR},
  volume    = {XXXX},
  year      = {2018},
  url       = {http://arxiv.org/abs/XXXXXX},
  archivePrefix = {arXiv},
  eprint    = {1810.06936},
}

```
