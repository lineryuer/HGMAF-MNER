📁 项目目录结构
HGMAF-MNER/
│
├── README.md                          # 项目说明文档
├── LICENSE                            # MIT许可证
├── requirements.txt                   # Python依赖
├── setup.py                          # 安装配置
│
├── config/                           # 配置文件
│   ├── config.yaml                   # 主配置文件
│   └── model_config.py               # 模型配置类
│
├── data/                             # 数据目录
│   ├── twitter2015/                  # Twitter2015数据集
│   │   ├── train.txt
│   │   ├── valid.txt
│   │   ├── test.txt
│   │   ├── images/                   # 原始图像
│   │   └── generated_images/         # 生成图像
│   │       ├── train/
│   │       ├── valid/
│   │       └── test/
│   │
│   └── twitter2017/                  # Twitter2017数据集
│       └── ...
│
├── preprocessing/                    # 数据预处理
│   ├── __init__.py
│   ├── emotion_prompt.py            # 情感分析
│   ├── entity_prompt.py             # 实体提取
│   ├── entity_interpretation_prompt.py  # 实体解释
│   ├── generated_entity_image.py    # 实体图像生成
│   ├── generated_sentences_image.py # 句子图像生成
│   └── data_augmentation.py         # 数据增强
│
├── models/                          # 模型定义
│   ├── __init__.py
│   ├── mner_model.py               # 主模型
│   ├── text_encoder.py             # 文本编码器
│   ├── image_encoder.py            # 图像编码器
│   ├── fusion_layer.py             # 融合层
│   ├── attention.py                # 注意力机制
│   └── crf.py                      # CRF层
│
├── datasets/                        # 数据集加载
│   ├── __init__.py
│   ├── mner_dataset.py             # MNER数据集类
│   └── data_collator.py            # 数据整理器
│
├── trainers/                        # 训练器
│   ├── __init__.py
│   ├── mner_trainer.py             # 训练器类
│   └── callbacks.py                # 回调函数
│
├── inference/                       # 推理
│   ├── __init__.py
│   ├── predictor.py                # 预测器
│   └── ensemble.py                 # 集成模型
│
├── utils/                           # 工具函数
│   ├── __init__.py
│   ├── metrics.py                  # 评估指标
│   ├── visualizer.py               # 可视化
│   ├── logger.py                   # 日志记录
│   └── io_utils.py                 # IO工具
│
├── scripts/                         # 运行脚本
│   ├── preprocess_data.sh          # 数据预处理脚本
│   ├── train.sh                    # 训练脚本
│   ├── evaluate.sh                 # 评估脚本
│   └── inference.sh                # 推理脚本
│
├── notebooks/                       # Jupyter notebooks
│   ├── data_exploration.ipynb      # 数据探索
│   ├── model_analysis.ipynb        # 模型分析
│   └── error_analysis.ipynb        # 错误分析
│
├── outputs/                         # 输出目录
│   ├── checkpoints/                # 模型检查点
│   ├── logs/                       # 训练日志
│   ├── visualizations/             # 可视化结果
│   └── predictions/                # 预测结果
│
├── tests/                          # 单元测试
│   ├── __init__.py
│   ├── test_model.py
│   ├── test_dataset.py
│   └── test_trainer.py
│
├── train.py                        # 训练入口
├── evaluate.py                     # 评估入口
├── predict.py                      # 推理入口
└── demo.py                         # 演示程序

📄 requirements.txt (更新版)
txt# Deep Learning Frameworks
torch>=2.0.0
torchvision>=0.15.0
transformers>=4.39.3
pytorch-crf>=0.7.2

# OpenAI API
openai==1.16.1

# Image Processing
Pillow>=10.0.0
opencv-python>=4.8.0

# Diffusion Models
diffusers>=0.25.0
accelerate>=0.20.0
safetensors>=0.3.0

# Data Processing
numpy>=1.24.0
pandas>=2.0.0
scikit-learn>=1.3.0

# NLP Tools
seqeval>=1.2.2
nltk>=3.8.0

# Visualization
matplotlib>=3.7.0
seaborn>=0.12.0
tensorboardX>=2.6
wandb>=0.15.0

# Utilities
tqdm>=4.65.0
pyyaml>=6.0
python-dotenv>=1.0.0

# Testing
pytest>=7.4.0
pytest-cov>=4.1.0

# Code Quality
black>=23.0.0
flake8>=6.0.0
isort>=5.12.0
