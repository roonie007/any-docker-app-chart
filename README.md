## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add roonie007 https://roonie007.github.io/any-docker-app-chart

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo
roonie007` to see the charts.

To install the any-docker-app-chart chart:

    helm install RELEASE_NAME roonie007/any-docker-app-chart

To uninstall the chart:

    helm delete RELEASE_NAME

## Dev

First of all, go to the root of the project

To package one of the helm chart use:

    helm package .

Then you must update the helm repo index using

    helm repo index --url https://roonie007.github.io/any-docker-app-chart --merge index.yaml .
