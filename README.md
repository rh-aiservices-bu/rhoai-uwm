# RHOAI Metrics Dashboard for Single Serving Models

Enable RHOAI User Workload Metrics for Single Serving Models

## Prerequisites

- OpenShift 4.10 or later
- OpenShift AI 2.10+ installed
- OpenShift AI KServe installed and configured
- NVIDIA GPU Operator installed and configured

## Installation

* [Configure Monitoring for the Single Model Serving Platform](https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/2.11/html/serving_models/serving-large-models_serving-large-models#configuring-monitoring-for-the-single-model-serving-platform_serving-large-models)
* [Configure GPU Monitoring Dashboard](https://docs.nvidia.com/datacenter/cloud-native/openshift/23.9.2/enable-gpu-monitoring-dashboard.html)
* [Install the RHOAI Metrics Grafana and Dashboards for Single Serving Models](./rhoai-uwm-grafana/README.md)

## Usage

Grab the Grafana route and open it in a browser:

```md
NS="user-grafana"
GRAFANA_URL=$(oc get route -n $NS grafana-route -o jsonpath='{.spec.host}')
echo $GRAFANA_URL
```

- **vLLM Model Metrics Dashboard**: Provides Model metrics for vLLM Single Serving Models dashboard.

![vLLM Dashboard 1](./assets/dashboard1.png)

- **vLLM Service Performance Dashboard**: Provides Service Performance metrics for vLLM Single Serving Models dashboard.

![vLLM Dashboard 2](./assets/dashboard2.png)

- **OpenVino Service Model Metrics Dashboard**: Provides metrics for OpenVino Single Serving Models

![vLLM Dashboard 4](./assets/dashboard4.png)

- **OpenVino Model Metrics Dashboard**: Provides Service Performance metrics for OpenVino Single Serving Models.

![vLLM Dashboard 3](./assets/dashboard3.png)
