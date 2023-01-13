# das-fiberoptic

## Configuration

1. Create the conda environment using the `environment.yml` file provided and activate it:

   ```{bash}
   > conda env create -f environemt.yml
   > conda activate das-fiberoptic

   ```

2. Configure module discovery using the `setup.py` file (this will help us find modules written in sub-diretories):

   ```{bash}
   pip install -e .
   ```
