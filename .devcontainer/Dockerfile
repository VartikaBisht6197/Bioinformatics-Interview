FROM mambaorg/micromamba:1.5.1

COPY environment.yml /tmp/environment.yml

RUN micromamba install -y -n base -f /tmp/environment.yml && \
    micromamba clean --all --yes

# Ensure bash is login shell so conda activates
SHELL ["/bin/bash", "-l", "-c"]