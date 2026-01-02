# Master Thesis

## Personal Note
This thesis represents my first sustained research experience, and it has shaped both my skills and my outlook. I am deeply grateful to my supervisors for their guidance, for the discussions that helped me refine my ideas, and for the meetings I genuinely looked forward to. I remember the long nights of reading, coding, and revising, and I appreciate how those moments taught me persistence and discipline. Although the results in this thesis were not as strong as I hoped, the process itself inspired me to continue; it confirmed that I want to pursue research further. The experience strengthened my critical thinking and my ability to question assumptions, evaluate evidence, and communicate uncertainty, which I now see as essential, transferable skills. I am preparing my first paper for publication, and I carry forward both the lessons and the motivation I gained during this work.

## Topic
Combining Full Bayesian Inference with Prior-Fitted Networks for Time Series Forecasting

## Supervisors
- Dr. Angus Dempster
- Dr. Christoph Bergemeir
- Prof. Daniel Schmidt

## Introduction
This thesis explores zero-shot time series forecasting by combining Bayesian statistical models with neural network priors. It focuses on using synthetic data from the Local and Global Trend (LGT) model to train Prior-Fitted Networks (PFNs) and assess how well the resulting models generalize across datasets.

## Abstract
Prior-Fitted Networks (PFNs) offer a novel approach to time series forecasting by training neural networks on synthetically generated data from statistical models, enabling zero-shot predictions without fine-tuning. This study investigates whether the Local and Global Trend (LGT) model, a Bayesian exponential smoothing method, can serve as an effective prior for PFN training. LGT models are fitted to M3 monthly competition series, and their learned parameter distributions are used to generate synthetic time series for training a ForecastPFN transformer architecture. Evaluation across five datasets reveals mixed performance: the model generally underperforms traditional automatic methods like AutoETS and AutoARIMA, but achieves competitive results on specific datasets. These findings demonstrate that LGT-generated synthetic data can capture meaningful forecasting patterns, whilst highlighting the importance of synthetic data diversity and prior-architecture alignment. The research establishes a foundation for combining Bayesian statistical models with neural forecasting approaches in the zero-shot domain.

## Results, Discussion, and Future Work (Short Summary)
Results show the PFN trained on LGT-simulated data wins only on CIF 2016 (MASE), and otherwise trails AutoETS and AutoARIMA, with the largest gaps on M3 Monthly and FRED-MD. sMAPE is broadly consistent, with the model usually beating Seasonal Naive but not the automatic baselines. Inference time is faster than AutoARIMA but slower than AutoETS and Seasonal Naive, with an anomaly on FRED-MD.
Discussion highlights a key confound: ForecastPFN implementation issues (training instability, scaling, evaluation setup, and persistent prediction flatness) make it hard to isolate whether LGT is a weak prior or the architecture is limiting. Limited synthetic data diversity (only M3 Monthly), possible architecture-prior mismatch, and the challenge of using LGT as a data generator also constrain performance, despite partial successes on CIF 2016 and Hospital.
Future work should fix architectural issues or test alternative architectures, expand LGT parameter learning to more diverse datasets and frequencies, and explore probabilistic forecasting and ensemble approaches to leverage Bayesian priors more effectively.

## Materials
- Thesis PDF: `31977251_Che-YuWu_AngusDempster_Thesis.pdf`
- Presentation slides: `Presentation.pptx`
- Presentation recording: `Che-YuWu-AngusDempster-FINAL_PRESENTATION.mp4`

## License
All rights reserved. No part of this work may be copied, reproduced, distributed, or transmitted in any form or by any means without explicit prior written permission from the author.
