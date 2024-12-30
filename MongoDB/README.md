# PowerSync + MongoDB Self Host Template

A template docker-compose file that starts a PowerSync Service and MongoDB instance.

## Setup the environment variables
Copy the `.env.template` file in this directory and update the variables accordingly if needed:

```bash
cp .env.template .env
```

# Run
```bash
docker-compose up -d
```

The PowerSync service is available at `http://localhost:8080` if the `PS_PORT` variable is not changed.

# Healthchecks

See [Healthchecks](https://powersync.mintlify.app/self-hosting/lifecycle-maintenance/healthchecks#liveness) in our official docs for more information on the healthchecks.