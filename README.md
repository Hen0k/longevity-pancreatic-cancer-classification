# longevity-pancreatic-cancer-classification

The dataset used in this project was taken from [Kaggle][dataset-link].
It has the following columns:

- **`sample_id`** - Unique string identifying each subject
- **`patient_cohort`** - "Cohort 1,  previously used samples; Cohort 2, newly added samples"
- **`sample_origin`** - "BPTB: Barts Pancreas Tissue Bank, London, UK; ESP: Spanish National Cancer Research Centre, Madrid, Spain; LIV: Liverpool University, UK; UCL: University College London, UK"
- **`age`** - in years
- **`sex`** - M = male, F = female"
- **`diagnosis`** - (1=Control, 2=Benign, 3=PDAC)","1 = control (no pancreatic disease), 2 = benign hepatobiliary disease (119 of which are chronic pancreatitis); 3 = Pancreatic ductal adenocarcinoma, i.e. pancreatic cancer"
- **`stage`** - "For those with pancreatic cancer, what stage was it? One of IA, IB, IIA, IIIB, III, IV"
- **`benign_sample_diagnosis`** - "For those with a benign, non-cancerous diagnosis, what was the diagnosis?"
- **`plasma_CA19_9`** - Blood plasma levels of CA 19–9 monoclonal antibody that is often elevated in patients with pancreatic cancer. Only assessed in 350 patients (one goal of the study was to compare various CA 19-9 cutpoints from a blood sample to the model developed using urinary samples).
- **`creatinine`** - Urinary biomarker of kidney function
- **`LYVE1`** - "Urinary levels of Lymphatic vessel endothelial hyaluronan receptor 1, a protein that may play a role in tumor metastasis"
- **`REG1B`** - Urinary levels of a protein that may be associated with pancreas regeneration.
- **`TFF1`** - "Urinary levels of Trefoil Factor 1, which may be related to regeneration and repair of the urinary tract"
- **`REG1A`** - Urinary levels of a protein that may be associated with pancreas regeneration. Only assessed in 306 patients (one goal of the study was to assess REG1B vs REG1A)

## The main goal

The goal here was to be able to predict the diagnosis of a patient given some of the above parameters. I decided not to use some of the features because they wouldn't contribute much to the prediction power of the model or because they would introduce some unwanted bias into the model.
[This][dataset-link] dataset was created to train a model that is able to differentiating between 3 (pancreatic cancer) versus 2 (non-cancerous pancreas condition) and 1 (healthy). But I decided to simplify the task into predicting only the diagnosis column. This makes the problem a 3 class classification task.

Here are the columns I decided to use:

- **`age`**
- **`sex`**
- **`diagnosis`**
- **`plasma_CA19_9`**
- **`creatinine`**
- **`LYVE1`**
- **`REG1B`**
- **`TFF1`**
- **`REG1A`**

[dataset-link]: https://www.kaggle.com/datasets/johnjdavisiv/urinary-biomarkers-for-pancreatic-cancer?select=Debernardi+et+al+2020+documentation.csv
