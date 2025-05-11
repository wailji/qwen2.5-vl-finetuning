# Qwen2.5-VL Fine-Tuning Interface

This repository provides an interactive notebook for fine-tuning the **Qwen2.5-VL** vision-language model.  
It is designed for experimentation and research with multimodal models using the Hugging Face Transformers library.

First run the commands : 
```bash
git clone https://github.com/wailji/qwen2.5-vl-finetuning
cd qwen2.5-vl-finetuning/
```
# Dataset

COCO 2017 Dataset was used in this fine-tuning project. Run the following commands to download it, and to download the messages used for training in the `llava_v1_5_mix665k.json` file:
```bash
wget http://images.cocodataset.org/zips/train2017.zip
mkdir -p ./coco/
unzip train2017.zip -d ./coco/
wget -P coco/ https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K/resolve/main/llava_v1_5_mix665k.json
```

# Environment

To proceed with the rest, we first need to create the virtual env `qwen_env`.
For MacOS/Linux users : 
```bash
python -m venv qwen_env
source qwen_env/bin/activate
```
for Windows users : 
```bash
python -m venv qwen_env
qwen_env\Scripts\activate
```
Then install the dependencies : 
```bash
pip install -r requirements.txt
# Add the environment to Jupyter as a new kernel
python -m ipykernel install --user --name=qwen_env --display-name "qwen_env"
```

After this step everything is on the notebook !