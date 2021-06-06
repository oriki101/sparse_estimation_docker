FROM jupyter/datascience-notebook


#必要なパッケージ
RUN pip install terminator japanize_matplotlib rpy2


# #行数表示 windowsで実行可能 ubuntuでは実行不可を確認(文字コードの可能性大)
# RUN mkdir -p ~/.jupyter/lab/user-settings/@jupyterlab/notebook-extension/
# RUN echo '\n\
# { \n\
#     "codeCellConfig": { \n\
#         "lineNumbers": true \n\
#     } \n\
# } \n\
# ' > ~/.jupyter/lab/user-settings/@jupyterlab/notebook-extension/tracker.jupyterlab-settings

RUN git clone https://github.com/bbalasub1/glmnet_python.git &&\
    cd glmnet_python &&\
    python setup.py install

# ENV NB_PREFIX /
# CMD ["sh","-c", "jupyter lab --notebook-dir=/home/jovyan --ip=0.0.0.0 --no-browser --allow-root --port=8888 --NotebookApp.token='' --NotebookApp.password='' --NotebookApp.allow_origin='*' --NotebookApp.base_url=${NB_PREFIX}"]