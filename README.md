# PyTorch Lightning Meetup Demo

A complete, production-ready template demonstrating PyTorch Lightning best practices with CIFAR-10 classification.

## 🎯 Key Features Demonstrated

1. **LightningModule** - Organizing PyTorch code into research components
2. **Trainer** - Automated training with best practices
3. **LightningDataModule** - Reproducible data handling
4. **Fabric** - Fine-grained control for custom training loops
5. **Config Management** - YAML-based configuration
6. **Logging** - TensorBoard & WandB integration
7. **Callbacks** - Checkpointing, early stopping, LR monitoring
8. **Reproducibility** - Full seed control and deterministic training

## 📁 Project Structure
lightning-meetup-demo/
├── config/ # YAML configuration files
├── data/ # LightningDataModule for CIFAR-10
├── models/ # PyTorch models + LightningModules
├── training/ # Training scripts (Lightning & Fabric)
└── notebooks/ # Interactive examples

text

## 🚀 Quick Start

### Installation
```bash
pip install -r requirements.txt
Basic Training
bash
python training/train.py
Try Different Hardware Configurations
Edit config/defaults.yaml:

yaml
trainer:
  accelerator: "gpu"  # or "cpu", "tpu"
  devices: 2          # number of devices
  precision: "16-mixed"  # mixed precision training
Debug Mode (Fast Iteration)
bash
# Edit config/defaults.yaml
trainer:
  fast_dev_run: true  # Run 1 batch only
  limit_train_batches: 0.1  # Train on 10% of data
