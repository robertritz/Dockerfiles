FROM jupyter/datascience-notebook

RUN conda config --append channels plotly

RUN conda install -c plotly --quiet --yes \
    'plotly' \
	'plotly_express' \
	'chart-studio' \
	'plotly-geo' \
	&& \
    conda clean --all -f -y

RUN jupyter labextension install @jupyterlab/plotly-extension

RUN jupyter lab clean && jupyter lab build