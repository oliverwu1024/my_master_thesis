# Master Thesis

## Supervisors
- Dr. Angus Dempster
- Dr. Christoph Bergemeir
- Prof. Daniel Schmidt

## Abstract
Prior-Fitted Networks (PFNs) offer a novel approach to time series forecasting by training neural networks on synthetically generated data from statistical models, enabling zero-shot predictions without fine-tuning. This study investigates whether the Local and Global Trend (LGT) model, a Bayesian exponential smoothing method, can serve as an effective prior for PFN training. LGT models are fitted to M3 monthly competition series, and their learned parameter distributions are used to generate synthetic time series for training a ForecastPFN transformer architecture. Evaluation across five datasets reveals mixed performance: the model generally underperforms traditional automatic methods like AutoETS and AutoARIMA, but achieves competitive results on specific datasets. These findings demonstrate that LGT-generated synthetic data can capture meaningful forecasting patterns, whilst highlighting the importance of synthetic data diversity and prior-architecture alignment. The research establishes a foundation for combining Bayesian statistical models with neural forecasting approaches in the zero-shot domain.

## Materials
- Thesis PDF: `31977251_Che-YuWu_AngusDempster_Thesis.pdf`
- Presentation slides: `Presentation.pptx`
- Presentation recording: `Che-YuWu-AngusDempster-FINAL_PRESENTATION.mp4`

## License
All rights reserved. No part of this work may be copied, reproduced, distributed, or transmitted in any form or by any means without explicit prior written permission from the author.
