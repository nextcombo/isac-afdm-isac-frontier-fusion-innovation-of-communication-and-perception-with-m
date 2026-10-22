# ISAC: AFDM-ISAC Frontier: Fusion Innovation of Communication and Perception [with MATLAB Code]

Abstract: This paper summarizes the theoretical basis of an integrated communication and perception (ISAC) system based on Non-Orthogonal Multicarrier (AFDM) technology. The system achieves both data transmission and target detection functions through the sharing of AFDM waveforms. The article details the modulation and demodulation mechanism, target echo model, communication signal restoration method, and radar perception signal processing flow of the system. It also verifies the system performance through constellation diagrams and Radar Decision Algorithm (RDA) visualization, providing a theoretical reference for the waveform design and signal processing of ISAC technology.
1. System Overview: The AFDM-ISAC system is centered around the adaptive frequency diversity multicarrier (AFDM) waveform, achieving efficient resource utilization through a single transmit signal that carries both communication information and radar perception tasks simultaneously. The core objectives of the system include: (1) Communication link: Transmitting high-order Quadrature Amplitude Modulation (QAM) signals through AFDM modulation, which are then recovered at the receiver end after equalization; (2) Perception link: Estimating the distance-Doppler characteristics of target echoes to achieve position and velocity detection of multiple targets. The system architecture is depicted in Figure 1 (conceptual framework), mainly comprising four modules: waveform generation at the transmitter, channel and target echo modeling, communication signal recovery at the receiver, and radar signal processing.
2. System Parameters and Waveform Design: 2.1 Core Parameter Configuration: System physical layer parameters determine the time-frequency characteristics of the waveform. Key parameters include:
Communication parameters: Subcarrier number (determining the frequency resolution), slow time pulse count (determining the Doppler resolution), QAM modulation order (determining the communication rate), SNR (representing the level of channel noise);
Physical layer parameters: Carrier frequency (determining the radar wavelength), subcarrier interval (determining the signal bandwidth), sampling rate (meeting the Nyquist criterion), CPP length (similar to a cyclic prefix, needed to combat multipath delay spread and should be greater than the maximum target delay corresponding to the number of samples).
2.2 Principle of AFDM Waveform Modulation
QAM symbol generation: Randomly generated -QAM symbol matrix, satisfying the unit average power constraint;
Inverse DAFT (IDAFT) transformation: Apply IDAFT to each column, generating time-domain block signals. The transformation formula is:
Among them, chirp modulation factor is the system design parameter to control time-frequency focusing characteristic.
CPP Modification: Add a tail sampling point for each time-domain block prefix to form the transmitted signal, in order to eliminate inter-block interference.
3. Communication Link Theory
Among them, for the multi-target echo signal, it is AWGN, whose power is determined.
3.2 The communication signal recovery receiver restores the communication symbols through the following steps:
CPP removal: Split the received signal into blocks, remove the leading samples of each block, resulting in a time-domain block.
DAFT Transformation: Inverse of the DAFT transformation (the reverse process of IDAFT), converted to the DAFT domain:
Channel Estimation and Equalization: Assuming the transmitted symbols are known (or estimated through pilots), the channel response is estimated using the Least Squares (LS) criterion, and then the received symbols are restored.
Performance Evaluation: By comparing the constellation diagrams of the transmitter and receiver, the degree of signal distortion can be intuitively evaluated, reflecting the reliability of the link.
4. Perception Link Theory
Among them, the target refraction coefficient is the target distance-corresponding time delay sampling number (the sampling interval), the target velocity-corresponding normalized Doppler frequency shift (the speed of light). Multi-target echoes are the linear superposition of individual target echoes.
4.2 Time-domain FCCR signal processing employs the fast cross-correlation radar (FCCR) method to estimate target range and Doppler information:
Fast time FFT: Conduct a fast time (subcarrier dimension) FFT on both the received time domain block and the transmitted time domain block, obtaining the frequency domain signals;
Frequency domain cross-correlation: Calculate the conjugate product of the frequency domain to achieve signal matching filtering;
Fast time IFFT: Conduct a fast time IFFT on the resultant distance domain target response;
Slow time FFT: Conduct a slow time (pulse dimension) FFT on the distance domain result, obtaining the range - Doppler spectrum (RDM), whose amplitude reflects the energy distribution of the target in the range-velocity plane.
4.3 Physical quantity conversion for distance axis: Range resolution, with range coordinates as (range gate index);
Doppler (velocity) axis: Doppler resolution (single symbol duration), velocity coordinates as (Doppler frequency offset).
5. Visualization and performance verification system performance is verified through two types of visualization results:
Communication performance: Comparison between the transmitter-QAM constellation diagram and the receiver-equalized constellation diagram, reflecting the quality of signal demodulation; the higher the clustering of constellation points, the better the communication performance;
Perception performance: 2D/3D range - Doppler spectrum (RDM), where the 2D plot is displayed using an amplitude dB heatmap to show the target energy distribution, and the 3D plot intuitively presents the relationship between distance - velocity - energy by surface rendering. Adding real target positions (marked in red) can quantify perception accuracy.
6. Conclusion The AFDM-ISAC system realizes efficient integration of communication and perception through the combination of DAFT modulated multi-carrier communication technology and FCCR radar signal processing methods. Theoretical analysis and simulation processes indicate that the system can provide reliable data transmission and high-precision target detection capabilities simultaneously, providing a feasible technical framework for ISAC applications in millimeter wave bands (such as 24GHz). Further optimization of chirp factor design and channel estimation algorithms can be conducted to enhance the system's robustness in complex scenarios.
Keywords: Communication and Perception Integration (ISAC); AFDM; DAFT Transformation; Distance-Doppler Estimation; Constellation Map

## Images

![[ISAC] AFDM-ISAC Frontier: Fusion Innovation of Communication and Perception (with MATLAB Code)](01.jpg)
![[ISAC] AFDM-ISAC Frontier: Fusion Innovation of Communication and Perception (with MATLAB Code)](02.jpg)
![[ISAC] AFDM-ISAC Frontier: Fusion Innovation of Communication and Perception (with MATLAB Code)](03.jpg)
![[ISAC] AFDM-ISAC Frontier: Fusion Innovation of Communication and Perception (with MATLAB Code)](04.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
