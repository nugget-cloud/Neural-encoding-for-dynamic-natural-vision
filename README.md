Objective:

To design, develop, and validate a deep learning-based model that decodes and predicts the specific visual stimuli presented to individuals based on their intracranial electrocorticography (iEEG) recordings.

This project seeks:

Decoding Sensory Representations: To understand the intricate patterns of brain activity and uncover how different visual stimuli are neurally represented and processed in the human brain. This involves translating the high-dimensional iEEG data into discernible visual stimulus attributes.

Advanced Neural Model Development: To employ state-of-the-art deep learning techniques, leveraging the temporal precision and spatial resolution of iEEG data, aiming to achieve accurate stimulus predictions.

Insights into Neural Processing: Beyond mere prediction, the project aims to shed light on the underlying neural mechanisms of sensory perception, potentially revealing the hierarchical and distributed nature of visual information processing in the cortex.

Enhanced Understanding of Brain Function: By successfully decoding visual stimuli from brain activity, the project can offer insights into how sensory information is encoded in neural circuits, enhancing our understanding of brain function, especially in the context of sensory perception.
1.1 Initial Exploration:

    Open the README and CHANGES files to understand any dataset-specific nuances or updates.
    Examine the dataset_description.json for an overview of the dataset's metadata.

1.2 Load & Visualize Raw Data:

    Load a subset of the iEEG data from one of the participant directories to visualize and understand the data's nature.
    Plot time-series data to inspect any noticeable patterns, artifacts, or noise.

1.3 Preprocessing:

    Based on the visualization, apply necessary filtering techniques to remove noise and artifacts.
    Normalize the data to ensure consistent scales across sessions and participants.
    Use the *.tsv and *.json files within participant folders to align events with EEG recordings.

2. Feature Engineering:
2.1 Time-frequency Transformations:

    Convert the iEEG data into spectrograms or other time-frequency representations.

2.2 Electrode Selection:

    Use the metadata provided to select the most relevant electrodes based on their location and data quality. Exclude electrodes marked as 'bad' in the channels.tsv files.

3. Dataset Preparation for Deep Learning:
3.1 Data Labeling:

    Use the provided task-*.json files to label the iEEG data based on the visual stimuli presented to participants.

3.2 Data Splitting:

    Split the dataset into training, validation, and test sets. Ensure that the split is stratified based on the different visual stimuli.

3.3 Data Augmentation (if necessary):

    To increase the size of the training set, apply data augmentation techniques suitable for time-series data.

4. Model Development:
4.1 Model Architecture:

    Design a hybrid deep learning model combining CNNs (for spatial patterns) and RNNs (for temporal patterns).

4.2 Training Strategy:

    Train the model using a stratified split or k-fold cross-validation.
    Use attention mechanisms to focus on crucial time points in the iEEG data.

4.3 Hyperparameter Tuning:

    Experiment with different hyperparameters to optimize the model's performance.

5. Model Evaluation:
5.1 Performance Metrics:

    Use metrics like accuracy, F1 score, and AUC-ROC to evaluate the model.

5.2 Cross-validation:

    Evaluate the model's robustness using k-fold cross-validation.

6. Interpretability & Insights:
6.1 Feature Importance:

    Use techniques like SHAP or LIME to interpret which features (e.g., time points, electrodes) are crucial for predictions.

6.2 Neuroscientific Mapping:

    Relate the model's predictions to known neuroscientific findings, enhancing the understanding of the neural representation of visual stimuli.

7. Iterative Refinement:
7.1 Feedback Loop:

    Revisit the model based on insights gained from the interpretability phase and refine accordingly.

7.2 Collaboration with Neuroscientists:

    Share preliminary findings with experts in the field to get feedback, ensuring that the model's insights align with existing knowledge.

8. Documentation & Dissemination:
8.1 Documentation:

    Thoroughly document the methodology, findings, and insights.

8.2 Share Findings:

    Consider publishing results and sharing the methodology with the broader scientific community.
