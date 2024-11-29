
    <h1>Fine-Tuning Whisper for Bangladeshi Dialects</h1>
    <p>
        This project explores fine-tuning OpenAI's Whisper model to improve speech recognition for Bangladeshi regional dialects.
        The journey involved comparing standard Whisper performance with district-wise fine-tuning. Ultimately, the original Whisper model 
        trained on a unified dataset outperformed district-wise training.
    </p>

    <h2>Project Workflow</h2>
    <h3>Initial Experiment:</h3>
    <p>
        The original Whisper model was tested with minimal fine-tuning. It provided baseline performance across diverse Bangladeshi dialects.
    </p>

    <h3>District-Wise Training:</h3>
    <p>
        Separate models were fine-tuned for each district, aiming to specialize the ASR for specific regional dialects. 
        However, this approach performed poorly due to insufficient generalization and limited district-specific data.
    </p>

    <h2>Results</h2>
    <ul>
        <li><strong>Best Performance:</strong> Unified dataset training achieved a Word Error Rate (WER) of <strong>0.76576</strong>, 
        significantly outperforming the district-wise models.</li>
        <li><strong>District-Wise Models:</strong> These models struggled with higher WERs due to overfitting and lack of comprehensive 
        dialectal coverage.</li>
    </ul>

    <h2>Key Insights</h2>
    <ul>
        <li><strong>Unified Dataset Wins:</strong> Combining data from all districts provided better generalization and robustness, 
        outperforming district-wise training approaches.</li>
    </ul>

    <h2>How to Use</h2>
    <ul>
        <li><strong>Fine-Tune the Model:</strong> Use the provided dataset to fine-tune the Whisper model for Bangladeshi dialects.</li>
        <li><strong>Perform Inference:</strong> Use the fine-tuned model to transcribe speech from various Bangladeshi dialects.</li>
    </ul>

    <h2>Future Work</h2>
    <ul>
        <li>Explore methods to improve district-specific performance.</li>
        <li>Collect more diverse and representative datasets for underrepresented regions.</li>
        <li>Evaluate model performance on live data for real-world applications.</li>
    </ul>

    <h2>Domain Weights</h2>
    <code>
domain_weights = {<br>
    'Barishal': 0.125,<br>
    'Chittagong': 0.083,<br>
    'Habiganj': 0.125,<br>
    'Kishoreganj': 0.083,<br>
    'Narail': 0.083,<br>
    'Narsingdi': 0.083,<br>
    'Rangpur': 0.083,<br>
    'Sylhet': 0.125,<br>
    'Sandwip': 0.125,<br>
    'Tangail': 0.083,<br>
}
    </code>



