## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## Setting Up Postgres with Docker

To run this project locally, you need a PostgreSQL database. The simplest way is using Docker.

1. **Install [Docker](https://docs.docker.com/get-docker/) if you haven't already.**

2. Launch a Postgres container using the following command:

   ```bash
   docker run --name nextjs-postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres
   ```

   This will:
   - Start a `postgres` container named `nextjs-postgres`
   - Set the default password to `postgres`
   - Expose Postgres on your local machine's `5432` port

3. Update your project's environment variables (e.g. `.env.local`) with a database URL like:

   ```
   DATABASE_URL=postgresql://postgres:postgres@localhost:5432/postgres
   ```

---

## Seeding the Database

The starter includes a database seed route at `/seed` to help populate your database with test data.

1. **Start your Next.js development server:**

   ```bash
   npm run dev
   # or
   yarn dev
   ```

2. **Visit [`http://localhost:3000/seed`](http://localhost:3000/seed) in your browser.**

   This will create the required tables and insert the initial users, customers, invoices, and revenue data.

---

Your database is now ready. You can begin working on the project!
