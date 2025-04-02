# License Plate Recognition Pipeline


## Workflow

```mermaid
graph TD;
    A[ANPR Camera] --> B[Image/Video Capture];
    B --> C[Pre-Processing];
    C --> D[License Plate Detection (Using YOLO models)];
    D --> E[License Plate Cropping];
    
    subgraph Detection
        B;
        C;
        D;
        E;
    end
    
    E --> F[Image Processing];
    F --> G[Character Segmentation];
    G --> H[Character Recognition (EasyOCR or Custom OCR)];
    H --> I[Post Processing to Validate License Plate];
    I --> J[OUTPUT];
    J --> K[API Endpoint];
    
    subgraph Recognition
        F;
        G;
        H;
        I;
        J;
    end
```

