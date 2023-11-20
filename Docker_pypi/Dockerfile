FROM python:3

COPY . /bevpo
WORKDIR /bevpo

# install twine and build
RUN python3 -m pip install --upgrade twine build

# build
RUN python3 -m build


# First upload, then download and install to see if all works
CMD python3 -m twine upload --config-file .pypirc dist/* \
    && python3 -m pip install bevpo
