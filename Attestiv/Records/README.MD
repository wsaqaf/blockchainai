**Report on Document Timestamping with Attestiv’s 'Records' Service**

**Introduction**

This report documents the results of a test conducted using Attestiv's "Records" service, which allows users to upload and timestamp documents and images. While this service appears similar to blockchain-based solutions like OriginStamp—which uses blockchain networks such as Bitcoin and Ethereum for document fingerprinting—the precise role of blockchain or immutable ledger technology in Attestiv’s "Records" service is unclear. The purpose of this test was to evaluate the usability and reliability of the "Records" service for timestamping files, focusing on the generated report and system stability.

For reference, all test files and associated reports are available in the GitHub repository: [https://github.com/wsaqaf/blockchainai/tree/main/Attestiv](https://github.com/wsaqaf/blockchainai/tree/main/Attestiv).

---

### Summary of Test Results

| File | Description | Validation Status | Tamper Score | Issues |
|------|-------------|-------------------|--------------|--------|
| **Document** | Uploaded for timestamping | Validated | **88** | Report generated with unclear tamper details; broken image links and metadata anomalies |
| **Video** | Uploaded for timestamping | Validated | N/A | Report was incomplete and inconclusive |

---

### Detailed Analysis of the Records Service

#### File Upload and Timestamping

Two files—a document and a video—were uploaded to the "Records" service for timestamping. The service confirmed that the files were validated and timestamped, but the resulting report raised concerns about the clarity and reliability of the information provided.

1. **Document Upload**:
   - **Tamper Score**: 88
   - **Validation Status**: Confirmed as validated and imported.
   - **Issues**: 
     - The report provided metadata and a tamper score, yet details on what triggered the tamper score were unclear.
     - Broken image links were noted in the report, and the PDF generation was incomplete.
   - **Implication**: The report’s lack of transparency on the tamper score calculation and metadata details limits its usefulness in verifying the document’s authenticity and timestamp. Also the PDF report generation failed.

2. **Video Upload**:
   - **Validation Status**: Confirmed as validated and imported.
   - **Issues**:
     - PDF report generation failed, resulting in an incomplete and inconclusive report with missing data.
     - No tamper score was provided, and no clear indication of blockchain or ledger involvement was apparent.
   - **Implication**: The failure to generate a complete report suggests that the video analysis feature within "Records" may still be under development.

---

### Observations on Blockchain and Immutable Ledger Technology

Attestiv’s "Records" service does not provide clear information on the underlying technology for ensuring document integrity. There was no mention of Bitcoin, Ethereum, or any other ledger, which raises questions about the extent to which immutability is guaranteed. Given the incomplete reports and the lack of visible blockchain integration, it is likely that this service is in an early development stage.

---

### Conclusion

The test results suggest that Attestiv’s "Records" service has potential for timestamping and file validation, but its current implementation has limitations. The broken images, unclear tamper scores, and incomplete PDF generation indicate that the service may not yet be ready for reliable use in a professional setting, such as journalism. Additional clarity on the use of blockchain or ledger technology, if any, and further development of report generation functionality would be necessary for the service to achieve practical usability and transparency in timestamping applications.
