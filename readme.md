# LivePortrait Optimization

## 🎯 Project Overview

This repository presents an optimized implementation of the LivePortrait model, focusing on reducing inference time while maintaining output quality. The optimization efforts achieved a **99.9% speed improvement** (from 1.0951s to 0.0008s) and a **1314.2x speedup factor**, demonstrating production-ready performance tuning techniques.

## 📁 Repository Structure

```
├── LivePortrait_Optimization_Code.ipynb      # Main optimization notebook
├── LivePortrait_Optimization_Summary.md      # Optimization summary and findings
├── README.md                                 # Project overview and instructions
```

## 🚀 Quick Start

### Option 1: Google Colab (Recommended)
1. Open the notebook: [LivePortrait Optimization Colab](https://colab.research.google.com/drive/1a7G7rJOleP0sF69ggK_5AGCfymB_CAIp#scrollTo=0laHlP3nzXgs)
2. Enable GPU runtime: `Runtime → Change runtime type → GPU`
3. Run all cells sequentially to observe baseline and optimized performance.

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/marupakasrija/LivePotrait_Optimization.git
cd LivePotrait_Optimization

# Install dependencies
pip install torch torchvision torchaudio
pip install opencv-python-headless matplotlib seaborn
pip install psutil GPUtil pillow
```

## 📈 Performance Overview

| Metric             | Baseline  | Optimized | Improvement      |
|--------------------|-----------|-----------|------------------|
| Inference Time     | 1.0951 s  | 0.0008 s  | 99.9% faster     |
| Speedup Factor     | 1.0x      | 1314.2x    | 1314.2x gain      |
| Memory Usage       | 320 MB    | 387 MB    | +20.9% (Managed) |
| Output Quality     | ✅        | ✅        | No degradation   |

## 🔍 Optimization Techniques Used

- **FP16 Quantization**: Faster inference with reduced precision
- **No Gradient Calculation**: Uses `torch.no_grad()` for inference
- **cuDNN Benchmarking**: Enables consistent optimization for fixed input sizes
- **Mixed Precision (AMP)**: Automatically improves memory and speed
- **torch.compile** (PyTorch 2.0): Graph-level optimizations with fallback support

## 📊 Notebook Structure

1. **Setup**: Environment, imports, and GPU configuration
2. **Baseline**: Original LivePortrait model with inference profiling
3. **Optimized Version**: Introduced multiple speedup techniques
4. **Analysis**: Warmup runs, performance charting, and memory tracking
5. **Conclusions**: Summary of results and future recommendations

## 💡 Highlights

- ✅ Production-safe optimizations with fallback logic
- ✅ Visualized benchmarking and profiling results
- ✅ Scalability insights and hardware efficiency evaluation

## 📝 Notes

- Testing performed on Tesla T4 GPU in Colab Pro
- PyTorch 2.0+ is required for `torch.compile`
- Results include warmup and cold-start inference comparison

## 🧑‍💻 Author

**Name**: Marupaka Srija Reddy  
**Submitted to**: IntellifAI Labs (ML Role)  
**Date**: 04-06-2025

## 📄 License

This work is created for educational evaluation purposes as part of an assignment. LivePortrait original source follows its respective license.

---

**🚀 Final Outcome**: Optimized LivePortrait model with 99.8% reduced inference time and robust code engineering practices.
