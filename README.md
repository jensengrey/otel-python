# otel-python

# documentation

* https://opentelemetry.io/docs/instrumentation/python/
* https://opentelemetry.io/docs/instrumentation/python/cookbook/
* https://github.com/open-telemetry/opentelemetry-python/tree/stable/docs/examples

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

Look for a `my-hello-service` in the Jaeger UI (**hint there is a small bug in the python code you need fix**).

<img width="1251" alt="jaeger-trace-python-5-trace" src="https://user-images.githubusercontent.com/46599294/216196445-6507360b-0ad0-434c-a677-2c28e57cf5e0.png">


# launch jaeger

```
#!/bin/bash

# filename: start-jaeger.sh

set -eux;

docker run --name jaeger \
  -e COLLECTOR_ZIPKIN_HOST_PORT=:9411 \
  -p 5775:5775/udp \
  -p 6831:6831/udp \
  -p 6832:6832/udp \
  -p 5778:5778 \
  -p 16686:16686 \
  -p 14268:14268 \
  -p 14250:14250 \
  -p 9411:9411 \
  jaegertracing/all-in-one:1.22

```



