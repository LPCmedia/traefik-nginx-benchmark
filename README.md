# Traefik vs Nginx vs HA Benchmark

install wrk : https://github.com/wg/wrk

```
# Traefik v3.2 with fastproxy
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8000/bench

# Nginx
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8001/bench

# HA Proxy
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8002/bench

# Pure Whoami
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8003/bench
```