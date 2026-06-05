# Music Emotion Recognition: Translating Musical Patterns into Emotional Cues

A 10-week summer research project for high school students.

Title: Translating Musical Patterns into Emotional Communication Cues for Children with Communication Challenges.

Research question: Can machine learning predict the perceived emotion of a short music clip from measurable audio features (tempo, pitch/chroma, MFCCs, loudness, rhythm), and can those musical cues be turned into a prototype communication-support tool?

## How to start

1. Open `music_emotion_classification.ipynb` -- or launch it directly in Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VietNguyen705/music-emotion-highschool/blob/main/music_emotion_classification.ipynb)
2. (Optional) Switch the runtime to GPU; this project runs fine on CPU too.
3. Fill in every TODO cell from top to bottom.

Ask your instructor if stuck. A completed reference is in `music_emotion_classification_solution.ipynb`.

## 10-Week Plan

| Week | Tasks |
|------|-------|
| 1 | Learn ML basics, audio/music information retrieval, and the music-emotion problem. Set up Python + Colab + GitHub. Download DEAM and listen to a clip |
| 2 | Literature review (music emotion recognition, valence-arousal, music therapy). Understand the annotation files |
| 3 | Inspect the dataset: number of clips, file format, metadata. Plot the valence-arousal annotation cloud |
| 4 | Extract audio features with librosa (tempo, chroma, MFCCs, spectral centroid, zero-crossing rate, RMS energy, beat strength). Build a feature CSV |
| 5 | Convert valence/arousal into 4 emotion categories (Happy, Calm, Tense, Sad). Build the labeled dataset and train/test split |
| 6 | Train baseline models: Logistic Regression, Decision Tree, Random Forest, SVM. Record accuracy, precision, recall, F1, confusion matrix |
| 7 | Interpret the best model: feature-importance chart and a short paragraph on which musical features predict emotion |
| 8 | Build a simple rule-based prototype mapping a communication need to a music cue. Present it as a research prototype, not a treatment |
| 9 | Write the IEEE-style paper (abstract, intro, methods, results, discussion, social impact). Build a "predict a new clip" demo |
| 10 | Final paper, slides, presentation. Discuss limitations and ethical considerations |

## Emotion Categories (valence-arousal quadrants)

| Valence | Arousal | Emotion category |
|---------|---------|------------------|
| High | High | Happy / Excited |
| High | Low  | Calm / Peaceful |
| Low  | High | Tense / Angry |
| Low  | Low  | Sad / Low-energy |

## Audio Features

`librosa` features extracted from each clip: tempo, chroma (pitch class energy), MFCCs, spectral centroid, zero-crossing rate, RMS energy, and beat/rhythm strength.

## Dataset

- **DEAM** (Database for Emotional Analysis of Music) -- 1,802 music excerpts with continuous and per-song **valence** (positive/negative feeling) and **arousal** (energy/intensity) annotations on a 1-9 scale. Audio clips are ~45 s MP3 files.
- Dataset page: https://cvml.unige.ch/databases/DEAM/
- Optional alternatives: **EMOPIA** (1,087 pop-piano clips, good for a violinist/musician) and **PMEmo** (794 pop choruses with EDA signals).
- The `mirdata` Python package can help download and validate MIR datasets.

> This project is a **research prototype**, not a medical or therapeutic tool.
