# 🚀 Ultra-Optimized Real-ESRGAN Image Upscaler

A **high-performance, realistic image super-resolution** Python toolkit built on **Real-ESRGAN** and **GFPGAN**.  
Supports large images, face enhancement, FP16 acceleration, tiling, and batch processing.

---

## 🌟 Features

- Upscale images up to 4x or 2x with multiple models
- Face enhancement using GFPGAN
- Automatic tiling for huge images (>10MP)
- FP16 support for faster GPU inference
- Batch processing with progress tracking
- Subtle post-processing for photo-realism
- Supports PNG, JPG, WebP output formats

---

## ⚡ Installation

```bash
# Install PyTorch (CUDA 11.8)
pip install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# Install Real-ESRGAN and dependencies
pip install realesrgan basicsr gfpgan facexlib opencv-python-headless Pillow numpy

📥 Download Models

The following models are used (auto-download included in script):

RealESRGAN_x4plus – General photos, high-quality 4x upscaling

RealESRGAN_x2plus – Subtle 2x upscaling

RealESRNet_x4plus – Sharper 4x upscaling

GFPGANv1.3 – Face enhancement
```
---
🎯 Configuration Presets: (for v2)
```bash
# For portraits with faces (BEST QUALITY)
upscaler_max.enhance('portrait.jpg')

# For general photos (BALANCED)
upscaler_balanced.enhance('photo.jpg')

# For huge images >10MP (MEMORY EFFICIENT)
upscaler_huge.enhance('huge_image.jpg')

# For subtle enhancement (NATURAL 2x)
upscaler_2x.enhance('image.jpg')
```
✨ (For ImageResolution): upscale_image('your_image.jpg', 'upscaled_your_image.jpg')

---
💡 Tips

Start with upscaler_balanced for best speed/quality trade-off

Use upscaler_max for portraits/products where detail matters

For very large images, use tile_size=256 to avoid GPU memory issues

Adjust denoise_strength (0.0–1.0) for smoother face enhancement

---
📄 License

This project is based on Real-ESRGAN
 and GFPGAN
. Check their licenses for usage details.
