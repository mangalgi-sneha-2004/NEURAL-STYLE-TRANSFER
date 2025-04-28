# NEURAL-STYLE-TRANSFER
COMANY:CODTECH IT SOLUTIONS
NAME:MANGALGI SNEHA
INTERN-ID:CTO4WT53
DOMAIN:ARTIFICIAL INTELLIGENCE
DURATION:4 WEEKS
DESCRIPTION:
This implementation blends the content of one image (e.g., a photo) with the artistic style of another (e.g., a painting) using deep learning. The code is optimized for Google Colab with GPU support.

Key Components:
Image Processing Pipeline
Handles PNG/JPG uploads
Removes alpha channels (if present)
Resizes to 512x512 for consistent processing
Creates a text mask to preserve written content

VGG19 Model Setup:
Uses pre-trained VGG19 (ImageNet weights)
Extracts features from specific layers:
Style Layers: block1_conv1, block2_conv1 (capture brushstrokes/textures)
Content Layer: block3_conv3 (preserves structures)

Core Algorithms:
Gram Matrix Calculation: Measures style correlations between features
Loss Functions:
Style Loss (prioritized with weight 3e5)
Content Loss (weight 1e4 protects text)
Total Variation Loss (1e-6 reduces noise)

Optimization:
Adam optimizer (learning rate=15.0)
1500 iterations for quality results
Text protection mask prevents style over-write on text

Output:
Side-by-side comparison of input/output
High-quality PNG download (100% quality)
