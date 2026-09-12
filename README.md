# AI Bootcamp 5 - Agentic AI Using the OpenAI Swarm Framework

This repository contains hands-on activities for building multi-agent workflows with the [OpenAI Swarm](https://github.com/openai/swarm) framework. The notebooks demonstrate agent instructions, function tools, handoffs, shared conversation state, web scraping, audience-specific copywriting, and data-analysis agents.

## Activities

### Activity 1: Marketing workflow with handoffs

[Open the notebook](AI_First_Day_6_Activity_1.ipynb)

Builds a marketing content workflow with three agents:

- **Lead Generator Bot** identifies target audiences, search trends, and competitors.
- **SEO Bot** performs keyword and search-visibility analysis.
- **Content Creator Bot** produces engaging, SEO-friendly marketing content.

The lead generator hands work to the SEO bot, which then hands the result to the content creator. The example prompt asks the workflow to create a blog about prompt engineering.

### Activity 2: Multi-agent marketing debate

[Open the notebook](AI_First_Day_6_Activity_2.ipynb)

Implements a four-turn debate between two alternating agents:

- **SEO Specialist** argues for organic traffic, keyword strategy, and long-term visibility.
- **Social Media Advocate** argues for engagement, virality, and audience targeting.

The agents pass control back and forth while discussing the best strategy for launching a new product.

### Activity 3: Website research and campaign copy

[Open the notebook](AI_First_Day_6_Activity_3.ipynb)

Uses [Firecrawl](https://www.firecrawl.dev/) to scrape a website in Markdown and routes the results through a marketing workflow:

1. The **User Interface Agent** receives a website URL.
2. The **Website Scraper Agent** collects the website content.
3. The **Analyst Agent** identifies marketing insights.
4. Copywriter agents create campaign messaging.

The notebook also experiments with general, women-centric, Gen Z, and millennial copywriters using `https://www.axa.com.ph/` as the example website.

### Project: Insight Hive sales analysis

[Open the notebook](project/insight_hive.ipynb) | [View the dataset](project/ai%20first%20sales%20data%20-%20sales.csv)

The `Insight Hive` notebook combines Pandas analysis with Swarm agents. It imports and cleans sales data, converts currency fields, checks data quality, and analyzes:

- traffic sources, visits, pageviews, transactions, and conversion rates;
- behavior and revenue by device type;
- marketing campaign return on investment;
- average revenue per transaction and pricing patterns;
- monthly sales performance; and
- historical revenue trends with a moving-average forecast.

Specialized agents perform each analysis, and a **Final Insights Agent** combines the results into a consolidated report.

## Setup

Create or activate a Python environment, then install the notebook dependencies:

```bash
pip install git+https://github.com/openai/swarm.git
pip install openai firecrawl-py numpy pandas matplotlib
```

Activity 3 requires a Firecrawl API key. All notebooks require an OpenAI API key. Set credentials as environment variables before running the notebooks:

```bash
# PowerShell
$env:OPENAI_API_KEY = "your-openai-api-key"
$env:FIRECRAWL_API_KEY = "your-firecrawl-api-key"
```

Then open the notebooks in Jupyter or VS Code and run the cells in order. Replace hard-coded placeholder keys in the notebooks with environment-variable-based credentials before executing them.

## Repository layout

```text
.
├── AI_First_Day_6_Activity_1.ipynb
├── AI_First_Day_6_Activity_2.ipynb
├── AI_First_Day_6_Activity_3.ipynb
├── project/
│   ├── ai first sales data - sales.csv
│   └── insight_hive.ipynb
└── README.md
```

