![Logo](https://assets-global.website-files.com/644f39b5d9996380f70dfa0f/644f429a2303d7148ead8765_AllotracLogo_SIDE%20BY%20SIDE%20-%20NAVY.svg)

# 2024 UOW Hackathon powered by Allotrac

Welcome to the Allotrac resource repository for the 2024 UOW Hackathon!

As a major sponsor of the event, Allotrac have provided a variety of operational datasets & tooling to allow hackathon participants to interact with, hack-on and develop for real world use cases in an existing market. The hope is that this will provide a fertile ground for tackling the problem statements that have been set for the event.

Further more, Allotrac will soon be launching it's public developer marketplace which will allow any intrepid entrepreneurs to easily launch their project direct to an established market with an appetite for automation, optimization and insights.

This repository contains several useful things for getting your hackathon project off the ground, including:

- Access to the Allotrac.io product suite & GraphQL API
- An example operational dataset
- An example image dataset

Participants are encouraged to utilize these resource for experimentation and the development of their projects.

## Hackathon Themed Tracks

### AI & Data

**Prize pool:** $3000 cash

Leverage the power of AI to enable non-technical users to extract value from operational datasets.

### Computer Vision

**Prize pool:** $2000 cash

Utilise computer vision technology to extract meaningful insights from image data, enabling rapid analysis and interpretation for enhanced decision-making and situational awareness across various applications and industries.

### API Integrations

**Prize pool:** $2000 cash + [Baseline traineeship](https://baselinejs.com/)

Combine a variety of existing public API functionality to generate new and meaningful utility greater than the sum of the parts.

### Gamification

**Prize pool:** $2000 cash

Leverage elements of game principles and design in non-game contexts to encourage the desired behaviour or outcome and rewarding those behaviours

### iAccelerate Business Plan

**Prize pool:** $1000 cash + [iAccelerate Scholarships](https://www.iaccelerate.com.au/scholarships/) + [Free online programs from HEX](https://www.startwithhex.com/)

Create a business plan outlining a vision for a company which can tackle a specific societal problem by submission time day 2.

## Some context on Allotrac

Allotrac is a cloud-based transport management software designed for the logistics and transportation industry. It offers a range of features to streamline operations, enhance visibility, and optimize efficiency in managing fleets, drivers, jobs, and compliance requirements. Some of the key features typically associated with Allotrac include:

- Job Management: Allotrac helps in efficiently managing transport jobs from creation to completion, including scheduling, assigning, and tracking.

- Fleet Management: It provides tools for monitoring and managing fleets, including vehicle tracking and performance analytics.

- Compliance Management: Allotrac assists in ensuring regulatory compliance by automating processes related to driver and vehicle compliance, such as fatigue management and safety checks.

- Real-time Visibility: Users can gain real-time visibility into their operations through dashboards and reports, allowing for better decision-making and resource allocation.

- Integration Capabilities: Allotrac often integrates with other systems such as ERP (Enterprise Resource Planning) software, accounting software, and telematics systems to provide a comprehensive solution for transport management.

Learn more [here](https://www.youtube.com/watch?v=axSHViIHqwE) or [here](https://allotrac.com.au) or approach one of our event attendees!

## Allotrac Developer Guide + API Docs

For documentation on how to use the Allotrac.io developer portal and GraphQL API [click here](https://jodatechnology.atlassian.net/wiki/external/ODUxYmFjZGExNTQ0NGUwYzhkOGFlMTdiMDUyOTBjYjk)

## Operational Dataset Overview

To get started, clone or download this repository to your local machine:

`git clone https://github.com/mgallotrac/hackathon2024`

Once you have the dataset locally, you can begin exploring the files and incorporating them into your project. Remember to adhere to the licensing terms outlined in the LICENSE.md file.

The dataset is structured into several CSV files, organized within the `csv-dataset` folder. Each CSV file contains specific data relevant to the operations of an example Allotrac site. Here is a list of the files available in the dataset:

- `customer.csv` - Example Allotrac Site Customers
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
![http://allotrac-hackathon-datasets.s3-website-ap-southeast-2.amazonaws.com/images/1701303743_881056_image_img_proof_881056_0.jpg](http://allotrac-hackathon-datasets.s3-website-ap-southeast-2.amazonaws.com/images/1701303743_881056_image_img_proof_881056_0.jpg)

# External Data Repositories

In addition to the provided dataset, participants are encouraged to leverage external data repositories such as [Kaggle](https://www.kaggle.com) and [AWS Data Exchange](https://aws.amazon.com/data-exchange/) to enhance their projects. External data can complement the provided dataset and enrich the solutions developed during the hackathon.
