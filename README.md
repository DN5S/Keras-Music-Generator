# Keras Music Generator

A deep learning project that generates music compositions using LSTM (Long Short-Term Memory) neural networks. This project uses Keras and Music21 to analyze MIDI files of existing music and generate new compositions in similar styles.

## Overview

This project demonstrates how to:
- Process MIDI files to extract musical notes and patterns
- Train an LSTM neural network on different musical styles
- Generate new musical compositions based on the learned patterns
- Save the generated music as MIDI files

## Project Structure

```
├── Music Composition.ipynb   # Main Jupyter notebook with the code
├── Music/                    # Input MIDI files for training
│   ├── Etudes, Opus 10/      # Chopin's Etudes
│   ├── Jazz/                 # Jazz compositions
│   └── Piano Sonata in D major Hoboken XVI33/ # Haydn's Piano Sonata
├── Etudes, Opus 10 Output/   # Generated music based on Chopin's style
├── Piano Sonata in D major Hoboken XVI33 Output/ # Generated music based on Haydn's style
└── train_data/              # Preprocessed training data in h5 format
```

## Requirements

- Python 3.6+
- TensorFlow
- Keras
- Music21
- NumPy
- Matplotlib
- Jupyter Notebook

## Installation

1. Clone this repository:
```
git clone https://github.com/yourusername/Keras-Music-Generator.git
cd Keras-Music-Generator
```

2. Install the required packages:
```
pip install tensorflow keras music21 numpy matplotlib jupyter
```

3. If you're using Windows, you might need to install a music notation software like MuseScore for Music21 to work properly:
   - Download and install [MuseScore](https://musescore.org/en/download)
   - Configure Music21 to use MuseScore by running:
   ```python
   from music21 import environment
   us = environment.UserSettings()
   us['musicxmlPath'] = 'C:/Program Files/MuseScore 3/bin/MuseScore3.exe'  # Adjust path as needed
   ```

## Usage

1. Open the Jupyter notebook:
```
jupyter notebook "Music Composition.ipynb"
```

2. Run the cells in the notebook to:
   - Load and preprocess MIDI files
   - Create training sequences
   - Build and train the LSTM model
   - Generate new music compositions

3. The generated MIDI files will be saved in the output directories based on the style of music used for training.

## Training Data

The project includes several types of training data:
- **Chopin's Etudes, Opus 10**: Classical piano compositions by Frédéric Chopin
- **Haydn's Piano Sonata in D major**: Classical piano compositions by Joseph Haydn
- **Jazz**: Various jazz compositions

You can add your own MIDI files to train the model on different styles of music.

## Generated Output

The model generates music at different epochs during training (100, 200, 300, 400, 500). This allows you to see how the quality of the generated music improves as the model learns.

## Customization

You can customize the model by:
- Changing the LSTM architecture (layers, units)
- Adjusting the sequence length
- Using different training data
- Modifying the temperature parameter for generation

## Acknowledgments

This project uses:
- [Keras](https://keras.io/) for deep learning
- [Music21](https://web.mit.edu/music21/) for music analysis and manipulation
- MIDI files from various composers for training data
