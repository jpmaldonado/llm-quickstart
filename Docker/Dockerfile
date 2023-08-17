FROM jupyter/minimal-notebook
LABEL description="Demo Container LLM"

ENV GIT_LFS_SKIP_SMUDGE=1

# Start as root
USER root

# Update packages
RUN apt-get update --fix-missing \
    && apt-get -y upgrade \
    && apt-get -y dist-upgrade	\
	&& apt-get -y install cmake protobuf-compiler \
	&& apt install -y libprotobuf-dev protobuf-compiler \ 
	&& apt install -y build-essential \
	&& apt install -y software-properties-common \
	&& add-apt-repository ppa:ubuntu-toolchain-r/test \
	&& apt install -y gcc-9 g++-9


# Install dependencies
RUN apt-get install --no-install-recommends --no-install-suggests -y \
    git

# install dependencies
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

COPY data /home/jovyan/work
COPY notebooks /home/jovyan/work

# Get spital/gpt2-small-czech-cs model
RUN git clone https://huggingface.co/spital/gpt2-small-czech-cs

# Clean packages and caches
RUN apt-get --purge -y autoremove git \
    && rm -rf /var/lib/apt/lists/* /var/cache/apt/archives/* \
    && rm -rvf /home/${ANACONDA_PATH}/.cache/yarn \
    && fix-permissions ${HOME} \
    && fix-permissions ${ANACONDA_PATH}