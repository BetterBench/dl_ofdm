# Paper 
Zhongyuan Zhao, Deep-Waveform: A Learned OFDM Receiver Based on Deep Complex Convolutional Networks, EESS.SP, vol abs/1810.07181, Oct. 2018, [Online] https://arxiv.org/abs/1810.07181

[Pre-Print](https://arxiv.org/abs/1810.07181)

@article{zhao2018dcnn,
author={Zhongyuan Zhao},
title={Deep-Waveform: A Learned OFDM Receiver Based on Deep Complex Convolutional Networks},
journal={EESS.SP},
vol = {abs/1810.07181},
month = {Oct},
year = {2018},
url={https://arxiv.org/abs/1810.07181},
}

## About this code
Cross validation benchmark for Deep Learning-Based OFDM Receiver.

+ Modulation: BPSK, QPSK, 8-QAM, 16-QAM, of Gray mapping.
+ SNR: -10:1:29 dB

## Usage
1. Run `OFDM_benchmark` in Matlab to generate .mat data for the received time-domain OFDM signal and corresponding TX bits per modulation per SNR. Each file has a size of 20MB, and total for about 3.7GB. The generated .mat data will be saved in `./mat/`
2. Run `python test_ofdm_cdnn_awgn.py --save_dir=./model/ --data_dir=./mat/` in terminal. This will load the trained models in ./model/ folder, and test the model with data stored in ./mat/ folder

## Tensors in loaded model
+ y: input bits, 
+ x: input received OFDM waveform,
+ outputs: output soft bits,
+ berlin: BER,
