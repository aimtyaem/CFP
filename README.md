## AutoGS
![AutoGS](img/logo.jpg)
# AutoGuided Onboarding WebApp for Carbon Footprint Reduction (v2.0)

---

## Background

The AutoGuided Onboarding webApp (AGO) addresses carbon footprint reduction through innovative technology. Leveraging autonomous small satellites (smallsats) for earth observation, this webApp provides users with personalized insights and recommendations, now enhanced by **AWS SageMaker AI models** for more accurate predictions and smarter recommendations. Our goal is to empower individuals and organizations to take actionable steps towards a more sustainable future.

---

## New Update: AWS SageMaker AI Model Integration

We’ve modernized the backend with **Amazon SageMaker** to manage, train, and deploy machine learning models that power the AGO platform.

### Features of the SageMaker Integration:
- Centralized training pipelines using SageMaker Pipelines
- Real-time recommendations via SageMaker Endpoints
- Automated model updates using SageMaker Model Registry
- Improved scalability for handling earth observation datasets
- Secured with AWS Identity and Access Management (IAM)

> **Note:** The legacy model in `/backend/ml/carbon_model.ipynb` has been migrated to a managed SageMaker pipeline for production readiness.

---

## Project Structure

autoguided-webapp/
├── frontend/
│   ├── pages/
│   │   ├── onboarding.html
│   │   └── dashboard.html
│   └── components/dashboard.json
├── backend/
│   ├── routes/sat_data.ipynb
│   ├── ml/
│   │   ├── carbon_model_sagemaker_pipeline.ipynb │   │   ├── deploy_endpoint.py │   │   └── inference_handler.py │   └── H2Ogpt/Onboarding_Dashboard_AutoGuidedChatbot
├── AutoSmallSat_Datasets/
│   ├── aws_ground_station.ipynb
│   └── imagery_processing.ipynb
├── Output/
└── Branches files/

---

## Readme Content

This project includes the following components:

1. [Wireframe Design](#wireframe-design)  
2. [Prototype](#prototype)  
3. [Mockup Design](#mockup-design)  
4. [SageMaker AI Model Update](#sagemaker-ai-model-update)  
5. [Development Requirements](#development-requirements)  
6. [Getting Started](#getting-started)  
7. [Contribution Guidelines](#contribution-guidelines)  
8. [Code of Conduct](#code-of-conduct)  
9. [Contact](#contact)  
10. [License](#license)  
11. [Resources](#resources)  

---

## Wireframe Design

[Wireframe Details Here — *unchanged*]

---

## Prototype

[Prototype Links Here — *unchanged*]

---

## Mockup Design

[Mockup Images Here — *unchanged*]

---

## SageMaker AI Model Update

### Pipeline Overview
- **Training:** Uses earth observation data from SmallSat datasets, processed via `imagery_processing.ipynb`.
- **Model Registry:** Tracks and versions trained models for audit and reproducibility.
- **Deployment:** Real-time inference is served through SageMaker Endpoints connected to the webApp dashboard.
- **AutoML Option:** Integrated H2O AutoML for model selection, optionally invoked through the pipeline.

### Key Files
- `ml/carbon_model_sagemaker_pipeline.ipynb`: Defines the SageMaker pipeline (processing, training, evaluation, registration).
- `ml/deploy_endpoint.py`: Deploys model to a live endpoint.
- `ml/inference_handler.py`: Handles incoming prediction requests from the webApp frontend.

### AWS Services Used
- **Amazon SageMaker**
- **AWS Ground Station**
- **Amazon S3**
- **AWS Lambda** (optional for serverless invocations)
- **Amazon CloudWatch** for monitoring

### Benefits of Migration to SageMaker:
- Managed scalability and training
- Built-in model versioning
- Secure and compliant infrastructure
- Reduced operational overhead

---

## Development Requirements

- **Python 3.9+**
- **AWS CLI** configured with appropriate IAM permissions
- **AWS SDKs** (`boto3`, `sagemaker`)
- Python packages:
  - `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `transformers`
  - `torch`, `tensorflow`, `gradio`, `rasterio`, `cv2`
  - `h2o`, `sagemaker`, `boto3`
- Optional: **Docker** (for local SageMaker training jobs)
- **Git client**

---

## Getting Started

1. **Clone the repository:**

```bash
git clone https://github.com/aimtyaem/AGO.git
cd AGO

2. Set up Python environment:



python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

3. Configure AWS credentials:



aws configure

4. Run SageMaker pipeline notebook:

Open ml/carbon_model_sagemaker_pipeline.ipynb and execute cells.

Deploy endpoint with deploy_endpoint.py.



5. Launch frontend and connect to live AI models.




---

Contribution Guidelines

[Contribution Guidelines — unchanged]


---

Code of Conduct

[Code of Conduct — unchanged]


---

Contact

Ahmed Ibrahim Metawee


---

License

Licensed under the MIT License.


---

Resources

Visit the project wiki for in-depth guides.


---

We hope this enhanced version of AGO empowers users even further in their carbon reduction journeys, backed by AWS-powered machine learning intelligence.


---

Would you also like me to generate a matching requirements.txt that aligns with this SageMaker upgrade?
(It’ll make onboarding contributors even smoother.)

Let me know if you’d like me to also convert the **"requirements.txt"** portion to markdown code style for full consistency!

