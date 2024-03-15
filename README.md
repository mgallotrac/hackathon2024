# Allotrac Dataset Repository

Welcome to the Allotrac Dataset Repository for the 2024 UOW Hackathon! This repository contains an example dataset provided by Allotrac Pty Ltd for use during the hackathon event. Participants are encouraged to utilize this dataset for experimentation and development of their projects.

## API Developer Guide

For documentation on how to use the Allotrac.io GraphQL API [click here](https://jodatechnology.atlassian.net/wiki/external/ODUxYmFjZGExNTQ0NGUwYzhkOGFlMTdiMDUyOTBjYjk)

## Dataset Overview

The dataset is structured into several CSV files, organized within the `csv-dataset` folder. Each CSV file contains specific data relevant to Allotrac's operations. Here is a list of the files available in the dataset:

- `customer.csv` - Example Allotrac Customers
- `delivery_type.csv` - Example delivery types
- `fleet.csv` - The Vehicle fleets for the example site
- `item.csv` - The list of products that are transported by the example customer (this is the catalogue, not the instantiated instances of items on a delivery)
- `location.csv` - The list of locations stored against allotrac contacts
- `state.csv` - Australian States
- `suburb.csv` - Australian Suburbs
- `truck.csv` - The vehicles attached to the Allotrac site
- `truck_home_location_data.csv` - A mapping of vehicles to locations where the trucks are parked overnight
- `truckclass.csv` - The various varieties of vehicles tracked in Allotrac
- `truckhistory.csv` - The GPS data of all vehicles in Allotrac during
- `msjob_activities.csv` - All job activities
- `msjob_activity_types.csv` - The lookup for the activity type mapping
- `msjob_history.csv` - All status changes for jobs
- `msjob_status.csv` - The lookup for the job statuses
- `msjob_pod.csv` - All proof of delivery documents for jobs
- `msjob_project.csv` - Projects (which can join a collection of jobs under a single instance)
- `msjobcustomer.csv` - Each line here represents an individual job done in Allotrac, this is the core table for workflow
- `msjobcusttoitems.csv` - Each line here maps an instantiated item to an instantiated job to allow for multiple items per job
- `msjobitems.csv` - The instantiated items for jobs
- `msprojectitems.csv` - The instantiated items for projects
- `mstrucktocust.csv` - The mapping from instantiated jobs to vehicles in the system

Feel free to explore and analyze these files to gain insights into Allotrac's business operations.

## POD Image Repository

The Proof of delivery images are also available as an image dataset. The entire dataset [can be downloaded here](https://allotrac-hackathon-datasets.s3.amazonaws.com/pop-pod-images.zip?AWSAccessKeyId=AKIASY2WFKX7SLJMMEFY&Signature=In23Mmz%2FZ0qU%2FedkTZWa2HQyCJw%3D&Expires=1710677728), however it's 26GB so be careful.

[An alternate download link can be found here.](https://allotrac-hackathon-datasets.s3.amazonaws.com/pop-pod-images.zip)

An alternative method for fetching images on demand is to access them directly from the domain: http://allotrac-hackathon-datasets.s3-website-ap-southeast-2.amazonaws.com/images/

POD filepaths can be found in the `csv-dataset/msjob_pod.csv` file. The column `filename` can be appended to the above domain to access the image. For example for the line:

```
7100236,881056,image/jpeg,296555,"width=""700"" height=""500""",1701303743_881056_image_img_proof_881056_0.jpg,2023-11-30 11:22:23,"-35.4054359,149.1674758",pickup,driver
```

The filepath key is `1701303743_881056_image_img_proof_881056_0.jpg`

Hence the image can be accessed at [http://allotrac-hackathon-datasets.s3-website-ap-southeast-2.amazonaws.com/images/1701303743_881056_image_img_proof_881056_0.jpg](http://allotrac-hackathon-datasets.s3-website-ap-southeast-2.amazonaws.com/images/1701303743_881056_image_img_proof_881056_0.jpg)

## External Data Repositories

In addition to the provided dataset, participants are encouraged to leverage external data repositories such as [Kaggle](https://www.kaggle.com) and [AWS Data Exchange](https://aws.amazon.com/data-exchange/) to enhance their projects. External data can complement the provided dataset and enrich the solutions developed during the hackathon.

## Usage

To get started, clone or download this repository to your local machine:

`git clone https://github.com/mgallotrac/hackathon2024`

Once you have the dataset locally, you can begin exploring the files and incorporating them into your project. Remember to adhere to the licensing terms outlined in the LICENSE.md file.

Happy hacking!
