<div align="center">

# N8N Workflows Collection

**Production-ready automation workflows with AI agents, data processing, and multi-platform integrations**

[![N8N](https://img.shields.io/badge/N8N-Latest-FF6D5A)](https://n8n.io/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-blue)](https://github.com/pgvector/pgvector)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED)](https://www.docker.com/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

<a name="toc"></a>

[Features](#features) •
[Getting Started](#getting-started) •
[Workflows](#workflows) •
[Configuration](#configuration) •
[API Integration](#api-integration) •
[Troubleshooting](#troubleshooting)

</div>

---

<a name="overview"></a>

## 📋 Overview

A comprehensive collection of production-ready N8N workflows featuring AI agents, web scraping, data processing, and multi-platform integrations. Built with PostgreSQL + pgvector for vector storage, automated backups, and enterprise-grade monitoring capabilities.

<a name="features"></a>

## ✨ Features

- 🤖 **AI Agents** - ReAct agents with web scraping, database chat, and knowledge assistants
- 🌐 **Web Scraping** - FireCrawl integration with automated data extraction
- 📊 **Data Processing** - ETL pipelines with transformation and validation
- 🗄️ **Database Integration** - PostgreSQL, Snowflake, and MongoDB connections
- 📧 **Email Automation** - Gmail workflows with attachment handling
- 📈 **Content Marketing** - OpenAI + Ahrefs integration for content intelligence
- 🔄 **Automated Backups** - GitHub integration for workflow version control
- 📋 **API Documentation** - Swagger spec generation for webhook endpoints
- 🔐 **Secure Configuration** - Environment-based secrets management

[Back to Top](#toc)

<a name="getting-started"></a>

## 🚀 Getting Started

### Prerequisites

- Docker and Docker Compose
- PostgreSQL with pgvector extension
- N8N account or self-hosted instance
- API keys for integrated services (OpenAI, FireCrawl, etc.)

### Installation

```bash
# Clone the repository
git clone https://github.com/shawnmcrowley/n8n_workflows.git

# Navigate to project directory
cd n8n_workflows

# Copy environment template
cp .env.example .env

# Edit .env with your configuration
# Configure database, API keys, and service URLs

# Start services with Docker Compose
docker-compose up -d
```

### Access Points

- **N8N Interface**: http://localhost:5678
- **PostgreSQL**: localhost:5432
- **PgAdmin**: http://localhost:5050

[Back to Top](#toc)

<a name="workflows"></a>

## 🔧 Available Workflows

### AI Agents & Chat

- **`ai-agent-that-can-scrape-webpages-.json`** - ReAct agent with web scraping capabilities
- **`ai-agent-to-chat-with-snowflake-database-.json`** - Database query agent for Snowflake
- **`chat-with-a-database-using-ai-.json`** - General database chat interface
- **`rag-chatbot-for-company-documents-using-google-drive-and-gemini-.json`** - Document Q&A system
- **`build-an-all-source-knowledge-assistant-with-claude,-rag,-perplexity,-and-drive-.json`** - Multi-source knowledge base

### Web Scraping & Data Extraction

- **`firecrawl_webscraping-.json`** - FireCrawl-powered web scraping
- **`scrape-and-summarize-webpages-with-ai-.json`** - AI-powered content summarization
- **`webscraping-with-file-updates-and-email-with-attachment-.json`** - Automated scraping with notifications
- **`automated-web-scraping:-email-a-csv,-save-to-google-sheets-&-microsoft-excel-.json`** - Multi-format data export

### Data Processing & ETL

- **`etl-pipeline-for-text-processing-.json`** - Text processing and transformation
- **`data-transformation-techniques-.json`** - Advanced data manipulation patterns
- **`master-data-transformation-with-the-complete-set-node-guide-.json`** - Comprehensive transformation guide
- **`postgres_api_workflow_with_email-postgres.json`** - PostgreSQL API with email notifications

### Content & Marketing

- **`automated-content-marketing-intelligence-with-openai,-ahrefs-&-multi-platform-integration-.json`** - Content marketing automation
- **`url-parsing-and-email-generation-.json`** - URL analysis and email generation

### Integrations & Utilities

- **`gmail_workflow-.json`** - Gmail automation and processing
- **`google_sheets_workflow-.json`** - Google Sheets integration
- **`google_sheets_subworkflow-.json`** - Modular Sheets operations
- **`google_sheets_mcp_server-.json`** - MCP server for Sheets
- **`snowflake-cortex-ai-with-chat-snowflake.json`** - Snowflake Cortex AI integration

### System & Maintenance

- **`automated-daily-workflow-backup-to-github-.json`** - Automated GitHub backups
- **`back-up-your-n8n-workflows-to-github-.json`** - Manual backup workflow
- **`generate-swagger-specs-for-workflows-that-have-webhooks-and-create-html-file-on-disk-.json`** - API documentation generator
- **`error-worflow-.json`** - Error handling and monitoring

### MCP Servers

- **`build-your-own-n8n-workflows-mcp-server-.json`** - N8N MCP server implementation
- **`mcp-email-sender-MCP with Trigger.json`** - Email MCP server with triggers

[Back to Top](#toc)

<a name="configuration"></a>

## 🔧 Configuration

### Environment Variables

Edit `.env` file with your configuration:

```env
# PostgreSQL Configuration
DB_TYPE=postgresdb
DB_POSTGRESDB_HOST=postgres
DB_POSTGRESDB_PORT=5432
DB_POSTGRESDB_DATABASE=vectordb
DB_POSTGRESDB_SCHEMA=n8n_schema
DB_POSTGRESDB_USER=postgres
DB_POSTGRESDB_PASSWORD=postgres

# PgAdmin Settings
PGADMIN_DEFAULT_EMAIL=admin@admin.com
PGADMIN_DEFAULT_PASSWORD=admin

# N8N Settings
N8N_HOST=localhost
N8N_PROTOCOL=http
N8N_WEBHOOK_URL=http://localhost:5678
GENERIC_TIMEZONE=America/New_York

# API Keys
N8N_API_KEY=your_n8n_api_key
FIRECRAWL_API_KEY=your_firecrawl_key
OPENWEATHER_KEY=your_openweather_key
ALPHA_VANTAGE_KEY=your_alpha_vantage_key
```

### Docker Compose Services

The `docker-compose.yml` includes:

- **N8N**: Workflow automation platform
- **PostgreSQL**: Database with pgvector extension
- **PgAdmin**: Database administration interface

### SSL Certificates

Custom certificates can be placed in the `certificates/` directory:

```
certificates/
├── zscalar.crt
├── zscalar.pem
└── 9d934b85.0@
```

[Back to Top](#toc)

<a name="api-integration"></a>

## 🔑 API Integration

### Supported Services

- **OpenAI/Snowflake Cortex**: AI model integration
- **FireCrawl**: Web scraping and content extraction
- **Google Sheets**: Spreadsheet automation
- **Gmail**: Email processing and automation
- **Snowflake**: Data warehouse operations
- **Ahrefs**: SEO and content marketing data
- **OpenWeather**: Weather data integration
- **Alpha Vantage**: Financial market data

### Webhook Endpoints

Many workflows expose webhook endpoints for external integration:

```bash
# Example webhook URL structure
http://localhost:5678/webhook/workflow-name

# Test webhook
curl -X POST http://localhost:5678/webhook/test \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello World"}'
```

### Swagger Documentation

Use the Swagger generation workflow to create API documentation:

1. Import `generate-swagger-specs-for-workflows-that-have-webhooks-and-create-html-file-on-disk-.json`
2. Execute the workflow
3. Access documentation at `swagger-html/index.html`

[Back to Top](#toc)

<a name="project-structure"></a>

## 📁 Project Structure

```
n8n_workflows/
├── workflows/                  # N8N workflow JSON files
│   ├── ai-agent-*.json        # AI agent workflows
│   ├── automated-*.json       # Automation workflows
│   ├── data-*.json           # Data processing workflows
│   ├── etl-*.json            # ETL pipeline workflows
│   ├── gmail_*.json          # Gmail integration workflows
│   ├── google_sheets_*.json  # Google Sheets workflows
│   ├── mcp-*.json            # MCP server workflows
│   ├── postgres_*.json       # PostgreSQL workflows
│   ├── rag-*.json            # RAG and knowledge workflows
│   ├── scrape-*.json         # Web scraping workflows
│   └── snowflake-*.json      # Snowflake integration workflows
├── certificates/              # SSL certificates
├── swagger-html/             # Generated API documentation
├── docker-compose.yml        # Docker services configuration
├── .env                      # Environment variables
├── .gitignore               # Git ignore rules
└── README.md                # This file
```

[Back to Top](#toc)

<a name="usage"></a>

## 📖 Usage

### Importing Workflows

1. Access N8N interface at http://localhost:5678
2. Navigate to **Workflows** → **Import from File**
3. Select desired JSON file from `workflows/` directory
4. Configure credentials and environment variables
5. Test and activate the workflow

### Running Workflows

```bash
# Via N8N API
curl -X POST http://localhost:5678/api/v1/workflows/{id}/execute \
  -H "X-N8N-API-KEY: your_api_key" \
  -H "Content-Type: application/json"

# Via webhook (if configured)
curl -X POST http://localhost:5678/webhook/workflow-name \
  -H "Content-Type: application/json" \
  -d '{"data": "your_data"}'
```

### Monitoring & Debugging

- **Execution History**: View in N8N interface under **Executions**
- **Logs**: Check Docker logs with `docker-compose logs n8n`
- **Database**: Query execution data in PostgreSQL
- **Error Handling**: Use the error workflow for centralized error management

[Back to Top](#toc)

<a name="troubleshooting"></a>

## 🔧 Troubleshooting

### Common Issues

**N8N Not Starting**

```bash
# Check Docker logs
docker-compose logs n8n

# Verify environment variables
cat .env

# Restart services
docker-compose restart
```

**Database Connection Issues**

```bash
# Test PostgreSQL connection
docker-compose exec postgres psql -U postgres -d vectordb

# Check pgvector extension
SELECT * FROM pg_extension WHERE extname = 'vector';
```

**Workflow Import Errors**

- Verify JSON file format is valid
- Check for missing credentials
- Ensure required nodes are available
- Update N8N to latest version

**API Key Issues**

- Verify API keys in `.env` file
- Check credential configuration in N8N
- Test API endpoints independently
- Review rate limits and quotas

### Performance Optimization

- **Database Indexing**: Ensure proper indexes on frequently queried tables
- **Memory Allocation**: Adjust Docker memory limits for large workflows
- **Concurrent Executions**: Configure N8N execution limits
- **Caching**: Implement caching for frequently accessed data

[Back to Top](#toc)

<a name="security"></a>

## 🔐 Security Best Practices

- **Environment Variables**: Never commit `.env` file to version control
- **API Keys**: Use N8N credential system for sensitive data
- **Network Security**: Configure firewall rules for production deployment
- **Database Security**: Use strong passwords and connection encryption
- **Webhook Security**: Implement authentication for webhook endpoints
- **Regular Updates**: Keep N8N and dependencies updated

[Back to Top](#toc)

<a name="contributing"></a>

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-workflow`)
3. Export your workflow from N8N as JSON
4. Add workflow to appropriate category in `workflows/`
5. Update this README with workflow description
6. Commit your changes (`git commit -m 'Add amazing workflow'`)
7. Push to the branch (`git push origin feature/amazing-workflow`)
8. Open a Pull Request

[Back to Top](#toc)

<a name="license"></a>

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

[Back to Top](#toc)

<a name="acknowledgments"></a>

## 🙏 Acknowledgments

- N8N team for the powerful automation platform
- PostgreSQL and pgvector for vector database capabilities
- OpenAI for AI model integration
- FireCrawl for web scraping capabilities
- Open source community for inspiration and contributions

[Back to Top](#toc)

<a name="contact"></a>

## 📧 Contact

**Shawn M. Crowley**

- 📧 Email: [shawn.crowley@lycra.com](mailto:shawn.crowley@lycra.com)
- 🔗 LinkedIn: [@shawnmcrowley](https://www.linkedin.com/in/shawnmcrowley)
- 🐦 Twitter: [@shawnmcrowley](https://twitter.com/shawnmcrowley)
- 🔗 GitHub: [n8n_workflows](https://github.com/shawnmcrowley/n8n_workflows)

[Back to Top](#toc)

---

<div align="center">
Made with ❤️ using N8N, PostgreSQL, and Docker
</div>