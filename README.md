# Multi Speaker Speech Recognition (MSSR)

## Overview
This project implements **Multi Speaker Speech Recognition (MSSR)** using the [ESPnet](https://github.com/espnet/espnet) tool. Currently, it only supports the separation and recognition of speech when two voices are mixed. Future plans include extending the implementation to handle an arbitrary number of speakers.

- Trained Model Link: [Model Link](#)
- Performance: Performance comparison of the baseline model and the proposed models in terms of WER (Word Error Rate) and their relative improvements (rel. imp.) over the baseline.

| Model                                    | WER   | Relative Improvement (rel. imp.) |
|------------------------------------------|-------|----------------------------------|
| Single-speaker ASR                       | 76.90 | -                                |
| DPRNN-TasNet + ASR [43]                  | 13.60 | -                                |
| Transformer Multi-speaker ASR [5]        | 8.43  | -                                |
| SAT-ASR i-vector                         | 8.50  | -0.8%                            |
| (proposed) d-vector                      | 8.32  | 1.3%                             |
| x-vector                                 | 8.10  | 3.9%                             |
| SAT-ASR i-vector + speaker profile       | 8.27  | 1.9%                             |
| (proposed) d-vector + speaker profile    | 8.18  | 3.0%                             |
| (proposed) x-vector                      | 7.48  | 11.2%                            |

- Related Paper Link: [Paper Link](#)

## Installation and Usage
This project follows the `egs2` format of ESPnet. Follow the steps below to install and run the project:

1. **Install ESPnet**  
   Install ESPnet by following the [ESPnet Installation Guide](https://espnet.github.io/espnet/installation.html).

2. **Modify path.sh**  
   Modify the `path.sh` file in this project to adjust the paths accordingly.

3. **Run the Project**  
   Execute the following command to start the project:
   ```bash
   ./run.sh
