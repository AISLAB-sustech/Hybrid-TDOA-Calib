# Hybrid-TDOA-Calib
This project has open source code and data for the article titled "Asynchronous Microphone Array Calibration Using Hybrid TDOA Information". This article aims to solve the calibration problem of asynchronous microphone arrays, which involves using hybrid TDOA and odometry measurements to construct a graph SLAM that simultaneously estimates microphone parameters (microphone positions, time offsets, and clock drift rates) and sound source positions. Simulation and real experiments consistently prove that our method performs better than the existing method.

## Calibration Scenario
<img src="https://github.com/Chen-Jacker/Hybrid-TDOA-Calib/blob/main/calibration_scenario.gif" width="500px">
The full video with high quality is avaliable at https://youtu.be/pmVgjJdjW2E.

## Audio Accessment
Link in OneDrive: https://1drv.ms/f/s!AilTdY3K-LzJgbdgoZZSl9-d8883ow?e=gFOias. After download it, place folder named "Audio" at the same level as folder "displacement". If the link has expired, send me an email to remind me.

## How to use
- `quick_start.m` realizes the estimation and visualization of calibration results between our method and the other method.
- `sim_main.m` achieves simulations in paper.
- `real_main.m` achieves real-world experiments in paper.
- `DataAnalysis.m` plot the results computed from `sim_main.m` and `real_main.m`. `data_id`=6,7,8 represent results concerning microphone locations, time offsets and clock drift rates respectively.

## Details
- The first part in `real_main` computes TDOA-S and TDOA-M based on real-world audio in folder named "audio".
- In the array named IFLYTEK M160C we use, the default output is microphone 0 as the first channel. However, we changed the audio output of microphone 0 to the last channel (sixth) and then output  `.wav` file.
- My email: 11911918@mail.sustech.edu.cn.
- link of the paper in arxiv: https://arxiv.org/abs/2403.05791.
