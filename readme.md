# GPT-LogSpotLight

Welcome to GPT-LogSpotLight, a unified suite of applications built on Python and Streamlit, harnessing the capabilities of OpenAI's language models for specialized log analysis. This umbrella solution encapsulates a variety of tools, each designed for a unique log type or use case, transforming raw log data into actionable insights. With GPT-LogSpotLight, users can interactively dialogue with the logs, extracting valuable insights about activities on their tenant.

## Overview

GPT-LogSpotLight is a comprehensive platform hosting a multitude of applications, each honed to analyze a distinct type of log. These applications are built on the robust foundation of OpenAI's language models, including the current GPT-3.5-turbo-16k and future iterations like GPT-4. The objective of GPT-LogSpotLight is to offer a versatile and scalable solution for log analysis, capable of evolving alongside advancements in AI technology.

The inaugural application under this suite is LogSpectra-SecurityEvents. This Python-based application leverages Microsoft's Graph API to fetch security event logs and employs OpenAI's GPT-3.5-turbo-16k model for analysis, based on user queries. It offers a user-friendly interface for seamless interaction with the data and extraction of valuable insights.

## Applications

- **LogSpotlight-SecurityEvents:** A Python application that fetches event logs from Microsoft's Graph API and utilizes OpenAI's GPT-3.5-turbo-16k model for user query-based analysis.

## Getting Started

To utilize an application within the GPT-LogSpotLight suite, please refer to the ReadMe.md file within each application's directory for specific instructions. The applications are built on Python and require various libraries (check the provided `requirements.txt` file in each application's directory).

## Future Developments

GPT-LogSpotLight is envisioned to expand with more applications, each tailored to a unique log type or use case. Planned enhancements include integration with Azure OpenAI Service and Office 365 Management API, and the introduction of a data pre-processing step to accommodate larger alert volumes. The suite is also designed to adapt to future OpenAI models, ensuring its continued relevance and effectiveness.

## License

This project is licensed under the terms of the MIT license.
