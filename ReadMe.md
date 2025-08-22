# End-to-End Realtime Weather Streaming with Azure: A Data Engineering Project

This project was designed to build a real-time weather streaming data engineering solution using a wide range of Azure services and Microsoft Fabric.

## Project Overview

The main objective of this project is to create a **real-time weather report** system that continuously updates weather information such as temperature, conditions, air quality, and other relevant details for a preferred location. A key feature is the ability to receive **real-time email alerts** for any unexpected extreme weather conditions, enabling prompt responses to emergencies.

This project covers the entire data engineering pipeline from data injection, streaming, processing, loading, to reporting and alerting, providing a full end-to-end solution.

---

## Key Features

- Real-time weather data ingestion from a free Weather API with up to 1 million API calls per month (one call every 3 seconds).
- Data injection using **Azure Databricks** and **Azure Functions** to demonstrate different approaches and architectural decision-making.
- Streaming data ingestion and processing using **Azure Event Hub** and **Microsoft Fabric Event Stream**.
- Loading streaming data into a **Eventhouse (Kusto DB)** optimized for time series and streaming data.
- Real-time interactive weather dashboard built with **Power BI**.
- Real-time alerting system using **Data Activator** to send email notifications on extreme weather conditions.
- Secure storage of sensitive information such as API keys and tokens using **Azure Key Vault**.
- Cost management and optimization insights for Azure resources used in the project.

---

## Architecture

The project architecture consists of the following components:

1. **Data Source**: Weather API providing real-time weather data.
2. **Data Injection**: Azure Databricks and Azure Functions connect to the Weather API, pull data, and send events to Azure Event Hub.
3. **Event Streaming**: Azure Event Hub streams the weather data to Microsoft Fabric.
4. **Event Stream Pipelines**: Microsoft Fabric Event Stream captures streaming data from Event Hub, transforms it, and loads it continuously into the Eventhouse (Kusto DB).
5. **Data Storage**: Eventhouse (Kusto DB) stores time series weather data for real-time analytics.
6. **Reporting**: Power BI dashboard provides an interactive, real-time weather report.
7. **Alerting**: Data Activator monitors data and sends real-time email alerts for extreme weather conditions.
8. **Security**: Azure Key Vault securely manages sensitive credentials.
9. **Cost Management**: Analysis and optimization of resource costs.

---

## Tools and Technologies

![databricks](https://github.com/dpds-md/Weather/blob/main/icons/databricks.svg)

- **Azure Databricks**: For scalable data injection and processing.
- **Azure Functions**: Serverless compute for data injection.
- **Azure Event Hub**: High-throughput data streaming service.
- **Microsoft Fabric**: Real-time intelligence platform with Event Stream.
- **Kusto DB**: Real-time storage of weather data.
- **Power BI**: Real-time interactive dashboarding.
- **Data Activator**: Real-time alerting and notifications.
- **Azure Key Vault**: Secure storage of secrets.
- **Weather API**: Free tier API for real-time weather data.




---

## License

This project is licensed under the MIT License - see the LICENSE file for details.