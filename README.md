# Epigenetic-Guided-Transformer
Deepmind's enformer model guided by epigenetic findings through "pathogenomic fingerprinting"

The Google Collab code runs as-is. To run locally with your own GPU/CPU:

1. Setup virtual environment
  python3 -m venv enformer_venv

2. Activate environment. Should appear in default pwd.
  source enformer_venv/bin/activate

3. Get the enformer repository from DeepMind
  git clone https://github.com/google-deepmind/deepmind-research.git

4. Navigate to the enformer folder where the requirements list is located. Install latest pandas and tensorflow_hub, then run requirements.txt. Make sure Python 3.9, TF 2.18, numpy 2.0, tensorflow_hub 0.16 are installed.
   
  cd deepmind-research/enformer
	•	pip install pandas
	•	pip install --upgrade tensorflow-hub
	•	pip install —r requirements.txt

6. Run Jupyter notebook. Import tensorflow and tensorflow_hub. In tensorflow_hub 2.0, enformer = hub.Module('https://tfhub.dev/deepmind/enformer/1’), is deprecated. Use:

  enformer = hub.load('https://tfhub.dev/deepmind/enformer/1')

6. Update jsonschema and kipoiseq:
  pip install --upgrade attrs
