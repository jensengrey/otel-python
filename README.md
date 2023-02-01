# otel-python

# documentation

* https://opentelemetry.io/docs/instrumentation/python/

# install

```
git clone https://github.com/jensengrey/otel-python
cd otel-python
deactivate # if you already have a python env
python3 -m venv otelpy.env
source otelpy.env/bin/activate
pip install -r requirements.txt
```

# fire off a sample trace

```
python3 jaeger_tracing.py
```

<img width="1397" alt="jaeger-trace-python" src="https://user-images.githubusercontent.com/46599294/216155088-1fb47913-d63d-4e03-b67f-a8a681ddc024.png">




