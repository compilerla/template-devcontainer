FROM python:3.10

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1 \
    USER=compiler

# create non-root $USER and home directory
RUN useradd --create-home --shell /bin/bash $USER && \
    chown -R $USER /home/$USER

# switch to $USER
USER $USER

# enter src directory
WORKDIR /home/$USER/src

# update PATH for local pip installs
ENV PATH "$PATH:/home/$USER/.local/bin"

# upgrade pip
RUN python -m pip install --upgrade pip

# install devcontainer requirements
COPY .devcontainer/requirements.txt .devcontainer/requirements.txt
RUN pip install --no-cache-dir -r .devcontainer/requirements.txt

# install docs requirements
COPY docs/requirements.txt docs/requirements.txt
RUN pip install --no-cache-dir -r docs/requirements.txt

# install pre-commit environments in throwaway Git repository
# https://stackoverflow.com/a/68758943
COPY .pre-commit-config.yaml .
RUN git init . && \
    pre-commit install-hooks && \
    rm -rf .git
