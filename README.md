# AI Image Caption Recommendation System
This project builds an AI-powered Image Caption Recommendation System using CLIP (Contrastive Language–Image Pretraining) and Python. Unlike caption generators that describe an image, this system recommends a relevant caption from a pre-defined list—making it ideal for social media posts like Instagram, where you want meaningful yet catchy captions.

**Overview**
Social media platforms often lack intelligent caption suggestion tools. Most LLMs tend to describe the image rather than suggest a user-friendly caption. This project solves that gap using a retrieval-based approach with CLIP to match visual content to the best-fitting caption from a large candidate pool.

**How It Works**

**1. Image Preprocessing**
The input image is preprocessed using CLIPProcessor from Hugging Face.

**2. Image Embedding**
We extract a high-dimensional vector for the image using the CLIPModel.

**3. Caption Embedding**
Each caption from the list is embedded using the same CLIP text model.

**4. Similarity Matching**
Cosine similarity is computed between the image vector and all caption vectors.

**5. Recommendation**
Captions are ranked based on similarity scores, and the top-k captions are returned.

**Sample Output**

Top 5 Best Captions:
1. Trees, Travel and Tea! (Similarity: 0.2272)
2. A moment to enjoy. (Similarity: 0.2268)
3. A moment to remember. (Similarity: 0.2204)
4. A moment of bliss. (Similarity: 0.2165)
5. The joy of discovery, the warmth of connection. (Similarity: 0.2159)
