# OC4IDS Registry

This repository contains the register of published [OC4IDS](https://standard.open-contracting.org/infrastructure/latest/en/) datasets.

The OC4IDS Reigstry is built using [DataTig](https://www.datatig.com/).

## Viewing the data

Go to the [DataTig UI](https://opendataservices.github.io/oc4ids-registry/datatig/) to view the register.

## Pulling data using the API

Go to [DataTig API page](https://opendataservices.github.io/oc4ids-registry/datatig/api.json) to see the available API endpoints.

For example, you can use the endpoint `https://opendataservices.github.io/oc4ids-registry/datatig/type/dataset/records_api.json`, to get the list of registered datasets.

## Updating the register

Information about each dataset is stored in a YAML file, where the name of the file is used as the ID of the dataset.

To update an existing dataset, update the YAML file for that dataset. To add a new dataset, create a new YAML file. The [datatig.yaml](./datatig.yaml) file shows the schema.

You can also use web forms [for existing datasets](https://opendataservices.github.io/oc4ids-registry/datatig/type/dataset/) or [new datasets](https://opendataservices.github.io/oc4ids-registry/datatig/type/dataset/newweb/) instead of editing the YAML. When editing expisting records, you may have to click on "properties" and select to add all the fields you want to edit.

Next, raise a pull request with your changes. The pull request will run a job that checks that the YAML file is in the correct format. Once the pull request is merged to the `live` branch, another job will publish it, making it available in the UI and via the API.
