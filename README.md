# FabNet-2.5k
FabNet-2.5k is a curated dataset consisting of 2,500 high-quality images of fabric textures. This dataset was created to support research in computer vision, specifically for the task of automated textile material identification.

It is designed for training Deep Learning models (such as CNNs or Vision Transformers) to distinguish between natural and synthetic fibers.

#    📂 Dataset Structure

The dataset is organized into a standard directory structure compatible with torchvision.datasets.ImageFolder and other standard dataloaders.

Total Images: ~2,500
Classes: 5 distinct fabric types
Format: JPG

Directory Tree

```
FabNet-2.5k/
├── train/                  # Training set
│   ├── Cotton/
│   ├── Linen/
│   ├── Polyester/
│   ├── Silk/
│   └── Wool/
└── val/                    # Validation set
    ├── Cotton/
    ├── Linen/
    ├── Polyester/
    ├── Silk/
    └── Wool/
```

# 🧶 Classes

The dataset includes the following 5 texture categories:

    Cotton: Natural fiber with a soft, breathable texture.

    Linen: Natural fiber made from flax, distinct weave pattern.

    Polyester: Synthetic fiber, often smooth or uniform.

    Silk: Natural protein fiber, high sheen/gloss.

    Wool: Natural animal fiber, fuzzy or thick texture.



# 🚀 Quick Start

Download Dataset:
Google Drive - https://drive.google.com/drive/folders/1_B5v7d_Qrmm0HJETYfKkbnq78ygijEK9?usp=drive_link

You can easily load this dataset using PyTorch:

```
import torch
from torchvision import datasets, transforms

# Define transformations
transform = transforms.Compose([
    transforms.Resize((224, 224)),
    transforms.ToTensor(),
])

# Load Data
train_data = datasets.ImageFolder(root='FabNet-2.5k/train', transform=transform)
val_data = datasets.ImageFolder(root='FabNet-2.5k/val', transform=transform)

print(f"Classes: {train_data.classes}")
# Output: ['Cotton', 'Linen', 'Polyester', 'Silk', 'Wool']
```

# 📝 Citation

If you use this dataset in your research or project, please cite it as follows:

```
@misc{FabNet2025,
  author = {Isadchenko Yevhen},
  title = {FabNet-2.5k: A Fabric Classification Dataset},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/kolon3d-prog/FabNet-2.5k}}
}
```

# 📜 License

This dataset is licensed under the Creative Commons Attribution 4.0 International license.
