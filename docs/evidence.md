# Evidence and source notes

This case study was prepared from two author-provided documents: the Arabic graduation report (89 PDF pages) and Abdul Salam Al-Saeedi's CV. Neither source document is bundled. No repository source code, dataset, model checkpoint, training log, or running application was inspected.

Page references below use the PDF page position, starting at 1. The report's printed page numbers differ by 10 in the relevant sections: PDF page 75 is printed page 65.

## Claim traceability

| Claim | Source and qualification |
| --- | --- |
| Five-person project team | CV, Smart Inventory System project entry |
| Personal role: led data collection and annotation, trained the model, contributed to the admin dashboard | CV, explicit “My role” statement. System-wide implementation is attributed to the team. |
| Approximately 800 images and 17 categories | CV project entry. The extracted report text did not independently establish these totals; dataset files were unavailable. |
| Bounding-box annotation with Roboflow | CV; report PDF page 72 describes YOLOv8-format export and normalized coordinates. |
| 80/10/10 split | Report PDF page 73 (printed 63), also CV. This documents the intended split, not an independent leakage audit. |
| YOLOv8s, AdamW, eight GPU-hours | Report PDF page 75 (printed 65). It also lists batch size 4, initial learning rate 0.0005, and weight decay 0.0001. |
| 94.3% mAP@50 | Report PDF page 75. The CV calls it validation-set mAP@50; the report page does not specify the split. No test-set result is asserted. |
| Approximately 50% in practical trials; incorrect or incomplete results | Report PDF page 75. An informal observation with no stated protocol, sample size or metric definition; not comparable with mAP@50. |
| Flutter, Flask, YOLOv8, ASP.NET Web API, SQL Server | Report PDF page 77 (printed 67). YOLOv8s variant is specified on PDF page 75. |
| Blazor dashboard and administrative functions | Report PDF page 78 (printed 68); screenshots on PDF page 66. |
| Image-to-prediction-to-audit workflow | Report PDF pages 78-79. These describe Flask `/predict` and an audit-save operation through the ASP.NET backend. The diagram summarizes the report rather than documenting a tested interface. |
| Visible objects only; no inference of box contents | Report PDF page 78. |
| Manual correction | PDF page 60 discusses review/correction; PDF page 79 explicitly disallows manual editing of boxes and quantities. The README treats this as unresolved and proposes correction as future work. |
| Continuous cameras, ERP integration, predictive analysis | Report PDF page 80, explicitly future functions. Not claimed as delivered. |

## Screenshot provenance

These files were extracted directly from embedded PDF images, without generative editing, resizing or cropping:

| Repository image | PDF page | Printed page | Description |
| --- | --- | --- | --- |
| `assets/screenshots/mobile-home.jpg` | 57 | 47 | Flutter home screen |
| `assets/screenshots/analysis-results.jpg` | 60 | 50 | Analysis result screen |
| `assets/screenshots/training-data.png` | 66 | 56 | Training-data management interface |
| `assets/screenshots/add-product.jpg` | 66 | 56 | Product creation dialog |

Images were visually checked for legibility and personal information. No student numbers, contact details or academic cover pages are included. Product names and interface labels are retained as shown in the report. Screenshots establish appearance only, not tested behavior.

## Release scope

This package contains a portfolio case study and four screenshots. It does not include application source code, a dataset, model weights, academic PDFs, personal contact details, or claims of exclusive ownership. No software license is assigned to the team's unprovided code.
