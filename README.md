# dl_ofdm
Cross validation benchmark for Deep Learning-Based OFDM Receiver.

+ Modulation: BPSK, QPSK, 8-QAM, 16-QAM, of Gray mapping.
+ SNR: -10:1:29 dB

Usage:
1. Run OFDM_benchmark.m in Matlab to generate .mat data for the received time-domain OFDM signal and corresponding TX bits per modulation per SNR. Each file has a size of 20MB, and total for about 3.7GB.
2. Run 'test_ofdm_cdnn_awgn.py --save_dir=./model/ --data_dir=./mat/'
