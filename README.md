# Cost-Effective Visual Anomaly Detection using Unsupervised Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


![System Architecture](flow_visual.png) 
*Figure 1: End-to-end anomaly detection pipeline on low-cost hardware*

## 📌 Key Features
- **10-image training**: Requires only normal samples
- **90-second inference**: On Raspberry Pi 4B
- **0.95+ F1 score**: Competitive accuracy
- **$50 hardware**: Full deployment cost

## 🚀 Quick Start

### Hardware Requirements
| Component          | Specification       | Cost    |
|--------------------|--------------------|---------|
| Raspberry Pi       | 4B (4GB RAM)       | $35     |
| Camera Module      | 8MP Official       | $15     |
| Total              |                     | **$50** |

### Installation
```bash
git clone https://github.com/your-repo/low-cost-anomaly-detection.git
cd low-cost-anomaly-detection
pip install -r requirements.txt
```
## 📊 Performance Benchmarks

### Detection Accuracy (MVTec Dataset)
| Model       | Image AUROC | Pixel AUROC | F1 Macro | Inference Time (s) |
|-------------|------------|------------|----------|-------------------|
| **PaDiM**   | 0.98       | 0.96       | 0.95     | 45                |
| PatchCore   | 0.97       | 0.95       | 0.94     | 52                |
| CFA         | 0.95       | 0.93       | 0.92     | 38                |
| FastFlow    | 0.94       | 0.91       | 0.90     | 60                |

### Hardware Efficiency
| Device               | Power (W) | Cost (USD) | FPS  | Max Resolution |
|----------------------|----------|------------|------|----------------|
| Raspberry Pi 4B      | 5        | 35         | 2.1  | 1080p          |
| Intel NUC (i5)       | 28       | 300        | 12.5 | 4K             |
| Jetson Nano          | 10       | 99         | 4.3  | 4K             |
| **Our Solution**     | **3.5**  | **50**     | **3**| **1080p**      |

### Environmental Robustness
| Condition            | Performance Drop | Mitigation Strategy |
|----------------------|------------------|---------------------|
| Low Light (50 lux)   | -8%             | Auto-exposure       |
| Partial Occlusion    | -12%            | Multi-view fusion   |
| Background Clutter   | -5%             | ROI segmentation    |
| Angle Variation (±30°)| -7%            | Data augmentation   |

## Citation
@inproceedings{long2024leveraging,
  title={Leveraging unsupervised learning for cost-effective visual anomaly detection},
  author={Long, Yunbo and Ling, Zhengyang and Brook, Sam and McFarlane, Duncan and Brintrup, Alexandra},
  booktitle={IET Conference Proceedings CP885},
  volume={2024},
  number={11},
  pages={95--101},
  year={2024},
  organization={IET}
}
