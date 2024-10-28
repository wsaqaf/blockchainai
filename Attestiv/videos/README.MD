
## Attestiv testing:
Ten videos were selected for testing based on the statement provided by Attestiv on their website at [https://attestiv.com/deepfake-video-detection-software/](https://attestiv.com/deepfake-video-detection-software/):

> With Attestiv, you can:
> 
> -   Prevent the spread of disinformation.
> -   Protect against elaborate phishing and security threats.
> -   Avoid potential fraud and losses from bad external or client data.
> -   Mitigate legal and compliance concerns.

**Report on Video Authenticity Testing Using Attestiv**

**Introduction**

This report presents the results of a video authenticity testing exercise conducted using the Attestiv tool. The objective was not to evaluate the tool’s quality in terms of accuracy but to assess its usability, accessibility, and potential application in journalistic practices. While Attestiv displayed some false positives and errors, it is important to acknowledge that this is the free-tier version, which may be in early development stages. Despite these limitations, the tool shows high potential to become an invaluable asset for journalists if future versions achieve higher accuracy and reliability.

For reference, all original media files (videos) and test screenshots are available in the GitHub repository: [https://github.com/wsaqaf/blockchainai/tree/main/Attestiv](https://github.com/wsaqaf/blockchainai/tree/main/Attestiv).

---

### Summary of Test Results

| Video | Description | Score | Interpretation | Link to Original Media |
|-------|-------------|-------|----------------|------------------------|
| **Video 1** | AI-generated, black-and-white video of Egyptians building pyramids | **0.3501** | Moderate suspicion due to AI-generation markers, minor fluctuations in score | [YouTube](https://www.youtube.com/shorts/688Op8oWvUM) |
| **Video 2** | AI-generated lip-syncing video using D-ID, with detectable lip-sync modifications | **0.2333** | Low suspicion; tool detects subtle lip replacement but maintains low suspicion overall | [D-ID Studio](https://studio.d-id.com/share?id=f201022ca36a1bbb480fcf78011a8a0f&utm_source=copy) |
| **Video 3** | AI-generated night-time cliff scenery from Leonardo platform | **0.3383** | Moderate suspicion due to generated markers, stable score | [Leonardo](https://cdn.leonardo.ai/users/cf239304-deb5-4ad4-ad74-b74ba38be85c/generations/27c0aa8a-3354-4964-81da-fdd6d43055fc/27c0aa8a-3354-4964-81da-fdd6d43055fc.mp4) |
| **Video 4** | AI-enhanced video with Tom Cruise face replacement | **0.4168** | Moderate suspicion, tool accurately detects face replacement | [YouTube](https://www.youtube.com/watch?v=iyiOVUbsPcM) |
| **Video 5** | Real stock video of a city view from a hotel, error encountered during upload | - | Internal server error prevented analysis | [YouTube](https://www.youtube.com/watch?v=CE0Q904gtMI) |
| **Video 6** | Real video of a city street view from a high floor, taken by mobile phone | **0.4038** | Slightly above moderate suspicion, possibly due to compression artifacts | GitHub repo |
| **Video 7** | Original unaltered video used in the lip-syncing exercise, lips fully closed | **0.2471** | Low suspicion; accurately detected as unaltered despite minor markers | GitHub repo |
| **Video 8** | Real drone footage of a river in a green valley | **0.5891** | Moderate to high suspicion, false positives likely due to natural scenery | [Vecteezy](https://www.vecteezy.com/video/38999617-green-simple-nature-slomo-view) |
| **Video 9** | Stock drone footage over New York at night, error encountered during processing | - | Persistent processing error prevented analysis | [YouTube](https://www.youtube.com/watch?v=TEjHDF9QXTY) |
| **Video 10** | Real video of impersonator Evan Ferrante imitating Tom Cruise without AI | **0.6327** | High suspicion due to impersonation style, false positives for face replacement markers | [YouTube](https://www.youtube.com/watch?v=6dVzXwmysdg) |

---

### Detailed Analysis of Each Video

#### Video 1: AI-generated Historical Scene
- **Suspicion Score**: 0.3501
- **Notes**: Minor AI-generation markers were detected, resulting in a moderate suspicion score, consistent across the timeline.
- **Implication**: Indicates that Attestiv can identify AI generation even in stylized, historical settings.
- **Link**: [YouTube](https://www.youtube.com/shorts/688Op8oWvUM)

#### Video 2: AI Lip-syncing Exercise
- **Suspicion Score**: 0.2333
- **Notes**: Lip replacement detected but rated low in suspicion, showing the tool’s ability to catch subtle lip-sync adjustments.
- **Implication**: Attestiv can detect AI lip-syncing but maintains a low suspicion level for minimally altered content.
- **Link**: [D-ID Studio](https://studio.d-id.com/share?id=f201022ca36a1bbb480fcf78011a8a0f&utm_source=copy)

#### Video 3: Night-time AI-generated Cliff Scene
- **Suspicion Score**: 0.3383
- **Notes**: Some markers flagged as generated content, but overall score is moderately low, reflecting consistency.
- **Implication**: Shows potential for handling subtle AI-generation cues in night-time natural scenery.
- **Link**: [Leonardo](https://cdn.leonardo.ai/users/cf239304-deb5-4ad4-ad74-b74ba38be85c/generations/27c0aa8a-3354-4964-81da-fdd6d43055fc/27c0aa8a-3354-4964-81da-fdd6d43055fc.mp4)

#### Video 4: Deepfake-style Tom Cruise Face Replacement
- **Suspicion Score**: 0.4168
- **Notes**: The tool effectively detected face and lip replacements, showing accurate face swap identification.
- **Implication**: Attestiv is capable of flagging AI face replacement, making it useful for deepfake detection.
- **Link**: [YouTube](https://www.youtube.com/watch?v=iyiOVUbsPcM)

#### Video 5: Real Video from Hotel Room, Error Encountered
- **Error**: Internal server error
- **Implication**: Persistent error suggests potential tool limitations with certain video formats or content.

#### Video 6: Real City Street View
- **Suspicion Score**: 0.4038
- **Notes**: Slightly above moderate suspicion, possibly due to natural video artifacts.
- **Implication**: Demonstrates that real footage can be flagged as suspicious, especially with complex lighting.
- **Link**: GitHub repo

#### Video 7: Unaltered Original Video
- **Suspicion Score**: 0.2471
- **Notes**: Low suspicion rating, correctly detected as genuine, despite minor markers likely from natural video noise.
- **Implication**: Confirms that Attestiv can recognize unaltered videos accurately.
- **Link**: GitHub repo

#### Video 8: Real Drone Footage of Nature
- **Suspicion Score**: 0.5891
- **Notes**: Moderate to high suspicion, with several false positives likely due to natural scenery complexity.
- **Implication**: Attestiv may overestimate suspicion in high-detail nature videos.
- **Link**: [Vecteezy](https://www.vecteezy.com/video/38999617-green-simple-nature-slomo-view)

#### Video 9: Stock Drone Footage of NYC, Error Encountered
- **Error**: Processing error repeated across attempts
- **Implication**: Highlights potential limitations or compatibility issues with nighttime urban footage.
- **Link**: [YouTube](https://www.youtube.com/watch?v=TEjHDF9QXTY)

#### Video 10: Real Video of Tom Cruise Impersonator
- **Suspicion Score**: 0.6327
- **Notes**: High suspicion rating likely due to realistic impersonation style, with false positives for face replacement.
- **Implication**: Suggests limitations in differentiating genuine impersonations from manipulated content, underscoring the need for human review.
- **Link**: [YouTube](https://www.youtube.com/watch?v=6dVzXwmysdg)

---

### Conclusion

This test provides insights into Attestiv’s usability and limitations when applied to various types of video content, both genuine and AI-modified. The tool effectively identifies AI-driven manipulations in certain contexts, such as face swaps, but demonstrates limitations in processing high-detail or complex natural scenery, leading to false positives in real footage. Additionally, repeated errors with certain uploads highlight potential compatibility issues.

Despite these findings, Attestiv shows promising potential for journalistic use, particularly in detecting deepfake-style alterations. Improvements in processing stability and accuracy could make it an essential tool for media verification in the future, especially as it evolves beyond its current developmental stage.
