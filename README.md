# RoboCup Rescue Simulator(RCRS)-Gym Integration
 
(Linux) Instructions to download, build and run the RoboCup Rescue Simulator (RCRS) integrated with OpenAI Gym. OpenAI Gym is a toolkit for developing and comparing reinforcement learning algorithms.

## 1. Software Pre-Requisites

* Git
* Gradle 3.4+
* OpenJDK Java 8+
* Python 3.5+
* Openai Gym
* Stable Baselines
* Tensorboard 1.14 (Note: Stable baselines is not compatible with Tensorboard 2.0) 

## 2. Download project from GitHub

```bash

$ git clone https://github.com/animeshgoyal9/RoboCup-Gym.git

``` 

## 3. Compile

Open a terminal window, navigate to the `rcrs-server-master` root directory and compile 

```bash 

$ ./gradlew clean

$ ./gradlew completeBuild

```

Open another terminal window, navigate to the `rcrs-adf-sample` root directory and compile 

```bash 

$ sh clean.sh

$ sh compile.sh

```

Close the second terminal

## 4. Execute

On the first terminal, navigate to the `boot` folder in  `rcrs-server-master` directory and run the following python file 

```bash

$ testing.py

``` 

## 5. Visualization

To visualize the reward over time, losses etc, you can use tensorboard. 

Open a new terminal window and run the following bash command

```bash

$ tensorboard --logdir ./ppo2_RoboCupGym_tensorboard/

``` 

## 6. Code Structre

- `./rcrs-server-master/`: folder where simulation server resides
- `./rcrs-adf-sample/`   : folder where simulation client resides
- `./PyRCRSClient/`      : gRPC python and proto files for client side 
- `./New_RCRS/`          : gRPC java and proto files for server side







