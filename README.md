# Multi Speaker Speech Recognition (MSSR)

## Overview
This project implements **Multi Speaker Speech Recognition (MSSR)** using the [ESPnet](https://github.com/espnet/espnet) tool. Currently, it only supports the separation and recognition of speech when two voices are mixed. Future plans include extending the implementation to handle an arbitrary number of speakers.

- Supported Language : EN(english) only
- Used Dataset : Libri2Mix from [LibriMix](https://github.com/JorisCos/LibriMix)
- Trained Model Link: [Model Link](https://huggingface.co/craft8244/MSSR)
- Performance:

| Model                                    | WER   | Relative Improvement (rel. imp.) |
|------------------------------------------|-------|----------------------------------|
| Single-speaker ASR                       | 76.90 | -                                |
| DPRNN-TasNet + ASR                       | 13.60 | -                                |
| Transformer Multi-speaker ASR            | 8.43  | -                                |
| SAT-ASR i-vector                         | 8.50  | -0.8%                            |
| SAT-ASR d-vector                         | 8.32  | 1.3%                             |
| SAT-ASR x-vector                         | 8.10  | 3.9%                             |
| SAT-ASR i-vector + speaker profile       | 8.27  | 1.9%                             |
| SAT-ASR d-vector + speaker profile       | 8.18  | 3.0%                             |
| SAT-ASR x-vector + speaker profile       | 7.48  | 11.2%                            |

- Related Paper Link: [Paper Link](#)

## Update Plan & History
### version 0.2.0 - future plan
- upload training code.
- upload paper link.

### version 0.1.0 - 2024-08-20
- Initial release with support for 2-speaker separation using ESPnet.
- Included Trained models and performance metrics.

## Installation and Usage
__Important: The current code only supports testing, training is not available.__  
This project follows the `egs2` format of ESPnet. Follow the steps below to install and run the project:

1. **Install ESPnet**  
   Install ESPnet by following the [ESPnet Installation Guide](https://espnet.github.io/espnet/installation.html).

2. **Modify path.sh**  
   Modify the __path.sh__ file in this project to adjust the paths accordingly.
   ```bash
   MAIN_ROOT=/your/custom/path/to/espnet/
   KALDI_ROOT=$MAIN_ROOT/tools/kaldi
3. **Download exp directory**
   Download exp directory from Trained Model Link.
   __Upcoming Update ver 0.2.0__ : Training code will be updated
4. **Run the Project**  
   Execute the following command to start the project:
   ```bash
   #Only support x-vector model in version 0.1.0
   ./run.sh
   
   #SAT-ASR i-vector
   ./run_ivec.sh
   #SAT-ASR d-vector
   ./run_dvec.sh
   #SAT-ASR x-vector
   ./run_xvec.sh
   #SAT-ASR with speaker profile (i,d,x vector)
   ./run_*vec_sp.sh
