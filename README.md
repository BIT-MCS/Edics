# Edics
This is the code accompanying the paper: "[Energy-Efficient Distributed Mobile Crowd Sensing: A Deep Learning Approach](https://ieeexplore.ieee.org/document/8664596)", published in JSAC.

## :page_facing_up: Description
High-quality data collection is crucial for mobile crowd sensing (MCS) with various applications like smart cities and emergency rescues, where various unmanned mobile terminals (MTs), e.g., driverless cars and unmanned aerial vehicles (UAVs), are equipped with different sensors that aid to collect data. However, they are limited with fixed carrying capacity, and thus, MT's energy resource and sensing range are constrained. It is quite challenging to navigate a group of MTs to move around a target area to maximize their total amount of collected data with the limited energy reserve, while geographical fairness among those point-of-interests (PoIs) should also be maximized. It is even more challenging if fully distributed execution is enforced, where no central control is allowed at the backend. To this end, we propose to leverage emerging deep reinforcement learning (DRL) techniques for directing MT's sensing and movement and to present a novel and highly efficient control algorithm, called energy-efficient distributed MCS (Edics). The proposed neural network integrates convolutional neural network (CNN) for feature extraction and then makes decision under the guidance of multi-agent deep deterministic policy gradient (DDPG) method in a fully distributed manner. We also propose two enhancements into Edics with N-step return and prioritized experienced replay buffer. Finally, we evaluate Edics through extensive simulations and found the appropriate set of hyperparameters in terms of number of CNN hidden layers and neural units for all the fully connected layers. Compared with three commonly used baselines, results have shown its benefits.

## :wrench: Installation
1. Clone repo
    ```bash
    git clone https://github.com/BIT-MCS/Edics.git
    cd Edics
    ```
2. Install dependent packages
    ```sh
    conda create -n mcs python==3.8
    conda activate mcs
    pip install tensorflow-gpu==1.15
    pip install -r requirements.txt
    ```


## :computer: Training

Train our solution
```bash
python experiments/train.py
```
## :checkered_flag: Testing

Test with the trained models 

```sh
python experiments/test.py --load-dir=your_model_path
```

Random test the env

```sh
python experiments/test_random.py
```

## :clap: Reference
- https://github.com/openai/maddpg


## :scroll: Acknowledgement

This paper was financially supported by National Natural
Science Foundation of China (No. 61772072).
<br>
Corresponding author: Chi Harold Liu.

## :e-mail: Contact

If you have any question, please email `3120215520@bit.edu.cn`.

## Paper
If you are interested in our work, please cite our paper as

```
@ARTICLE{liu2019energy,
    author={Liu, Chi Harold and Chen, Zheyu and Zhan, Yufeng},
    journal={IEEE Journal on Selected Areas in Communications},
    title={Energy-Efficient Distributed Mobile Crowd Sensing: A Deep Learning Approach (JSAC)},
    year={2019},
    volume={37},
    number={6},
    pages={1262-1276},
}
```
