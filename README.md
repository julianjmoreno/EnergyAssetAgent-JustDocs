> [!IMPORTANT]  
> The conntent and views expressed here are personal and meant for information/education purposes only and not representative of my employer directly or indirectly and not investment advice. Any mention of company names are for illustrative examples only.
> 
# Vol1 - Chat with my Energy Asset Unstructured Data
Energy companies generate and rely on vast volumes of unstructured data—geological surveys, well logs, seismic interpretations, and production or drilling reports—often stored in PDFs, scanned documents, and images. These data sources hold critical insights, but extracting and interpreting them manually is time-consuming, error-prone, and inefficient.<br><br>

This solution leverages the power of Microsoft Copilot and Copilot Studio to create intelligent, task-specific Copilot Agents that transform how energy companies access, analyze, and act on their unstructured data. By combining advanced AI, natural language understanding, and seamless integration with Microsoft 365 and Azure ecosystems, these agents automate data extraction, interpretation, and insight generation—turning static documents into dynamic intelligence.

With this solution, energy professionals can:

- Ask natural language questions and receive grounded, document-backed answers.
- Summarize complex reports like drilling logs or seismic interpretations in seconds.
- Visualize trends and anomalies across wells, formations, and time periods.
- Collaborate across teams using familiar tools like Teams, SharePoint, and Power BI.
- Whether you're optimizing drilling performance, assessing geological risk, or streamlining regulatory reporting, this Copilot-powered solution brings clarity, speed, and intelligence to your most valuable but underutilized—data assets.

## Before you start
If you would like to get a live demonstration of the solution and some guidance, please feel free to request it here:

[![Button Shield1]][Shield1]
<br>

<!---------------------------------------------------------------------------->
[Button Shield1]: https://img.shields.io/badge/Request_Your_Personal_Demo_Here-37a779?style=for-the-badge
[License]: LICENSE
[Shield1]: https://forms.office.com/r/He2aHtAVMf
[KBD]: Types/KBD.md
[#]: #

## Important Reading
Before you deep dive, we strongly recommend you get familiar with the following subjects so you better understand the reasons behind and the value proposition of this solution accelerator:

|  Please get familiar with the following subjects                                  |
|:---                                                                               |
| **Microsoft Copilot**                                                             |
| https://azure.microsoft.com/en-us/products/data-manager-for-energy/               |
| **Microsoft Copilot Studio**                                                      |
| https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio/       |


## Understanding the Solution
The following diagram illustrates the main components on this solution accelerator
<br> <br>


![Solution Accelerator Diagram](https://github.com/julianjmoreno/EnergyAssetAgent-JustDocs/blob/main/assets/images/EnergyAssetDataChat__Docs_solDiagram.png "Solution Accelerator Diagram")

**A. The data landscape:** represented by structured data sources (like Azure Data Manager for Energy), including metadata and bulk data, and corresponding unstructured data sources (such as SharePoint or OneDrive, which contains data in the form of PDFs, Excel files, PowerPoint presentations, and other documents).

**B. The Copilot Agent:** Specialized set of AI tools built to handle specific processes or solve business challenges, in this case to provide access to data insights from unstructured data store on corresponding SharePoint site. 
They also automate tasks, analyze data, make decisions, and adapt to new challenges.
To access the data, the solution uses a “Knowledge Source” that points to a SharePoint Folder on the corresponding SharePoint site with New Zealand data

## Getting Started
### Prerequisites 

<ol>
  <li> <p> <strong>Get your dataset ready</strong> <br>
    For this solution, we have selected the New Zealand Petroleum Exploration Data Pack as dataset, which features a large selection of open-file seismic and well data, interpretation projects, reports and studies. To understand more about the New Zealand Petroleum Exploration Data Pack here:<br>
    https://www.nzpam.govt.nz/maps-geoscience/petroleum-datapack<br>
  <strong>Note:</strong> You could also use your own datasets.</p>
  </li>
  <li> <p> <strong>Make available your unstructured data in SharePoint</strong> <br>
   Make sure that unstructured data in a form of geological, well, seismic interpretation and other reports as PDFs and images, are available on a SharePoint site / folder of your preferences. Please remember that the Agent will respect the entitlement / secutiry configuration in place.<br>
    </p>
  </li>
</ol>

## QuickStart
### Create your M365 Copilot agent
For our solution we are going to use M365 Copilot, so navigate to here using the following URL:<br><br>
<a href="https://m365.cloud.microsoft/">https://m365.cloud.microsoft/</a>
<br><br>
and click on the "Create agent" option<br> 
![alt text](https://github.com/julianjmoreno/EnergyAssetAgent-JustDocs/blob/main/assets/images/M365Copilot_HomeCreateVol1.png)

You will land into the  Agent “creation screen” by conversational assistance, lets skip and go to configure by clicking the "Configure" option.

![alt text](https://github.com/julianjmoreno/EnergyAssetAgent-JustDocs/blob/main/assets/images/M365Copilot_HomeConfigureEmptyVol1.png)

On this screen, you would be able to to provide Agent name, description, instructions, connect knowledge sources (only URLs to internet or SharePoint folders), and optionally, define starter prompts to guide user interactions. <br> <br>

Start by providing a meaningful name, description… as well as an icon !!! We will now go setting up some instructions. <br><br>

***Copilot Agent Instructions***<br>

M365 Copilot Agent instructions will direct the behavior of the agent, including its tasks and how it completes them. Here is a sample set of instructions that we have used to set up the agent.<br><br>

These instructions helps the data agent understand your data by writing a detailed system prompt. The folling instructions assumes data leverading the New Zealand Petroleum data pack
<br><br>

```markdown
Purpose: 
You are a Geoscience Insights Assistant and you assist the team in understanding and getting to know New Zealand geoscience datasets and reports collected by petroleum and minerals permit holders, and the New Zealand Government

Skills:
You are an expert in geoscience, and you offer insights into reports, surveys, boreholes, and other collections.

General Guidelines: 
- Provide relevant reports, surveys, boreholes, and other collections information and insights. 
- Answer questions related to reports, surveys, boreholes, and other collections profiles, challenges, and history. 
- Ensure responses are accurate and helpful. 
- Maintain a friendly and professional tone. 
- Avoid sharing sensitive or confidential information. 
- Emphasize accuracy in all responses. 
- Communicate in a formal manner. 
- Ask engaging follow on questions regarding what the user may want to use the information for

```
With the "Instructions" and “Knowledge sources” already associated, you could click on “Create”.<br><br>

![alt text](https://github.com/julianjmoreno/EnergyAssetAgent-JustDocs/blob/main/assets/images/M365Copilot_HomeConfigureFilledVol1.png)

> [!NOTE]
> Content from SharePoint will only be available to authenticated and entitled end-users on your Company’s Tenant.
<br>

# Lets test the agent
Lets use the following prompt:<br><br>

```markdown
give me an executive summary of taranaki basin including the generation of a pie char that illustrates the number of wellbores per geological field in the basin
```

![alt text](https://github.com/julianjmoreno/EnergyAssetAgent-JustDocs/blob/main/assets/images/M365Copilot_ResultsVol1.png)

## Sample Prompts
Here are some sample promts for this dataset<br>
https://github.com/julianjmoreno/EnergyAssetAgent-ADME/blob/main/assets/chatSamplePrompts.MD<br><br>
