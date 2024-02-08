# Results

## docker compose version == `v2.24.0`

If `foo` service defined in `./docker-compose.yml` output is **correct**.

---

Command:

```bash
docker compose version
```

Result:

```
Docker Compose version v2.24.0
```

---

Command:

```
docker compose config
```

Output:

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
