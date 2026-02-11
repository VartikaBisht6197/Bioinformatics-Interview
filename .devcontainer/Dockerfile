FROM mambaorg/micromamba:1.5.1

# Copy environment file
COPY Bioinformatics_Interview.yml /tmp/Bioinformatics_Interview.yml

# Install everything into base env
RUN micromamba install -y -f /tmp/Bioinformatics_Interview.yml -n base && \
    micromamba clean --all -f -y

# Initialize micromamba for all future shells
SHELL ["bash", "-c"]
RUN micromamba shell init -s bash -p /opt/conda