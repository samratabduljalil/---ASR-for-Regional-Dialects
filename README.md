
Fine-Tuning Whisper for Bangladeshi Dialects
This project explores fine-tuning OpenAI's Whisper model to improve speech recognition for Bangladeshi regional dialects. The journey involved comparing standard Whisper performance with district-wise fine-tuning. Ultimately, the original Whisper model trained on a unified dataset outperformed district-wise training.

Project Workflow
Initial Experiment:
The original Whisper model was tested with minimal fine-tuning. It provided baseline performance across diverse Bangladeshi dialects.

District-Wise Training:
Separate models were fine-tuned for each district, aiming to specialize the ASR for specific regional dialects. However, this approach performed poorly due to insufficient generalization and limited district-specific data.


Results
Best Performance: Unified dataset training achieved a Word Error Rate (WER) of 0.76576, significantly outperforming the district-wise models.
District-Wise Models: These models struggled with higher WERs due to overfitting and lack of comprehensive dialectal coverage.

Key Insights
Unified Dataset Wins: Combining data from all districts provided better generalization and robustness, outperforming district-wise training approaches.


How to Use
Fine-Tune the Model: Use the provided dataset  to fine-tune the Whisper model for Bangladeshi dialects.
Perform Inference: Use the fine-tuned model to transcribe speech from various Bangladeshi dialects.

Future Work
Explore methods to improve district-specific performance.
Collect more diverse and representative datasets for underrepresented regions.
Evaluate model performance on live data for real-world applications.


domain_weights = {
    'Barishal': 0.125,
    'Chittagong': 0.083,
    'Habiganj': 0.125,
    'Kishoreganj': 0.083,
    'Narail': 0.083,
    'Narsingdi': 0.083,
    'Rangpur': 0.083,
    'Sylhet': 0.125,
    'Sandwip': 0.125,
    'Tangail': 0.083,
}

Model Link : https://www.kaggle.com/datasets/samratabduljalil/bhasha-bichitra-model

