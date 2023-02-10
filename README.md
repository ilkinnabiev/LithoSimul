# Neural lithography simulator

## Prerequisites
- Python3
- Nvidia GPU and CUDA
- Pytorch (1.4+) and other dependencies (e.g., torchvision, opencv)
    - For pip users, please type the command `pip install -r requirements.txt`
    - For Conda users, create a new Conda environment using `conda env create -f environment.yml`

## Getting Started

### Lithography Simulation
- **Input:** mask.
- **Output:** aerial image (intensity map).
#### Customize with Your Own Dataset

- Put corresponding items in `./datasets/litho_simul/train/mask` and `./datasets/litho_simul/train/aerial_image` respectively for training, and similarly for testing in `./datasets/litho_simul/test/`
- Before training or testing, you need to change the resolution of the images using the script exDee.py.

  ```shell
  python exDee.py
  ```

#### Train and Test
- Train with the default 256x256 resolution:
  ```shell
  python train.py --phase litho_simul
  ```
- Test the model:
  ```shell
  python test_lithosimul.py --plot
  ```
- The test results will be saved as log files and images. You can find them in `./checkpoints/litho_simul/test_results/`.

# Physical lithography simulator

## Getting Started

- The image for the simulation in `./test/data`.
- The simulation results will be saved in `./output`

- Test the simulation
  ```shell
  python example.py
  ```