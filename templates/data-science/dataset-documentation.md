<!-- 
  TEMPLATE: Dataset Documentation
  COMPLEXITY: Medium to High
  FEATURES: Data dictionary, Schema documentation, Metadata tables
  USE CASE: Documenting datasets for research, machine learning, and data science projects.
-->

# Dataset Documentation Template

Comprehensive documentation for datasets used in research, data science, and machine learning projects. Choose the variant that matches your dataset's complexity and audience.

## Intended For

- Research datasets (academic, scientific)
- Machine learning training data
- Open data releases
- Data repositories and archives
- Corporate data assets
- Government data portals

## Variants Included

- **Minimal**: Quick documentation for simple datasets or internal use
- **Standard**: Recommended structure for most public datasets
- **Comprehensive**: Full documentation for complex datasets requiring detailed metadata

## Tested On

- GitHub
- GitLab
- Markdown viewers (VS Code, bat, less)
- Documentation sites (MkDocs, Sphinx)
- Data repository platforms (Zenodo, figshare)

---

## Variant 1: Minimal

*Best for: Small datasets, proof-of-concept data, internal team use*

```markdown
# [Dataset Name]

## Overview

[Brief description of what the dataset contains and its purpose.]

**Size**: [e.g., 1,000 rows, 50MB]  
**Format**: [e.g., CSV, JSON, Parquet]  
**License**: [e.g., CC BY 4.0, MIT]

## Files

- `data.csv` - Main dataset file
- `README.md` - This file

## Columns

| Column | Type | Description |
| ------ | ---- | ----------- |
| id | integer | Unique identifier |
| name | string | Name field |
| value | float | Measurement value |
| timestamp | datetime | Recording time |

## Usage

\`\`\`python
import pandas as pd

df = pd.read_csv('data.csv')
print(df.head())
\`\`\`

## License

[License name and link]
```

---

## Variant 2: Standard

*Best for: Public datasets, research data, ML datasets*

```markdown
# [Dataset Name]

![License](https://img.shields.io/badge/license-CC_BY_4.0-blue)
![Format](https://img.shields.io/badge/format-CSV-green)

> [One-sentence description of the dataset and its primary purpose.]

## Overview

[Detailed description of the dataset: what it contains, why it was created, what problems it addresses, and who should use it.]

**Key Statistics:**
- **Instances**: 10,000
- **Features**: 25
- **File Size**: 15 MB
- **Format**: CSV
- **Last Updated**: 2025-11-24

## Table of Contents

- [Files](#files)
- [Data Dictionary](#data-dictionary)
- [Collection Methodology](#collection-methodology)
- [Data Quality](#data-quality)
- [Usage Examples](#usage-examples)
- [License and Citation](#license-and-citation)

## Files

| File | Size | Description |
| ---- | ---- | ----------- |
| `dataset.csv` | 15 MB | Main dataset |
| `README.md` | 5 KB | This documentation |
| `schema.json` | 2 KB | JSON schema definition |

## Data Dictionary

### Overview

[Brief explanation of the data structure and organization.]

### Column Specifications

| Column | Type | Range/Values | Nullable | Description |
| ------ | ---- | ------------ | -------- | ----------- |
| `id` | integer | 1-10000 | No | Unique identifier |
| `timestamp` | datetime | 2020-2025 | No | Recording timestamp (UTC) |
| `category` | string | A, B, C | No | Classification category |
| `value` | float | 0.0-100.0 | Yes | Measured value |
| `label` | boolean | true/false | No | Target variable |

### Categorical Variables

**category**:
- `A`: Category A description
- `B`: Category B description  
- `C`: Category C description

## Collection Methodology

### Data Sources

[Describe where the data came from: surveys, sensors, APIs, web scraping, etc.]

### Collection Process

1. [Step 1 of data collection]
2. [Step 2 of data collection]
3. [Step 3 of data collection]

### Time Period

Data collected from [start date] to [end date].

### Sample Strategy

[Explain sampling method: random, stratified, convenience, etc.]

## Data Quality

### Completeness

- **Missing values**: 2% overall
- Columns with missing data: `value` (2%), others complete

### Accuracy

[Describe validation process and accuracy measures.]

### Known Issues

- [Issue 1]: Description and impact
- [Issue 2]: Description and impact

### Preprocessing Applied

- [x] Removed duplicates
- [x] Handled missing values (strategy: [mean imputation/removal/etc.])
- [x] Standardized formats
- [ ] No outlier removal applied

## Usage Examples

### Loading the Data

**Python (pandas):**
\`\`\`python
import pandas as pd

df = pd.read_csv('dataset.csv')
print(df.shape)  # (10000, 5)
print(df.head())
\`\`\`

**R:**
\`\`\`r
library(readr)

data <- read_csv("dataset.csv")
summary(data)
\`\`\`

### Basic Analysis

\`\`\`python
# Summary statistics
print(df.describe())

# Check for missing values
print(df.isnull().sum())

# Value counts for categorical
print(df['category'].value_counts())
\`\`\`

## License and Citation

### License

This dataset is licensed under [License Name] ([License Link]).

**You are free to:**
- Share and redistribute
- Adapt and build upon

**Under these terms:**
- Provide attribution
- [Any additional terms]

### Citation

If you use this dataset in your research, please cite:

\`\`\`bibtex
@dataset{dataset_name_2025,
  author = {Author Name},
  title = {Dataset Name},
  year = {2025},
  publisher = {Platform Name},
  doi = {10.XXXX/example}
}
\`\`\`

### Contact

For questions or issues: [email@example.com]
```

