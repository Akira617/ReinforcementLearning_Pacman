## Pacman using Q-Learning methods

## Overview

This repository contains codes for the implementation of 
1) Q-Learning
2) Approximate Q-Learning
3) Deep-Q-Learning



## To install dependencies via command-line

Access your project directory, open terminal and type the following commands to clone the repository.

```
mkdir -p ~/workspace
cd ~/workspace
git clone --recursive https://github.com/NithishkumarS/ReinforcementLearning_Pacman.git
```

Once repository is cloned, type the following commands to run the demo.

```
pip3 install --user --upgrade tensorflow
```
To verify install
```
python3 -c "import tensorflow as tf; tf.enable_eager_execution(); print(tf.reduce_sum(tf.random_normal([1000, 1000])))"
```

### Layouts
Different layouts can be found and created in the `layouts` directory


To train and test the pacman game for different grid run the following commands

To check the Q-learning demo run 
```
cd src/Pacman
python pacman.py -p PacmanQAgent -x 2000 -n 2010 -l smallGrid
d
```
```
python pacman.py -p PacmanQAgent -x 2000 -n 2010 -l mediumGrid
```
```
python pacman.py -p PacmanQAgent -x 2000 -n 2010 -l mediumClassic
```


To check the Approximate Q-learning demo run
```
python pacman.py -p ApproximateQAgent -a extractor=SimpleExtractor -x 20 -n 25 -l smallGrid
```
```
python pacman.py -p ApproximateQAgent -a extractor=SimpleExtractor -x 50 -n 60 -l mediumGrid
```
```
python pacman.py -p ApproximateQAgent -a extractor=SimpleExtractor -x 50 -n 60 -l mediumClassic
```

To check the DQN demo
```
cd ..
cd PacmanDeep

python3 pacman.py -p PacmanDQN -n 5000 -x 4000 -l smallGrid
```
```
python3 pacman.py -p PacmanDQN -n 6000 -x 5000 -l mediumGrid
```

```
python3 pacman.py -p PacmanDQN -n 11000 -x 10000 -l mediumClassic
```
Here -n paramter is the total number of episodes (training + testing)
     -x parameter is for total number of episodes of training

## Acknowledgements

Pac-man implementation by UC Berkeley:
* [The Pac-man Projects - UC Berkeley](http://ai.berkeley.edu/project_overview.html) ([http://ai.berkeley.edu/project_overview.html](http://ai.berkeley.edu/project_overview.html))


DQN Framework by  (made for ATARI / Arcade Learning Environment)
* [deepQN_tensorflow](https://github.com/mrkulk/deepQN_tensorflow) ([https://github.com/mrkulk/deepQN_tensorflow](https://github.com/mrkulk/deepQN_tensorflow))

