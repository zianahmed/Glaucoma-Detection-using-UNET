# Glaucoma Detection in Retinal Fundus Images Using U-Net and Supervised/Unsupervised Machine Learning Algorithms

---

**Introduction:**
Glaucoma, a neuro-degenerative eye disease, poses a significant threat to vision globally, being the second largest cause of blindness. Early diagnosis is crucial to prevent irreversible blindness. This project aims to develop a system that can effectively detect glaucoma in retinal fundus images, circumventing the need for extensive equipment and specialized medical expertise.

---

**Step By Step Explanation:**

---

**Preprocessing:**
- Convert images to a uniform size and channel format for model compatibility.
- Resize images to (256,256,1) for consistency.
- Create folders for processed/resized images and masks.

---

**Preparing Data:**
- Standardize image sizes and channels.
- Convert images to grayscale.
- Separate optical cup and optical disk from masks.
- Prepare lists for images, optical cup, and optical disk.

---

**Model Building Functions:**
- Utilize U-Net architecture for glaucoma detection.
- Define functions for encoder and decoder blocks.
- Implement `conv_block`, `encoder_block`, and `decoder_block`.

---

**Building the U-Net Model:**
- Construct the U-Net architecture using encoder and decoder blocks.
- Input shape: `(256, 256, 1)` for binary segmentation mask.


---

**Model Compilation and Training:**
- Train the model on the first 20 images of the dataset.
- Use a batch size of 2 and 30 epochs.
- Set a minimum of 25 epochs for optimal results.

---

**Model Prediction and Post-processing:**
- Test the trained model on selected images.
- Generate segmentation results.

---

**Evaluation Metrics and Diagnosis:**
- Calculate Cup-to-Disc Ratio (CDR) for diagnosis.
- Determine likelihood of glaucoma based on CDR threshold (0.4).
- Compute evaluation metrics (accuracy, precision, recall, IoU) for segmentation.

---

**Readme File:**
- For detailed project report, refer to [project_report](Project_Report.pdf).

---

**Conclusion:**
This project demonstrates the potential of using U-Net and machine learning algorithms for glaucoma detection in retinal fundus images. By automating the diagnosis process, it can contribute significantly to early detection and prevention of vision loss due to glaucoma.
