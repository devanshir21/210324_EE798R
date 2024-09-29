# 210324_EE798R
Title of the Paper:
Driving Stress Detection Using Multimodal Convolutional Neural Networks with Nonlinear Representation of Short-Term Physiological Signals
Paper Summary:
The paper introduces a method for detecting driving stress using short-term physiological signals (Galvanic Skin Response - GSR, and Heart Rate - HR). The physiological signals are transformed into 2D continuous recurrence plots (Cont-RPs), which are then processed by a multimodal Convolutional Neural Network (CNN) to classify stress levels.
Key Contributions:
Multimodal CNN: Combines multiple signals (FGSR, HGSR, HR) using parallel CNNs for better stress detection.
Continuous Recurrence Plots (Cont-RPs): Nonlinear representation of time-series data that captures complex dynamic patterns in physiological signals.
Short-Term Signals: Focuses on signals of 10-30 seconds, making it suitable for real-time stress detection.
Data Used:
The paper uses the SRAD (Stress Recognition in Automobile Drivers) dataset, which includes real-world physiological signals collected from drivers in various stress levels (low, medium, high).
Model Architecture:
The model consists of three separate CNNs for FGSR, HGSR, and HR signals, with a VGG16-based architecture. These outputs are concatenated and passed through a fully connected layer for binary classification (stressed vs. relaxed).
Results:
The model achieved 95.67% accuracy with 30-second signals and 92.33% with 10-second signals, outperforming previous methods that required longer signals.
Why This Approach?
By using multiple physiological signals and nonlinear transformations (Cont-RPs), the model captures more intricate stress-related features, improving the accuracy of real-time stress detection.
Implementation Overview:
Preprocessing: Resampling, noise filtering, and normalization of physiological signals.
Feature Extraction: Generation of Continuous Recurrence Plots (Cont-RPs).
Model: Multimodal CNN trained using leave-one-recording-out cross-validation.
