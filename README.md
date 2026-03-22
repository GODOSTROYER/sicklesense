# Sicklesense: Sickle Cell Detection App 🩺

Sicklesense is an AI-powered application designed to detect sickle cells from microscopic images of red blood cells. By leveraging Deep Learning, this tool aims to provide rapid preliminary screening for sickle cell anemia, a genetic blood disorder.

## 🌟 Highlights

- 🧠 **AI-Powered Analysis**: Utilizes a custom-trained **TensorFlow** Convolutional Neural Network (`sickle_cell_model.h5`) for accurate detection from red blood cell images.
- 🚀 **End-to-End Pipeline**: Includes complete Jupyter notebooks detailing the machine learning lifecycle:
  - `Preprocessing.ipynb`: Image preparation and data augmentation.
  - `Train_test_valid_split.ipynb`: Structuring the dataset.
  - `Model.ipynb`: Model architecture design, training, and evaluation.
- 🌐 **Interactive UI**: Built with **Streamlit** for a seamless user experience, allowing for easy image uploads and instant AI predictions.
- 🩺 **Actionable Health Insights**: In the event of a positive detection, the app automatically provides immediate health precautions and emergency helpline numbers for both India and the USA.

## 🏆 Achievements & Recognition

- 🥉 **3rd Place at University of Miami Horizon AI Hackathon 2025**: Awarded $1,000 prize for an AI-driven healthcare screening project aimed at improving early sickle-cell detection in underserved areas.
  - _Source:_ [Punekar News — MIT-ADT Students Secured Third Place at Horizon AI Hackathon](https://www.punekarnews.in/?s=Horizon+AI+Hackathon)
- 🏅 **Top 100 Startups / Top Presenters**: Recognized at IIT Delhi’s College Youth Ideathon.
  - _Source:_ [IIT Delhi College Youth Ideathon](https://www.google.com/search?q=IIT+Delhi+College+Youth+Ideathon+Sickle+Cell)

## 📊 Impact & Performance

Sicklesense is designed to radically lower the barrier to rapid sickle-cell diagnosis:

| Feature                       | Benefit/Impact                                                                        |
| :---------------------------- | :------------------------------------------------------------------------------------ |
| **🔬 Digital Microscopy**     | Uses a low-cost digital microscope to capture high-resolution images of blood smears. |
| **🧠 AI/ML Model**            | Detects sickled cells with **>92% accuracy**.                                         |
| **⚡ Rapid Results**          | Diagnosis in minutes, not days.                                                       |
| **🔋 Low-Power Hardware**     | Runs on battery; suitable for rural clinics and accessible via API.                   |
| **🧑‍⚕️ Health Worker Friendly** | Easy to operate without a trained pathologist on-site.                                |
| **💰 High Affordability**     | Over 95% reduction in cost! Test cost is approximately **₹75/test**.                  |
| **🌍 Telepathology Support**  | Images can be securely reviewed remotely by specialists.                              |

## 🏗️ Architecture & Pipeline Flow

The project follows a standard machine learning lifecycle, from raw data to a deployed application:

1.  **Data Preprocessing (`Preprocessing.ipynb`)**: Raw cell images are cleaned, resized (to match the 224x224 input size expected by the model), and normalized.
2.  **Dataset Handling (`Train_test_valid_split.ipynb`)**: The processed data is split into training, validation, and testing sets to ensure robust model evaluation.
3.  **Model Training (`Model.ipynb`)**: A TensorFlow/Keras model is defined and trained on the preprocessed images. The final trained weights are saved to `sickle_cell_model.h5`.
4.  **Application Inference (`app.py`)**: The Streamlit interface loads the `sickle_cell_model.h5` model. When a user uploads an image, the app preprocesses it identical to the training phase and passes it to the model to predict the presence of sickle cells.

## 💻 Setup & Installation (Local Development)

Follow these steps to run the interactive Sicklesense application locally:

### 1. Prerequisites

Ensure you have Python installed (preferably version 3.8+).

### 2. Clone the Repository

```bash
git clone https://github.com/GODOSTROYER/sicklesense.git
cd sicklesense/code/Sickle-cell
```

### 3. Install Dependencies

Install the required Python packages using pip:

```bash
pip install -r requirements.txt
```

_(Dependencies include `streamlit`, `tensorflow`, `numpy`, `pillow`, and `opencv-python-headless`)_

### 4. Run the Application

Start the Streamlit server:

```bash
streamlit run app.py
```

The application will open in your default web browser (typically at `http://localhost:8501`).

---

_Disclaimer: This tool is for informational and preliminary screening purposes only and should not replace professional medical diagnosis._
