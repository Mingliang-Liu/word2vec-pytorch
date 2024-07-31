conda create -n word2vec python=3.8 -y
conda activate word2vec

nvidia-smi
my cuda version:11.7

wget https://download.pytorch.org/whl/cu117/torch-1.13.0%2Bcu117-cp38-cp38-linux_x86_64.whl
pip3 install torch-1.13.0+cu117-cp38-cp38-linux_x86_64.whl
python -m pip install git+https://github.com/leifdenby/nb_black/#egg=nb_black
pip3 install -r requirements.txt

```
python3 train.py --config config.yaml
```

ERROR:
requests.exceptions.HTTPError: 403 Client Error: Forbidden for url: https://s3.amazonaws.com/research.metamind.io/wikitext/wikitext-2-v1.zip

download https://modelscope-open.oss-cn-hangzhou.aliyuncs.com/wikitext/wikitext-2-v1.zip
=> data/datasets/WikiText2/wikitext-2-v1.zip