# MemoTag Speech Intelligence - Cognitive Decline Detection

This project analyzes anonymized audio clips to detect early signs of cognitive impairment using unsupervised machine learning and NLP-based speech feature extraction.

---

## 📌 Objective

To extract meaningful linguistic and acoustic features from speech and identify participants showing early symptoms of cognitive decline, using unsupervised clustering techniques.

---

## 🔍 Extracted Features

We extracted a mix of linguistic and prosodic (acoustic) features from the audio samples:

| Feature | Description |
|--------|-------------|
| **Pauses per sentence** | Measures average pause duration and frequency. Increased pauses can suggest retrieval or fluency issues. |
| **Hesitation markers** | Counts "uh", "um", etc. High counts indicate potential processing or memory delays. |
| **Word recall issues** | Detects word substitutions or semantic anomalies using NLP patterns. |
| **Speech rate** | Calculated in words per minute. Lower speech rate may signal cognitive strain. |
| **Pitch variability** | Measures changes in vocal pitch over time. Flattened prosody can indicate neurological issues. |
| **Naming/Word-Association Gaps** | Manual or pattern-based checks for missing key terms. |
| **Sentence Completion Failures** | Incomplete or abruptly stopped sentences. Often found in MCI patients. |

---

## 🤖 Machine Learning Method

### K-Means Clustering (Unsupervised)

- **Why K-Means?**  
  No labels were available (diagnosis info), so clustering helped uncover natural groupings in speech data.

- **Steps**:
  - Extract features from each audio file.
  - Normalize data using scaling techniques.
  - Cluster into 2 groups using K-Means.
  - Visualize clusters for better interpretation.

- **Outcome**:
  - Two distinct clusters emerged.
  - One cluster showed higher pauses, slower speech, and more hesitations — indicating potential cognitive impairment.

---

## 🔮 Next Steps (Toward Clinical Robustness)

| Area | Description |
|------|-------------|
| **Labeled Dataset** | Collaborate with clinicians to obtain diagnostic labels. |
| **Advanced NLP** | Use models like BERT to detect subtle semantic impairments. |
| **Acoustic Modeling** | Apply `openSMILE`, `Praat`, or deep learning for prosody and articulation features. |
| **Multimodal Fusion** | Combine text, audio, and optionally video cues. |
| **Clinical Validation** | Integrate MMSE/MoCA scores for validation and evaluation. |

---

## ✅ Conclusion

This pipeline demonstrates how everyday voice recordings can be analyzed for cognitive health. With further refinement and data, this tool could become a **non-invasive, scalable screening method** for early cognitive disorders.

---

## 🧑‍💻 Project Overview

- **Audio Feature Extraction**: Extracts linguistic and acoustic features such as pauses, hesitation markers, speech rate, and pitch variability from speech.
- **Unsupervised Clustering**: Applies K-Means clustering to identify natural groupings in speech data, without requiring labeled data.
- **Cluster Interpretation**: Provides insights into cognitive impairment based on speech features (e.g., longer pauses, slower speech, and hesitation markers associated with cognitive decline).
- **Scalability**: The methodology can be extended to large datasets for widespread screening applications.

---

## 💡 Future Directions

1. **Improved Clustering Algorithms**: Experiment with other unsupervised algorithms like DBSCAN or hierarchical clustering for better groupings.
2. **Multimodal Data**: Combine speech with other data types (e.g., visual cues, clinical metrics) for more accurate predictions.
3. **Clinical Integration**: Work with medical professionals to validate the effectiveness of the tool for real-world clinical applications.

---

## 📚 References

- K-Means Clustering: A common unsupervised learning algorithm used for grouping similar data points.
- Whisper: A deep learning model for speech recognition that can transcribe audio to text.
- Librosa: A Python package for audio and music analysis, useful for extracting audio features such as pitch and speech rate.
- SpeechRecognition: A library to convert audio speech into text using Google Web Speech API.

---

## 👨‍💻 Creator

This project was developed by **Ashutosh Prasad**.
