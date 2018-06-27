
# 模拟信号压缩感知的 AIC 实现研究(Research on AIC implementation of analog signal based on compressed sensing)

## 中文简介

根据香农定理，必须以不小于奈奎斯特采样频率的采样速率对模拟信号采样，才能保证信号不失真地恢复，对于高频信号，实际生产的模拟到数字转换器（ADC）很难满足采样速率与带宽的要求。

我们研究实现了一套针对于稀疏宽带信号的，基于压缩感知的欠奈奎斯特采样系统，将稀疏宽带信号与周期信号相乘混叠，然后用普通低速低带宽ADC采样，再使用重构算法进行原始信号的精确重构。在16.8%的欠奈奎斯特采样率下，仍能较精确地重构信号。

本人负责子板的调试，系统联调，项目结题等工作！

## English Introduction

Based on compressed sensing, the Sub-Nyquist sampling method is studied, and the hardware verification system is implemented.

According to the Nyquist sampling theorem, in order to sample the signal without distortion, the sample rate of analog to digital converter (ADC) must larger than Nyquist sampling frequency (the maximum frequency of the signal of 2 times). However, for high-frequency signals, in actual, the sampling rate and bandwidth of the ADC is difficult to meet.

According to the theory of compressed sensing, most of the signals in nature are sparse. For sparse wideband analog signals, multiplying the sparse wideband signal with the mixing periodic signal in m channels. After mixing, the signal spectrum is truncated by a low-pass filter, and the filtered signal is sampled at a very low sampling rate. The original signal can be recovered by the reconstruction algorithm from the samples.

I am responsible for the analog board debugging, demo video production, project acceptance, etc.


# 相关概念

模拟到信息转换器（Analog to Information Converter，AIC），不同于传统的ADC，AIC在信号稀疏先验知识下，通过欠奈奎斯特频率的采样值对信号进行采样，并能够通过采样值精确恢复原信号，并且，欠奈奎斯特采样频率直接和信号的信息相关。

调制宽带转换器（Modulated Wideband Converter，MWC），一种针对稀疏宽带信号的Sub-Nyquist采样转换器，通过对稀疏宽带信号与周期信号相乘混叠，然后低速率采样，再用重构算法恢复原始信号的一种转换器。
