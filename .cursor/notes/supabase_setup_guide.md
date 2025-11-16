# Supabase Local Setup Guide for Outline

## Overview

This guide helps you configure Outline to use your local Supabase instance instead of the default Postgres setup.

## Supabase Connection Details

From your Supabase local setup, you have:

- **Database URL**: `postgresql://postgres:postgres@127.0.0.1:54322/postgres`
- **API URL**: `http://127.0.0.1:54321`
- **Studio URL**: `http://127.0.0.1:54323` (Supabase Dashboard)
- **GraphQL URL**: `http://127.0.0.1:54321/graphql/v1`

## Environment Configuration

Add these variables to your `.env` or `.env.development` file:

```bash
# Database Configuration (Supabase Local)
DATABASE_URL=postgresql://postgres:postgres@127.0.0.1:54322/postgres

# Required Secrets (generate new ones for production!)
SECRET_KEY=d1e95afff8d4147aed99ddb2c1c651ba5cf459ffaa23a739bb8b0be3c8703628
UTILS_SECRET=fa7d99ad4b99059d57e4713fe3eef6f231ab0b9b306aed54cd1dc364e7acc7ff

# Application URL
URL=http://localhost:3000

# Redis Configuration (if using docker-compose)
REDIS_URL=redis://127.0.0.1:6379

# Environment
NODE_ENV=development
```

## Next Steps

1. **Update your `.env` file** with the configuration above

2. **Run database migrations** to set up the Outline schema:

   ```bash
   yarn db:migrate
   ```

3. **Start Redis** (if not already running):

   ```bash
   docker-compose up -d redis
   ```

   Or if you're using Supabase's Redis, configure `REDIS_URL` accordingly.

4. **Start the Outline development server**:

   ```bash
   yarn dev:watch
   ```

5. **Access Supabase Studio** (optional):
   - Open http://127.0.0.1:54323 in your browser
   - This gives you a visual interface to manage your database

## Important Notes

- **Port Conflict**: Supabase uses port `54322` for Postgres (not the default `5432`), so it won't conflict with your docker-compose Postgres if you have it running.

- **Database Name**: The default Supabase database is `postgres`. If you want to use a different database name, you can create one in Supabase Studio and update the `DATABASE_URL`.

- **Secrets**: The `SECRET_KEY` and `UTILS_SECRET` above are for local development only. Generate new ones for production using:

  ```bash
  openssl rand -hex 32
  ```

- **Migrations**: Outline uses Sequelize migrations. Make sure to run `yarn db:migrate` before starting the app.

## Troubleshooting

- **Connection Issues**: Make sure Supabase is running (`supabase status` in your `everyday-kb` directory)
- **Migration Errors**: Check that the database is accessible and the user has proper permissions
- **Port Conflicts**: Ensure ports 54321-54324 are available

## Useful Supabase Commands

```bash
# Check Supabase status
cd everyday-kb
supabase status

# Stop Supabase
supabase stop

# Start Supabase
supabase start

# Reset database (WARNING: deletes all data)
supabase db reset
```
