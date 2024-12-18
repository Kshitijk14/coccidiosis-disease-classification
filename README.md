# Chicken Disease (Coccidiosis) Classification

This project implements a deep learning model to classify chicken diseases, specifically focusing on coccidiosis detection through image analysis.

## Features

- Deep learning-based classification of chicken diseases
- Interactive web interface using Flask
- Containerized application using Docker
- MLOps integration with DVC (Data Version Control)
- Real-time model monitoring with TensorBoard

## Project Structure

The project follows a modular and maintainable structure:

1. `config.yaml` - Main configuration file
2. `secrets.yaml` - Sensitive configuration (not tracked in git)*
3. `params.yaml` - Model parameters and hyperparameters
4. `entity/` - Core data entities and models
5. `src/config/` - Configuration management
6. `components/` - Reusable project components
7. `pipeline/` - Data and training pipelines
8. `main.py` - Application entry point
9. `dvc.yaml` - DVC pipeline configuration

## Installation and Setup

1. Clone the repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Training and Monitoring

1. Start TensorBoard for monitoring:
```bash
tensorboard --logdir artifacts/prepare_calbacks/tensorboard_log_dir/
```

2. Use DVC for experiment tracking and pipeline management:
```bash
# Initialize DVC
dvc init

# Run the complete pipeline
dvc repro

# Visualize pipeline dependencies
dvc dag
```

### Running the Application

#### Local Development

1. Start the Flask application:
```bash
python app.py
```

2. Access the application:
- Main interface: `http://127.0.0.1:8080/`
- Model training endpoint: `http://127.0.0.1:8080/train/`

#### Docker Deployment

1. Build the Docker image:
```bash
docker build -t kshitiijj/coccidiosis_classifier .
```

2. View available images:
```bash
docker images
```

3. Run the container:
```bash
docker run -p 8080:8080 kshitiijj/coccidiosis_classifier
```

4. View running containers:
```bash
docker ps
```

5. Push to Docker Hub:
```bash
docker push kshitiijj/coccidiosis_classifier:latest
```

## Contributing

Feel free to open issues and pull requests for improvements (especially for the model architecture).
