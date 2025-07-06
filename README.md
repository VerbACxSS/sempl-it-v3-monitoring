# SEMPL-IT V3 monitoring
This is the monitoring module of SEMPL-IT, a web app designed to simplify Italian administrative document using different fine-tuned LLMs.

## WebApp
The SEMPL-IT web app consists of the following repositories:
- Frontend: [GitHub Repository](https://github.com/VerbACxSS/sempl-it-v3-frontend)
- Backend: [GitHub Repository](https://github.com/VerbACxSS/sempl-it-v3-backend)
- Monitoring Module: [GitHub Repository](https://github.com/VerbACxSS/sempl-it-v3-monitoring)
- Inference Module: [GitHub Repository](https://github.com/VerbACxSS/sempl-it-v3-inference)
- LLMs Collection: [HuggingFace Collection](https://huggingface.co/collections/VerbACxSS/sempl-it-v3-awq-6817ea4f843804006965f110)

## Getting started
### Pre-requisites
This web application is developed using FastAPI framework. The following software are required to run the application:
* Python (tested with version 3.9.18)
* Pip (tested with version 23.2.1)

Alternatively, you can use a containerized version by installing:
* Docker (tested on version 27.3.1)

### Configuration
The application can be configured using the following environment variable:
```
PYTHONUNBUFFERED=1
MONITORING_API_KEY=...
```

### Using `python` and `pip`
Create python virtual environment
```shell
python3 -m venv venv
```
Activate the virtual environment
```shell
source venv/bin/activate   # Linux/macOS
./venv/Scripts/activate    # Windows
```
Install all dependencies in requirements.txt
```shell
pip install -r requirements.txt
```
Start the server
```shell
python -m uvicorn app.app:app --host=0.0.0.0 --port=30011 --log-level=info --workers=2 --timeout-keep-alive=120
```

### Using `docker`
Run the application using `docker compose`
```sh
docker compose up --build -d
```

## Usage
The web application will be running at `http://localhost:30010` by default.

## Built with
* [FastAPI](https://fastapi.tiangolo)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
This contribution is a result of the research conducted within the framework of the PRIN 2020 (Progetti di Rilevante Interesse Nazionale) "VerbACxSS: on analytic verbs, complexity, synthetic verbs, and simplification. For accessibility" (Prot. 2020BJKB9M), funded by the Italian Ministero dell'Università e della Ricerca.
