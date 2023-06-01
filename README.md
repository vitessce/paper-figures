# vitessce-figures

## Setup

Create a conda environment

```sh
conda env create -f environment.yml
```

Install Globus Connect Personal - see comments in `./codex/Snakefile` for more details


## Run

Activate the conda environment

```sh
conda activate vitessce-figures-env
```

```sh
# Vignette 01
cd osmfish
snakemake -j 1
cd ..
jupyter lab
# Run all cells of osmfish/src/osmfish.ipynb

# Vignette 02
cd visium
snakemake -j 1
cd ..
jupyter lab
# Run all cells of visium/src/visium.ipynb

# Vignette 03
cd ims/data
curl -L -o VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.AREA.ome.tiff "https://vitessce-demo-data.storage.googleapis.com/test-data/VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.AREA.ome.tiff"
curl -L -o VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.GAUSSIAN.ome.tiff "https://vitessce-demo-data.storage.googleapis.com/test-data/VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.GAUSSIAN.ome.tiff"
curl -L -o VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.LINEAR.ome.tiff "https://vitessce-demo-data.storage.googleapis.com/test-data/VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.LINEAR.ome.tiff"
curl -L -o VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.SIMPLE.ome.tiff "https://vitessce-demo-data.storage.googleapis.com/test-data/VAN0006-LK-2-85-IMS_PosMode_multilayer.pyramid.SIMPLE.ome.tiff"
cd ../..
jupyter lab
# Run all cells of ims/src/ims.ipynb

# Vignette 04
cd codex
snakemake -j 1
cd ..
jupyter lab
# Run all cells of codex/src/codex.ipynb

# Vignette 05
cd cite-seq
snakemake -j 1
cd ..
jupyter lab
# Run all cells of cite-seq/src/cite-seq.ipynb

# Vignette 06
cd multiome
jupyter lab
# Run all cells of multiome/src/multiome.ipynb

```

