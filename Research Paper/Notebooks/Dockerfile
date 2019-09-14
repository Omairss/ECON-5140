FROM continuumio/anaconda3
RUN  /bin/bash -c "/opt/conda/bin/conda install jupyter -y --quiet \
	&& mkdir /opt/notebooks"

RUN apt-get -y install gcc &&
	apt-get -y install htop &&
	apt-get -y install python3-pip &&
	apt-get -y install python-dev &&
	apt-get install libxml2-dev libxslt-dev &&
	apt-get install libjpeg-dev zlib1g-dev libpng12-dev

RUN pip install pandas-datareader \
	&& pip install tensorflow \
	&& pip install keras \
	&& pip install matplotlib \
	&& pip install numpy \
	&& pip install sklearn\
	&& pip install tqdm\
	&& pip install wordcloud \
	&& pip3 install newspaper3k


CMD /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks \
	--ip='*' --port=8888 --no-browser --allow-root
