**Report on Document Fingerprinting and Authentication for Journalistic Use Using OriginStamp**

**Introduction**

This report documents a test conducted with OriginStamp’s blockchain-based timestamping service, which anchors data to public blockchains, creating tamper-proof timestamps that verify a document’s existence at a specific time. OriginStamp's timestamping is highly relevant for journalism, as it provides a secure method to protect major media content and sensitive documents against unauthorized alterations, ensuring the integrity of exclusive content. The test focused on fingerprinting and authenticating two files—a Microsoft Word document and a PDF file—anchored to both Bitcoin and Ethereum blockchains.

For reference, all certificates and relevant data are available in the GitHub repository: [https://github.com/wsaqaf/blockchainai/](https://github.com/wsaqaf/blockchainai/).

---

### Summary of Test Results

| File | Type | Hash | Blockchain | Timestamp | Transaction ID | Root Hash | Verification Link |
|------|------|------|------------|-----------|----------------|-----------|-------------------|
| **Document 1 (Example.pdf)** | PDF | `5750bc5811e40a7767372828c4c972e9537614b7371eb49762c93f06554856e5` | Bitcoin | Mar-27-2024 00:01:24 UTC | `15c86bc19e203f5ad15a3536bc78de4fcca61972a2d6ef96001fde2646f3c7f7` | `3cd08c1630376e317284ade94c650d3091c1806a1cdf86e9f41c1bb51e030b82` | [Verify](https://verify.originstamp.com) |
|  |  |  | Ethereum | Mar-26-2024 18:00:11 UTC | `0xe9cbff835dfa55501660173a6c3e20d8878d806bcd9a9940d14ab1e559f1b06e` | `c73181f66bcaf73a7af66d50aba84262473ec61023382f5be75d65db01bbf0b6` | [Verify](https://verify.originstamp.com) |
| **Document 2 (Test Document 2.docx)** | MS Word | `bffab64326fa361cab019bc38a62923fe04c0b8dfb1a776c4e2d79f63ddadc29` | Bitcoin | Oct-28-2024 00:52:45 UTC | `fcd24af11b083fa76d20e5c5960de9bee4ea9d9651fd1435b72b0905de8dcd6f` | `46838ca2a1f2bb12c44916aebed12ba29aa8342fb973ae818e09e89263d9d222` | [Verify](https://verify.originstamp.com) |
|  |  |  | Ethereum | Oct-27-2024 18:00:23 UTC | `0xdea355596931b69f25d9f9d41d46d20957190530ebf785b29930850714dd2894` | `975ee2ff1804d6b3316d29327094ffcf30b1c3480dbf944f5cbb6ddcc74a19b1` | [Verify](https://verify.originstamp.com) |

---

### Detailed Analysis of the Fingerprinting Process

For journalists handling exclusive content and confidential documents, OriginStamp offers a secure, privacy-conscious method for timestamping without exposing document content. Key elements of the fingerprinting process, as applied in this test, are outlined below:

1. **File Hash Generation**:
   - Each document’s SHA-256 hash was generated locally to ensure privacy, allowing OriginStamp to receive only the cryptographic fingerprint rather than the content itself.
   - This privacy-focused method secures the document’s authenticity while preventing potential data exposure.

2. **Blockchain Anchoring**:
   - Once submitted, OriginStamp anchored the hashes to the Bitcoin and Ethereum blockchains, providing an immutable, tamper-proof timestamp. Each blockchain entry includes:
     - **Transaction ID**: Unique identifier for the transaction embedding the document’s hash.
     - **Root Hash**: The Merkle root hash confirms the document’s inclusion in the transaction, enabling authentication.
   - **Verification Links**: Each timestamp includes a verification link, enabling confirmation on OriginStamp’s platform or directly through blockchain explorers, allowing verification independent of OriginStamp itself. This approach has been verified through blockchain explorers as part of the testing, confirming that the Bitcoin and Ethereum transactions took place.

3. **Proof Certificates**:
   - Each timestamp generated a certificate detailing file hash, blockchain transaction IDs, root hashes, and timestamps.
   - These certificates provide a tangible method for independently verifying document authenticity, ensuring journalistic content remains unaltered and exclusive.

4. **Re-Upload Verification**:
   - The system identifies previously fingerprinted files, immediately confirming their prior blockchain presence on re-upload, streamlining authenticity verification for journalists handling iterative content reviews.

5. **White-Labeling Capability**:
   - OriginStamp’s white-labeling feature allows news organizations to apply their corporate identity to timestamp certificates, offering a branded layer of assurance for exclusive media content. This customization enhances brand credibility while demonstrating document authenticity in a format recognizable to audiences.

---

### Implications for Journalistic Use and Large-Scale Applications

**Scalability with API Integration**:
OriginStamp’s RESTful API can facilitate high-volume document anchoring, providing a scalable solution for news organizations requiring frequent timestamping of articles, sources, or investigative reports.

**Enhancing Media Integrity**:
By offering tamper-proof timestamping on two blockchains, OriginStamp bolsters content security. The ability to independently verify timestamped files supports the protection of exclusive news materials, preserving journalistic integrity.

**Comparison to Traditional Hashing**:
Unlike centralized hash storage, OriginStamp’s anchoring of documents on public blockchains adds a verifiable public record, reinforcing document trustworthiness and reducing reliance on third-party verification.

---

### Conclusion

OriginStamp demonstrates high usability and security as a timestamping solution for journalism, making it an effective tool for protecting exclusive content and sensitive documents. The white-labeling capability adds a customized layer, suitable for large media outlets aiming to showcase document authenticity. The ability to verify timestamps directly through blockchain explorers without OriginStamp also adds credibility and independence, making this service especially valuable for journalism where content integrity is essential.
