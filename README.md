# Synapse-seq (*Dolan et al., 2025*) – Code and Vignettes

**Synapse-seq** is a suite of technologies designed to measure both single-neuron molecular expression profiles and long-range neuroanatomical projections. The **pre-synaptic system** enables detection of distal projections, making it possible to analyze how a neuron's transcriptomic identity relates to its projection behavior.

## 📘 Vignettes

This repository provides walkthroughs for key analytical components of Synapse-seq.  
We recommend starting with the **presynaptic vignette**, which characterizes **cortico-thalamic projections from the primary visual cortex (VISp)**.

---

## Data Access

All required data is publicly available in a Google Cloud Storage bucket.

### Programmatic Access

Data can be accessed using the Google Cloud SDK [Google Cloud SDK](https://cloud.google.com/sdk/docs/install-sdk) at:
gs://macosko_public/Synapseseq_data_2025

For executing vignettes, required files will be downloaded at beginning of the notebook.

### Manual Access

You can also browse and download the data manually from the following link:  
[Google Cloud Console – Synapseseq Data (2025)](https://console.cloud.google.com/storage/browser/macosko_public/Synapseseq_data_2025)

### Create environment

The requirements.yaml file can be used to create a conda environment for which we can use to execute the notebooks.

Ensure a conda solver is installed. We recommend mamba. (https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html)


The `requirements.yaml` file can be used to create a conda environment for running the notebooks.

```
 mamba env create -f requirements.yaml -n synapseseq_env
 mamba activate synapseseq_env
```

Next we need to export the environment so it is accessible via jupyter.
```
python -m ipykernel install --user --name synapseseq_env --display-name "synapseseq_env"
```

Then run jupyter-lab
```
jupyter-lab --ip='*' --port=8989
```
