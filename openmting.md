> openmting

sudo apt-get update
sudo apt-get install python3-pip
pip install --upgrade pip
pip install OpenNMT-tf[tensorflow]

# export tf lite
```bash
onmt-main --model_type TransformerBase \
    --config ~/Downloads/data.yml \
    --model_dir ~/Downloads/averaged-ende-ckpt500k \
    --checkpoint_path ~/Downloads/averaged-ende-ckpt500k/model.ckpt-500000 \
    export --format tflite \
    --output_dir ~/Downloads/tflite-out2
```


-- 1st averaging (just in case)
```bash
onmt-main \
    --config fr_ff_2/data-copy.yml --model_type TransformerBase --auto_config \
    average_checkpoints \
    --output_dir Users/Weebi/import \
    --max_count 2
```
-- then exporting
```bash
onmt-main --model_type TransformerBase  --config fr_ff_2/export-tf-lite.yml --model_dir /home/azureuser/cloudfiles/code/Users/Weebi/import/ --checkpoint_path /home/azureuser/cloudfiles/code/Users/Weebi/import/ckpt-16000 export --format tflite --output_dir Users/Weebi/output
```

# serving tensorflow
suivre le tuto, puis...
sudo snap install docker

?
sudo docker pull nvcr.io/nvidia/dli/dli-nano-ai:v2.0.1-r32.5.0
sudo apt install nvidia-cuda-toolkit

ls /anaconda/envs/azureml_py38/lib/python3.8/site-packages/numpy*
pip install trash-cli
