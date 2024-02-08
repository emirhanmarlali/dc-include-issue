# Results

## docker compose version == `v2.24.5`

If `foo` service defined in `./foo.docker-compose.yml` and that file is included in `./docker-compose.yml` output is **wrong**.

Command:

```bash
docker compose version
```

Result:

```
Docker Compose version v2.24.5
```

Command:

```
docker compose config
```

Output:

```
services.foo conflicts with imported resource
```

**Expected** Output:

```
name: demo
services:
  foo:
    image: ubuntu:lunar
    networks:
      default: null
  main:
    image: alpine
    networks:
      default: null
networks:
  default:
    name: demo_default
```
