# Point·E

![Animation of four 3D point clouds rotating](point_e/examples/paper_banner.gif)

This is the official code and model release for [Point-E: A System for Generating 3D Point Clouds from Complex Prompts](https://arxiv.org/abs/2212.08751).

# Usage


## Build

1. Download repository to local workstation:

```bash
cd $HOME
git clone https://github.com/cardboardcode/point-e.git
cd ~/point-e
```

2. Create a python3 virtual environment:
```bash
cd ~/point-e
virtualenv -p python3 venv
source venv/bin/activate
```

3. Install with `pip install -e .`.

```bash
cd $HOME
pip install -e .
pip install notebook
```


To get started with examples, see the following notebooks:

 * [image2pointcloud.ipynb](point_e/examples/image2pointcloud.ipynb) - sample a point cloud, conditioned on some example synthetic view images.
 * [text2pointcloud.ipynb](point_e/examples/text2pointcloud.ipynb) - use our small, worse quality pure text-to-3D model to produce 3D point clouds directly from text descriptions. This model's capabilities are limited, but it does understand some simple categories and colors.
 * [pointcloud2mesh.ipynb](point_e/examples/pointcloud2mesh.ipynb) - try our SDF regression model for producing meshes from point clouds.

```bash
#image2pointcloud.ipynb
jupyter notebook point_e/examples/image2pointcloud.ipynb
#text2pointcloud.ipynb
jupyter notebook point_e/examples/text2pointcloud.ipynb
#pointcloud2mesh.ipynb
jupyter notebook point_e/examples/pointcloud2mesh.ipynb
```

> Make sure to enable "Trust" in the Jupyter notebook interface.

For our P-FID and P-IS evaluation scripts, see:

 * [evaluate_pfid.py](point_e/evals/scripts/evaluate_pfid.py)
 * [evaluate_pis.py](point_e/evals/scripts/evaluate_pis.py)

For our Blender rendering code, see [blender_script.py](point_e/evals/scripts/blender_script.py)

# Samples

You can download the seed images and point clouds corresponding to the paper banner images [here](https://openaipublic.azureedge.net/main/point-e/banner_pcs.zip).

You can download the seed images used for COCO CLIP R-Precision evaluations [here](https://openaipublic.azureedge.net/main/point-e/coco_images.zip).
