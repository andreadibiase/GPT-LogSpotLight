# LogSpotLight-SecurityEvents

This repository contains the code for an Alert Logs Analyzer application called LogSpotLight-SecurityEvents. The application is built using Python, Streamlit, OpenAI's GPT-3.5-turbo-16k model, and Microsoft's Graph API.

## Overview

LogSpotLight-SecurityEvents is a Streamlit application that fetches alert event logs from Microsoft's Graph API and uses OpenAI's GPT-3.5-turbo-16k model to analyze the alerts based on user queries.

The application performs the following steps:

1. Fetches an access token from Microsoft's OAuth2 endpoint.
2. Uses the access token to fetch alerts from Microsoft's Graph API.
3. Displays the alert logs in the Streamlit application.
4. Takes a user query as input.
5. Uses OpenAI's GPT-3.5-turbo-16k model to analyze the alert logs based on the user query.
6. Displays the analysis result in the Streamlit application.

## Limitations

Due to the current limitations of the GPT-3.5-turbo-16k model, it's not possible to ingest all the Alerts but only a few that stay within the limit of the 16k tokens. However, Microsoft Graph API supports the `$filter` OData query parameter, which allows you to retrieve a subset of a collection. This can be used to filter the results from the API call according to your needs. Here the filter is set on "Top 8".

## Instructions

To implement the Event Log Analyzer, follow these steps:

1. Clone the repository to your local machine.
2. Install the necessary Python packages (check the provided `requirements.txt` file in each application's directory).
3. Replace `'Insert your OpenAi Key'`, `'App Client Id'`, `'App Client Secret'`, and `'Tenant Id'` in the code with your actual OpenAI key, App Client ID, App Client Secret, and Tenant ID respectively.
4. Run the Streamlit application: streamlit run app.py
5. Open your web browser and navigate to `localhost:8501` to view the application.
6. Wait for the alerts to be fetched by the Graph API, then enter your query in the text box and press Enter to analyze the event logs.

## Documentation

For more information on how to use the `$filter` query parameter with Microsoft Graph API, refer to the [official documentation](https://learn.microsoft.com/en-us/graph/filter-query-parameter?tabs=http).

## License

This project is licensed under the terms of the MIT license.

## Planned Enhancements

1. **Azure OpenAI Service Integration:** The intention is to integrate the application with the Azure OpenAI Service. This will allow the application to leverage the advanced capabilities of Azure OpenAI and its seamless integration with other Azure services.

2. **Data Pre-processing for Token Limitation:** Due to the current model's token limitation, it's only possible to process a limited number of alerts (currently 8). The plan is to introduce a data pre-processing step to reduce the number of tokens in each item. This will increase the number of alerts that can be analyzed by the model.

3. **Office 365 Management API Integration:** The goal is to broaden the application's scope beyond event analysis. By integrating with the Office 365 Management API, the application will be able to ingest audit logs, providing more comprehensive insights.
