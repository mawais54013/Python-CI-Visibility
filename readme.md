# Ci-Visibility For Python PyTest 
 
## Compatibility 
Supported Python interpreters:

Python >= 2.7 and >= 3.5
Supported test frameworks:

pytest >= 3.0.0
pytest < 5 when using Python 2


## Prerequisites
 [Install the Datadog Agent to collect tests data](https://docs.datadoghq.com/continuous_integration/setup_tests/agent/?tab=azurepipelines)

 <br/>

[Install the Python tracer](https://docs.datadoghq.com/tracing/setup_overview/setup/python/?tab=containers) 

Command:
```
pip install -U ddtrace
```
OR 
```
pip3 install ddtrace
```
## How to Use:
Install flask via pip3
```
pip3 install flask
```

Run pytest command below
```
DD_SERVICE=my-python-app DD_ENV=ci pytest --ddtrace
```

Likewise you can run the app witb the command below:
```
ddtrace-run python3 app.py
```

## Results:
Should be shown in datadog ci after a couple of minutes:
https://app.datadoghq.com/ci/test-runs?index=citest&start=1632627253983&end=1632630853983&paused=false

Working example output:
![image](/test.png)

## Documentation
https://docs.datadoghq.com/continuous_integration/setup_tests/javascript/?tab=jest 