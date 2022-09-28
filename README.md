# docker-wrtc-whep

Docker container of a WHEP endpoint based on `@eyevinn/wrtc-egress` library.

Example docker-compose file:

```
version: "3.7"

services:
  egress:
    image: eyevinntechnology/wrtc-whep:latest
    network_mode: "host"
    environment:
      - PORT=8200
      - EXT_PORT=8200
      - SMB_URL=http://<SMB-HOST>:8280/conferences/
      - SMB_API_KEY=example
```

## Configuration

Default configuration can be changed by setting these environment variables:
- `PORT`
- `EXT_PORT`
- `HOSTNAME`
- `USE_HTTPS`
- `SMB_URL`
- `SMB_API_KEY`
- `PREFIX` (default is `/whep`)
