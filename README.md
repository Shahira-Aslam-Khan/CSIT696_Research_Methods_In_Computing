# CSIT696_Research_Methods_In_Computing
The project trains a composite deep-learning pipeline comprising a Denoising Autoencoder (DAE), Graph Neural Network (GNN), Multi-Head Attention mechanism, and a 1D Convolutional Neural Network (CNN1D) on CTGAN-synthesised telemetry data. 


Arista Network Telemetry Anomaly Detection Research Report:
Project Overview This report documents the research and validation of an AI-driven anomaly detection system specifically designed for Arista network telemetry data. The project focuses on utilizing a composite deep-learning pipeline to correlate millions of logs into predictive patterns for identifying network irregularities and classifying event severity. 
________________________________________
Proposed Model Architecture The core of the system is a Neural Processing Engine (NPE) designed to handle temporal event prediction and pattern recognition. The finalized architecture integrates four key model families: 
•	Denoising Autoencoder (DAE): Used for initial feature extraction and noise reduction. 
•	Graph Neural Network (GNN): Captures relational dependencies and node-level anomaly scores. 
•	Multi-Head Attention: Identifies critical temporal patterns within the telemetry sequences. 
•	1D Convolutional Neural Network (CNN1D): Extracts local spatial and temporal patterns from event sequences. 
________________________________________
Data Ingestion and Methodology The project developed a full-scale data ingestion pipeline that extracts system, simple, and application logs from CSV files. 
•	Data Transformation: Timestamps are normalized to UTC, and severity labels (e.g., "warn", "err") are standardized into canonical forms like WARNING and ERROR. 
•	Synthetic Data: Due to the lack of live production logs, the models were trained on data synthesized using a Conditional Tabular GAN (CTGAN). 
•	Pipeline Iterations: Two versions were compared—an older prototype and a refined "NEW" version—to evaluate stability and correctness. 
________________________________________
Key Findings and Comparative Analysis The research highlighted a critical structural improvement in the NEW pipeline iteration. 
•	Code Correctness: A major bug in the OLD pipeline’s encoding method was fixed, ensuring all neural layers (GAT, Attention, Conv1D) are fully utilized. 
•	Stability: While the OLD pipeline showed higher headline accuracy (99%), it exhibited signs of overfitting. The NEW pipeline demonstrated 4x lower variance in cross-validation, indicating more reliable generalization. 
•	Volume: The NEW iteration successfully trained on nearly double the event volume (19,747 events) compared to the prototype. 
________________________________________
Conclusion and Recommendations:  The NEW pipeline is recommended as the foundation for future production deployment due to its architectural integrity and consistent performance. Future work will focus on integrating live collection agents like FluentBit and SNMP pollers, re-introducing numeric feature dimensions, and testing the system under live network conditions. Plans to work on using a mobile phones logs generated across various tools to ger a glimpse of the project’s current situation and future.


