📸 VGG16 + Metadata for Multi-class Image Classification

This project demonstrates how to build an interpretable, data-centric AI model for multi-class image classification using:
✅ Transfer learning (VGG16)
✅ Fine-tuning
✅ Metadata features (captions TF-IDF or interpretable image features)
✅ LIME explainability

✨ Project Goals

Build an end-to-end model using transfer learning with VGG16.

Add custom layers on top that incorporate metadata (photo captions or interpretable image features).

Iterate and improve the model using data-centric AI.

Ensure the final model is interpretable and suitable for deployment.

🗂️ Dataset
Multi-class image classification dataset: 5 classes → drink, food, inside, menu, outside.

Structure:

bash
Copy
Edit
data_sorted/
    train/
        drink/
        food/
        inside/
        menu/
        outside/
    val/
    test/
Metadata:

photo_id

business_id

Caption

label

🏗️ Models
Iteration 1
VGG16 + Metadata (caption TF-IDF)

Fully fine-tuned.

Iteration 2
VGG16 + Metadata → replaced caption TF-IDF with interpretable image features:

Mean R, G, B values

Brightness

Aspect ratio

Fully fine-tuned.

⚙️ Results
Model	Data Type	Accuracy	AUC
VGG16 + metadata (TF-IDF)	Validation	~0.90	~0.99
VGG16 + metadata (image features)	Validation	~0.89	~0.98
VGG16 + metadata (image features)	Test	0.90	0.99

✅ Final model selected: VGG16 + interpretable image-based metadata → deployable without captions.

🔍 Explainability
LIME used to explain model predictions on individual images and global behavior.

Helps visualize which parts of the image are most influential for each class.



💡 Key Takeaways
Fine-tuning VGG16 with metadata significantly improves accuracy.

Interpretable image-based features are a practical alternative to captions → no need for text input at deployment.

LIME provides valuable insights into model decisions → improving trust.

