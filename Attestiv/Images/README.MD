**Report on Image Authenticity Testing Using Attestiv**

**Introduction**

This report summarizes the results of testing five images with Attestiv’s image authenticity tool. The goal was to examine the usability of the tool in detecting tampered or AI-generated images, particularly focusing on whether the tool could accurately identify authentic images and images generated or manipulated by AI. This test is not meant to judge the accuracy of the tool but rather its accessibility and ease of use. Despite some false positives and other limitations, the tool, even in its free-tier early development stage, holds promise for potential use in journalistic verification workflows.

For reference, all original media files and test results are available in the GitHub repository: [https://github.com/wsaqaf/blockchainai/tree/main/Attestiv](https://github.com/wsaqaf/blockchainai/tree/main/Attestiv).

---

### Summary of Test Results

| Image | Description | Tamper Score | Interpretation | Notes |
|-------|-------------|--------------|----------------|-------|
| **test1-f.jpg** | AI-generated image | **100** | High suspicion due to editing traces and provenance | Origin detected as web-sourced; software traces found |
| **test2-f.png** | AI-generated image | **31** | Low suspicion due to small image size affecting analysis | Quality and "photo of photo" analyses were skipped |
| **test3-r.jpg** | Real photo | **100** | High suspicion, likely due to screen capture detection and noise | Detected as a photo of a screen; generative AI probability flagged at 0.93 |
| **test4-r.jpg** | Real photo | **100** | High suspicion, with metadata anomalies detected | Unfamiliar ICC color profile and provenance from editing software |
| **test5-f.jpg** | AI-generated image photographed from a screen | **100** | High suspicion, correctly identified as a "photo of a screen" | Metadata indicates editing; software traces found |

---

### Detailed Analysis of Each Image

#### Image 1: test1-f.jpg (AI-generated)
- **Tamper Score**: 100
- **Notes**: High suspicion due to provenance and metadata indicating editing. Reverse search suggests the image may have originated from the web.
- **Implication**: Attestiv accurately flagged this AI-generated image with high suspicion based on editing traces.
  
#### Image 2: test2-f.png (AI-generated, small size)
- **Tamper Score**: 31
- **Notes**: Analysis partially skipped due to the small image size, affecting quality and "photo of photo" detection. Despite being AI-generated, it received a low tamper score.
- **Implication**: Size limitations can impact Attestiv’s detection accuracy; thus, high-resolution images are recommended for complete analysis.

#### Image 3: test3-r.jpg (Real)
- **Tamper Score**: 100
- **Notes**: High suspicion rating despite being real, likely due to detected screen capture and generative AI probability of 0.93. Also flagged for unfamiliar ICC color profile and noise.
- **Implication**: Real images captured from screens may trigger false positives, highlighting the need for improved differentiation of screen-captured content.

#### Image 4: test4-r.jpg (Real)
- **Tamper Score**: 100
- **Notes**: High suspicion, attributed to unusual ICC color profile and metadata suggesting editing software traces. Reverse search suggests possible web origin.
- **Implication**: Real photos with specific metadata profiles or color configurations may be flagged as tampered, indicating limitations in differentiating authentic metadata from edited content.

#### Image 5: test5-f.jpg (AI-generated, photographed from a screen)
- **Tamper Score**: 100
- **Notes**: Correctly identified as a photo of a screen. Metadata analysis detected multiple dimensions, suggesting image scaling, and traces of editing software were found.
- **Implication**: The tool successfully identified this image as a screen photo, showing its capability in detecting photos of AI-generated content.

---

### Conclusion

This test demonstrates Attestiv’s potential in detecting manipulated or AI-generated images based on metadata, provenance, and structural inconsistencies. However, there are notable limitations, such as false positives on real images, particularly those captured from screens or with complex metadata configurations. The tool’s partial analysis of small images also highlights the importance of high-resolution input.

For journalistic applications, Attestiv could become a valuable tool with further refinement to reduce false positives, especially on authentic images. Enhanced capability in distinguishing real images from AI-generated ones and improved handling of screen-captured content could significantly increase its usability in verifying media authenticity.
