# periquito

transcription

## usage

Periquito takes a sound file as input and produces four text file outputs. One text file output is a simple text transcription. Another is a transcription in SRT format. Another is a JSON giving the start and end times of the various words transcribed. Another is a progressive version of the simple text transcription, but one which is written to progressively as the program runs, enabling the prompt use of a partial transcription (which may be of use for parsing, or for prompt consultation in the case of a lengthy transcription).

## setup Ubuntu 22.04

```Bash
sudo apt install -y python3-venv python3-dev ffmpeg libsndfile1
sudo apt install -y python3.10-venv
sudo apt install -y ffmpeg

sudo pip3 install "numpy<2.0" # precaution to avoid an incompatibility reported for some NeMo builds
sudo pip3 install soundfile webrtcvad tqdm
sudo pip3 install "torch==2.4.*" "torchaudio==2.4.*" --index-url https://download.pytorch.org/whl/cpu
sudo pip3 install --no-build-isolation "nemo_toolkit[asr]>=2.2,<3"
sudo pip3 install "nemo_toolkit[asr]>=2.2,<3"
sudo pip3 install -U "ml_dtypes>=0.5.0"
sudo pip3 install transformer-engine
```
