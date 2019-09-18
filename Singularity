Bootstrap: docker
From: continuumio/miniconda2

%labels
   AUTHOR s.schmeier@protonmail.com

%environment
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This sets global environment variables for anything run within the container
  export PATH="/opt/conda/bin:$PATH"
  unset CONDA_DEFAULT_ENV
  export ANACONDA_HOME=/opt/conda
  #export LANG=en_US.UTF-8
  #export LC_ALL=en_US.UTF-8
  #export LANGUAGE=en_US.UTF-8

%post
   # CONDA
   export PATH=/opt/conda/bin:$PATH
   #conda update --yes -q conda 
   echo "We add conda channels."
   conda config --add channels defaults
   conda config --add channels bioconda
   conda config --add channels conda-forge
   conda config --add channels aroth85
   conda update -n base -c defaults conda
   echo "We install tools."
   conda install --yes opossum platypus-variant
   conda clean --index-cache --tarballs --packages --yes
   conda list > /conda.txt
   touch /`date -u -Iseconds`

