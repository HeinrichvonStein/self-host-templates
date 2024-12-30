# PowerSync + MySQL Self Host Template

A template docker-compose file that starts a PowerSync Service and MySQL instance.

## Setup the environment variables
Copy the `.env.template` file in this directory and update the variables accordingly if needed:

```bash
cp .env.template .env
```

## Update `init-scripts` (optional)
Update the user and password created in [mysql.sql](init-scripts/mysql.sql):
- user: `repl_user`
- password: `good_password`

```sql
-- Create a user with necessary privileges
CREATE USER 'repl_user'@'%' IDENTIFIED BY 'good_password';
```

# Run
```bash
docker-compose up -d
```

The PowerSync service is available at `http://localhost:8080` if the `PS_PORT` variable is not changed.

# Healthchecks

See [Healthchecks](https://powersync.mintlify.app/self-hosting/lifecycle-maintenance/healthchecks#liveness) in our official docs for more information on the healthchecks.