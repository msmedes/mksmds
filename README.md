# mksmds

Minimal static site deployed via Kamal 2.

## Structure

```
public/
  index.html    # Landing page
  resume.html   # Resume
```

## Setup

1. Update `config/deploy.yml`:
   - Replace `YOUR_HETZNER_IP` with your server IP
   - Replace `YOUR_DOMAIN` with your domain

2. Set your Docker registry password:
   ```bash
   export KAMAL_REGISTRY_PASSWORD=your_token
   ```

3. Deploy:
   ```bash
   kamal setup   # First time
   kamal deploy  # Subsequent deploys
   ```

## Local Preview

```bash
docker build -t mksmds .
docker run -p 8080:80 mksmds
# Visit http://localhost:8080
```

