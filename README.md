### Implementation of "Learning Multi-View Molecular Representations with Structured and Unstructured Knowledge"

**Warning: This repository is still under development. If you encounter any problem implementing our model, please open an issue or concat yz-luo22@mails.tsinghua.edu.cn** 

The model architecture is implemented in `open_biomed/models/multimodal/mvmol.py`.

The model checkpoint is currently available at [Google Drive](https://drive.google.com/drive/folders/1cd1EZTuyNOCLRt2Vr0JgXh3kWm9f2qwU?usp=sharing). Install the checkpoint and put it under `./ckpts/fusion_ckpts/mvmol`.

For evaluating MV-Mol on downstream tasks, run the following scripts:

```bash
# cross-modal retrieval on PCDes
bash scripts/multimodal/mtr/run_pcdes.sh mvmol [device id]

# molecule captioning on CheBI-20
bash scripts/multimodal/molcap/train.sh mvmol [device id]

# text-based molecule generation on CheBI-20
bash scripts/multimodal/text2smi/train.sh mvmol [device id]

# We will be incorporating the molecular property prediction task soon
```