---

## Variant 3: Comprehensive

*Best for: Large-scale datasets, research publications, highly regulated data*

```markdown
# [Dataset Name]: [Descriptive Subtitle]

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXX)
[![License](https://img.shields.io/badge/license-CC_BY_4.0-blue)](LICENSE)
[![Format](https://img.shields.io/badge/format-CSV%20|%20JSON%20|%20Parquet-green)]()

> [Compelling one-sentence description of the dataset's value proposition.]

## Abstract

[Academic-style abstract: comprehensive overview of the dataset, its creation, key characteristics, potential applications, and significance. 150-250 words.]

## Table of Contents

- [Overview](#overview)
- [Key Statistics](#key-statistics)
- [File Structure](#file-structure)
- [Data Dictionary](#data-dictionary)
- [Collection Methodology](#collection-methodology)
- [Data Quality and Validation](#data-quality-and-validation)
- [Ethical Considerations](#ethical-considerations)
- [Usage Guide](#usage-guide)
- [Versioning and Updates](#versioning-and-updates)
- [Related Datasets](#related-datasets)
- [Publications](#publications)
- [License and Attribution](#license-and-attribution)
- [Support and Contact](#support-and-contact)

## Overview

### Purpose

[Detailed explanation of why this dataset was created and what problems it addresses.]

### Scope

- **Domain**: [e.g., Healthcare, Finance, Climate Science]
- **Geographic Coverage**: [e.g., United States, Global, Urban areas]
- **Temporal Coverage**: [Start date] to [End date]
- **Population**: [Description of entities or subjects]

### Key Features

- **Instances**: 1,000,000
- **Features**: 127
- **Feature Types**: 45 numerical, 32 categorical, 50 text
- **Target Variable(s)**: [Yes/No and description]
- **File Size**: 2.3 GB (uncompressed)
- **Formats Available**: CSV, JSON, Parquet, HDF5

### Versions

| Version | Date | Changes | DOI |
| ------- | ---- | ------- | --- |
| 2.0.0 | 2025-11-24 | Added 20 new features | [10.XXXX/v2] |
| 1.1.0 | 2025-06-15 | Fixed quality issues | [10.XXXX/v1.1] |
| 1.0.0 | 2025-01-10 | Initial release | [10.XXXX/v1] |

## Key Statistics

### Dataset Size

| Metric | Value |
| ------ | ----- |
| Total Records | 1,000,000 |
| Total Features | 127 |
| Compressed Size | 650 MB |
| Uncompressed Size | 2.3 GB |
| Number of Files | 12 |

### Feature Distribution

| Type | Count | Percentage |
| ---- | ----- | ---------- |
| Numerical (continuous) | 25 | 19.7% |
| Numerical (discrete) | 20 | 15.7% |
| Categorical (nominal) | 22 | 17.3% |
| Categorical (ordinal) | 10 | 7.9% |
| Text | 35 | 27.6% |
| Datetime | 10 | 7.9% |
| Boolean | 5 | 3.9% |

### Class Distribution (if classification dataset)

| Class | Count | Percentage |
| ----- | ----- | ---------- |
| Class 0 | 650,000 | 65% |
| Class 1 | 300,000 | 30% |
| Class 2 | 50,000 | 5% |

**Note**: Dataset is imbalanced; consider stratified sampling.

## File Structure

\`\`\`
dataset/
├── README.md                    # This file
├── LICENSE                      # License text
├── CHANGELOG.md                 # Version history
├── data/
│   ├── train.csv               # Training set (70%)
│   ├── validation.csv          # Validation set (15%)
│   ├── test.csv                # Test set (15%)
│   └── full_dataset.parquet    # Complete dataset (optimized format)
├── metadata/
│   ├── schema.json             # JSON schema definition
│   ├── codebook.pdf            # Detailed variable descriptions
│   └── statistics.json         # Computed statistics
├── scripts/
│   ├── load_data.py            # Data loading utilities
│   ├── validate.py             # Data validation script
│   └── requirements.txt        # Python dependencies
└── documentation/
    ├── collection_protocol.pdf # Detailed collection methodology
    ├── quality_report.pdf      # Data quality assessment
    └── ethical_review.pdf      # Ethics approval documentation
\`\`\`

## Data Dictionary

### Core Identifiers

| Column | Type | Example | Description |
| ------ | ---- | ------- | ----------- |
| `record_id` | string | "REC-0001234" | Unique record identifier |
| `timestamp` | datetime | 2025-11-24T10:30:00Z | Record creation time (UTC) |
| `version` | integer | 2 | Data version number |

### Demographic Features

| Column | Type | Range/Values | Nullable | Description |
| ------ | ---- | ------------ | -------- | ----------- |
| `age` | integer | 18-100 | No | Age in years |
| `gender` | categorical | M/F/O/U | No | Gender (M=Male, F=Female, O=Other, U=Undisclosed) |
| `location` | string | ISO 3166-1 | Yes | Country code |
| `education_level` | ordinal | 1-5 | Yes | Education level (1=Primary, 5=Postgraduate) |

### Measurement Features

| Column | Type | Range | Unit | Nullable | Description |
| ------ | ---- | ----- | ---- | -------- | ----------- |
| `value_1` | float | 0.0-100.0 | % | No | Primary measurement |
| `value_2` | float | -50.0-50.0 | units | Yes | Secondary measurement |
| `confidence` | float | 0.0-1.0 | probability | No | Measurement confidence score |

### Categorical Encodings

**gender**:
- `M`: Male
- `F`: Female
- `O`: Other/Non-binary
- `U`: Prefer not to disclose

**education_level**:
- `1`: Primary education
- `2`: Secondary education
- `3`: Bachelor's degree
- `4`: Master's degree
- `5`: Doctoral degree

**status** (target variable):
- `0`: Negative class
- `1`: Positive class (primary interest)
- `2`: Ambiguous/inconclusive

### Text Features

| Column | Type | Max Length | Language | Description |
| ------ | ---- | ---------- | -------- | ----------- |
| `description` | text | 500 chars | English | Free-text description |
| `comments` | text | 1000 chars | Multiple | Optional comments |

### Computed Features

| Column | Formula | Description |
| ------ | ------- | ----------- |
| `normalized_value` | `(value - mean) / std` | Z-score normalized value |
| `risk_score` | Custom algorithm | Computed risk indicator |

## Collection Methodology

### Data Sources

1. **Primary Sources**:
   - [Source 1]: Description and access method
   - [Source 2]: Description and access method

2. **Secondary Sources**:
   - [Source 3]: Used for validation/enrichment

### Collection Process

#### Phase 1: Data Acquisition

[Detailed description of initial data collection, including dates, methods, and tools used.]

#### Phase 2: Data Integration

[Explanation of how multiple sources were combined, including join keys and resolution strategies.]

#### Phase 3: Quality Assurance

[Description of validation, cleaning, and verification procedures.]

### Sampling Strategy

**Method**: [e.g., Stratified random sampling]

**Rationale**: [Why this sampling method was chosen]

**Implementation**: [How sampling was performed]

### Collection Period

- **Start Date**: 2023-01-01
- **End Date**: 2024-12-31
- **Total Duration**: 24 months

### Geographic Distribution

| Region | Records | Percentage |
| ------ | ------- | ---------- |
| North America | 400,000 | 40% |
| Europe | 300,000 | 30% |
| Asia | 250,000 | 25% |
| Other | 50,000 | 5% |

### Inclusion/Exclusion Criteria

**Included:**
- [Criterion 1]
- [Criterion 2]

**Excluded:**
- [Criterion 1]
- [Criterion 2]

## Data Quality and Validation

### Completeness Analysis

| Feature | Missing (%) | Strategy |
| ------- | ----------- | -------- |
| `age` | 0% | Required field |
| `location` | 5% | Allowed missing |
| `value_2` | 15% | Not applicable cases |
| Overall | 3.2% | Multiple strategies |

### Missing Data Handling

- **Required fields**: No missing values allowed
- **Optional fields**: Missing preserved as NULL
- **Imputed fields**: [List fields with imputation method]

### Accuracy and Validation

**Validation Methods:**
1. Range checks: All values within expected ranges
2. Cross-field validation: Logical consistency verified
3. External validation: Spot checks against source systems
4. Expert review: Domain experts reviewed samples

**Accuracy Metrics:**
- **Data entry error rate**: < 0.1%
- **Validation pass rate**: 99.8%

### Outliers

**Detection Method**: [e.g., IQR method, Z-score]

**Treatment**: Outliers flagged but retained in dataset. Use `is_outlier` flag.

### Known Limitations

1. **Limitation 1**: [Description and impact]
2. **Limitation 2**: [Description and impact]
3. **Limitation 3**: [Description and impact]

### Quality Metrics

| Metric | Score | Interpretation |
| ------ | ----- | -------------- |
| Completeness | 96.8% | Excellent |
| Accuracy | 99.2% | Excellent |
| Consistency | 98.5% | Excellent |
| Timeliness | Current | Up-to-date |

## Ethical Considerations

### Privacy and Anonymization

[Description of privacy protections, anonymization techniques, and PII removal.]

**Anonymization Methods:**
- [Method 1]: [Description]
- [Method 2]: [Description]

### Consent and Approval

- Ethics approval obtained: [Yes/No]
- IRB approval number: [Number]
- Consent obtained from participants: [Yes/No/N/A]

### Bias and Fairness

**Potential Biases:**
1. **Selection bias**: [Description and mitigation]
2. **Measurement bias**: [Description and mitigation]

**Fairness Considerations:**
[Discussion of representation, balance across sensitive attributes, and recommendations for fair use.]

### Intended Use

**Recommended Uses:**
- [Use case 1]
- [Use case 2]

**Not Recommended For:**
- [Inappropriate use case 1]
- [Inappropriate use case 2]

## Usage Guide

### Prerequisites

\`\`\`bash
# Python 3.8+
pip install pandas numpy scikit-learn

# R
install.packages(c("readr", "dplyr", "ggplot2"))
\`\`\`

### Loading Data

**Python:**

\`\`\`python
import pandas as pd

# Load CSV
df = pd.read_csv('data/full_dataset.csv')

# Load Parquet (faster, smaller)
df = pd.read_parquet('data/full_dataset.parquet')

# Load pre-split sets
train = pd.read_csv('data/train.csv')
val = pd.read_csv('data/validation.csv')
test = pd.read_csv('data/test.csv')
\`\`\`

**R:**

\`\`\`r
library(readr)
library(arrow)

# Load CSV
data <- read_csv("data/full_dataset.csv")

# Load Parquet
data <- read_parquet("data/full_dataset.parquet")
\`\`\`

### Basic Exploration

\`\`\`python
# Dataset shape
print(f"Shape: {df.shape}")

# Summary statistics
print(df.describe())

# Check missing values
print(df.isnull().sum())

# Class distribution
print(df['status'].value_counts())

# Feature types
print(df.dtypes)
\`\`\`

### Handling Missing Values

\`\`\`python
# Drop rows with any missing values
df_clean = df.dropna()

# Fill missing with mean (numerical)
df['value_2'].fillna(df['value_2'].mean(), inplace=True)

# Fill missing with mode (categorical)
df['location'].fillna(df['location'].mode()[0], inplace=True)
\`\`\`

### Feature Engineering Examples

\`\`\`python
# Create age groups
df['age_group'] = pd.cut(df['age'], bins=[0, 30, 50, 100], 
                         labels=['young', 'middle', 'senior'])

# Extract datetime features
df['year'] = pd.to_datetime(df['timestamp']).dt.year
df['month'] = pd.to_datetime(df['timestamp']).dt.month

# One-hot encode categorical
df_encoded = pd.get_dummies(df, columns=['gender', 'education_level'])
\`\`\`

### Machine Learning Example

\`\`\`python
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report

# Prepare features and target
X = df.drop(['status', 'record_id', 'timestamp'], axis=1)
y = df['status']

# Handle categorical variables
X = pd.get_dummies(X)

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

# Train model
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)

# Evaluate
y_pred = model.predict(X_test)
print(classification_report(y_test, y_pred))
\`\`\`

## Versioning and Updates

### Version History

See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

### Update Schedule

- **Major updates**: Annually (add new data, significant changes)
- **Minor updates**: Quarterly (bug fixes, quality improvements)
- **Patches**: As needed (critical issues)

### Reproducibility

Each version is archived with a permanent DOI. To reproduce results:

1. Note the dataset version used in your analysis
2. Include DOI in your citations
3. Document any preprocessing steps

## Related Datasets

- **[Related Dataset 1]**: [Brief description and link]
- **[Related Dataset 2]**: [Brief description and link]

## Publications

### Primary Citation

[Full citation for the dataset paper or primary publication]

### Research Using This Dataset

1. [Author et al. (Year)]. [Title]. [Journal/Conference]. [DOI]
2. [Author et al. (Year)]. [Title]. [Journal/Conference]. [DOI]

## License and Attribution

### License

This dataset is released under the **[License Name]** ([Full License Link]).

**Summary:**
- ✅ Commercial use allowed
- ✅ Modification allowed
- ✅ Distribution allowed
- ✅ Private use allowed
- ⚠️ Attribution required
- ⚠️ Share-alike required (if applicable)

Full license text: [LICENSE](LICENSE)

### Citation

**Plain Text:**
[Author Names]. (Year). [Dataset Name] [Data set]. [Publisher/Platform]. [DOI]

**BibTeX:**

\`\`\`bibtex
@dataset{dataset_key_2025,
  author = {Smith, John and Doe, Jane},
  title = {Dataset Name: Comprehensive Description},
  year = {2025},
  publisher = {Zenodo},
  version = {2.0.0},
  doi = {10.5281/zenodo.XXXXX},
  url = {https://doi.org/10.5281/zenodo.XXXXX}
}
\`\`\`

**RIS:**

\`\`\`
TY  - DATA
AU  - Smith, John
AU  - Doe, Jane
TI  - Dataset Name: Comprehensive Description
PY  - 2025
PB  - Zenodo
DO  - 10.5281/zenodo.XXXXX
UR  - https://doi.org/10.5281/zenodo.XXXXX
ER  -
\`\`\`

### Attribution Requirements

When using this dataset, please:

1. Cite the dataset using the citation above
2. Include the DOI in your bibliography
3. Mention the version number used
4. Link to the original dataset repository

## Support and Contact

### Reporting Issues

Found a problem with the data? Please:

1. Check existing issues: [Issue Tracker URL]
2. Open a new issue with:
   - Version number
   - Description of the problem
   - Steps to reproduce (if applicable)
   - Expected vs. actual behavior

### Questions and Discussion

- **Email**: [maintainer@example.com]
- **Discussion Forum**: [Forum URL]
- **GitHub Issues**: [Issues URL]

### Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for:
- How to report issues
- How to suggest improvements
- Code of conduct

### Maintainers

- **[Name]** - [Role] - [Email]
- **[Name]** - [Role] - [Email]

### Acknowledgments

This dataset was created with support from:
- [Funding source 1]
- [Funding source 2]
- [Contributing organization 1]
- [Contributing organization 2]

Special thanks to [individuals or groups who contributed].

---

**Last Updated**: 2025-11-24  
**Dataset Version**: 2.0.0  
**Documentation Version**: 2.0.0
```

---

## Additional Resources

- [Datasheet for Datasets](https://arxiv.org/abs/1803.09010) - Framework for documenting datasets
- [Data Documentation Initiative (DDI)](https://ddialliance.org/) - Standards for research data
- [Schema.org Dataset](https://schema.org/Dataset) - Structured metadata format
- [FAIR Principles](https://www.go-fair.org/fair-principles/) - Findable, Accessible, Interoperable, Reusable data

