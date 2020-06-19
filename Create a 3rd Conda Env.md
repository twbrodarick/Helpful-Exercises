# Hello

Creates the vizenv environment

``` bash
conda env create -f environment.yml
```

```bash
conda activate vizenv
```

``` bash
set NODE_OPTIONS=--max-old-space-size=4096
jupyter labextension install @jupyter-widgets/jupyterlab-manager@1.1 --no-build
jupyter labextension install jupyterlab-plotly@4.6.0 --no-build
jupyter labextension install plotlywidget@4.6.0 --no-build
jupyter labextension install @pyviz/jupyterlab_pyviz --no-build
jupyter lab build
set NODE_OPTIONS=
```

``` bash
python -c "import nltk;nltk.download('all')"
pip install --upgrade "ibm-watson>=3.0.3"
python -m spacy download en_core_web_sm

python -m ipykernel install --user --name vizenv --display-name "Python (Viz)"
```
