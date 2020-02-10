FROM jupyter/datascience-notebook

RUN pip install datawrapper
	
RUN conda install -c conda-forge --quiet --yes \
	'psycopg2' \
	&& \
	conda clean --all -f -y


RUN jupyter labextension install @jupyterlab/toc

RUN jupyter labextension install @jupyterlab/celltags

RUN jupyter lab clean && jupyter lab build

RUN jupyter lab build