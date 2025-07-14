# Generative AI Project

A structured Generative AI project template built with FastAPI, designed for creating robust AI applications. This template follows best practices for maintainability, scalability, and reusability, incorporating database integration using SQLAlchemy and modular code organization.

## 🚀 Features

- **FastAPI Framework**: High-performance web framework for building APIs
- **Database Integration**: SQLAlchemy ORM with migration support
- **Modular Architecture**: Clean, organized code structure
- **Configuration Management**: YAML-based configuration files
- **Rate Limiting**: Built-in API rate limiting
- **Caching**: Intelligent caching for improved performance
- **Error Handling**: Comprehensive error handling system
- **Testing**: Unit tests for API and utility functions
- **Documentation**: Complete project documentation
- **Docker Support**: Ready-to-use containerization

## 📁 Project Structure

```
generative_ai_project/
├── config/
│   ├── __init__.py
│   ├── database_config.yml         # Database connection settings
│   ├── model_config.yml           # Model parameters
│   └── logging_config.yml         # Logging configurations
├── src/
│   ├── __init__.py
│   ├── api/
│   │   ├── __init__.py
│   │   ├── main.py                # FastAPI app initialization
│   │   ├── endpoints.py           # API routes
│   │   └── schemas.py             # Pydantic models for data validation
│   ├── db/
│   │   ├── __init__.py
│   │   ├── database.py            # SQLAlchemy engine and session
│   │   └── migrations/            # Database migration scripts
│   │       ├── __init__.py
│   │       └── version_1.py
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── rate_limiter.py        # API rate limiting
│   │   ├── cache_manager.py       # Caching logic
│   │   └── logger.py              # Logging utility
│   ├── handlers/
│   │   ├── __init__.py
│   │   └── error_handler.py       # Custom error handling
├── data/
│   ├── cache/                     # Cached responses
│   ├── prompts/                   # Prompt templates
│   └── embeddings/                # Precomputed embeddings
├── tests/
│   ├── __init__.py
│   ├── test_api.py                # API unit tests
│   └── test_utils.py              # Utility function tests
├── docs/
│   ├── __init__.py
│   ├── architecture.md            # Project architecture
│   └── api_reference.md           # API documentation
├── examples/
│   ├── basic_completion.py        # Simple text generation example
│   └── chain_prompts.py           # Chained prompt example
├── notebooks/
│   ├── prompt_testing.ipynb       # Prompt experimentation
│   └── model_analysis.ipynb       # Model performance analysis
├── requirements.txt               # Project dependencies
├── setup.py                       # Installation script
├── README.md                      # Project overview and setup guide
└── Dockerfile                     # Containerization setup
```

## 🏗️ Key Components

### Core Modules

- **`config/`**: YAML configuration files for database, model, and logging settings
- **`src/api/`**: FastAPI application files including routes and schemas
- **`src/db/`**: Database setup with SQLAlchemy and migration scripts
- **`src/utils/`**: Reusable utility functions for rate limiting, caching, and logging
- **`src/handlers/`**: Custom error handling logic

### Data & Resources

- **`data/`**: Storage for cached responses, prompt templates, and embeddings
- **`examples/`**: Sample scripts demonstrating basic and chained prompt usage
- **`notebooks/`**: Jupyter notebooks for prompt testing and model analysis

### Development & Testing

- **`tests/`**: Comprehensive unit tests for API and utility functions
- **`docs/`**: Project architecture and API reference documentation

## 🛠️ Prerequisites

- Python 3.8+
- Docker (for containerization)
- Git (for version control)

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/generative_ai_project.git
cd generative_ai_project
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Settings

Edit the configuration files as needed:
- `config/database_config.yml`
- `config/model_config.yml`
- `config/logging_config.yml`

### 4. Set up the Database

Run the migration scripts located in `src/db/migrations/`:

```bash
python src/db/migrations/version_1.py
```

### 5. Run the Application

```bash
uvicorn src.api.main:app --reload
```

The API will be available at `http://localhost:8000`

### 6. Explore Examples

Check the `examples/` directory for usage samples:

```bash
python examples/basic_completion.py
python examples/chain_prompts.py
```

## 🐳 Docker Setup

### Build the Docker Image

```bash
docker build -t generative-ai-app .
```

### Run the Container

```bash
docker run -p 8000:8000 generative-ai-app
```

## 🧪 Testing

Run the test suite:

```bash
pytest tests/
```

## 📋 Best Practices

This project follows these key principles:

- ✅ **YAML Configuration**: Use YAML files for all configuration settings
- ✅ **Error Handling**: Implement comprehensive error handling
- ✅ **Rate Limiting**: Apply rate limiting for all API endpoints
- ✅ **Modular Design**: Separate concerns with clear module boundaries
- ✅ **Caching**: Cache results appropriately for performance
- ✅ **Documentation**: Maintain up-to-date documentation
- ✅ **Testing**: Use notebooks and unit tests for validation

## 🔧 Development Tips

- Follow modular design principles for better maintainability
- Use Git for version control and collaborative development
- Keep documentation updated in the `docs/` directory
- Monitor API usage with the built-in logging utilities
- Experiment with prompts using the provided Jupyter notebooks

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📞 Support

For questions, issues, or contributions:

- Open an issue in the repository
- Contact the maintainers via the repository
- Check the `docs/` directory for detailed documentation

## 🔗 API Documentation

Once the application is running, visit:
- **Interactive API docs**: `http://localhost:8000/docs`
- **ReDoc documentation**: `http://localhost:8000/redoc`

---

**Built with ❤️ using FastAPI and modern Python practices**
