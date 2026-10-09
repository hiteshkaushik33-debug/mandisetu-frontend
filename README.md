# Frontend

One Next.js application with separately owned role modules:

- `users/`: public marketplace and buyer panel.
- `seller/`: supplier panel, products, leads, subscription and claim responses.
- `admin/`: marketplace administration, reviews and reporting.
- `shared/`: reusable UI, providers, state, types and styles.
- `src/app/`: Next.js route files and layouts that load the role modules.

From the project root run `npm.cmd run dev` or `npm.cmd run build -w frontend`.
The public homepage, `/buyer/*`, `/seller/*`, and `/admin/*` routes stay on the same application and port. This preserves the shared browser preview data and current links; these folders are not separate deployments.

The global design styles are in `shared/styles/globals.css`. shadcn/ui aliases and TypeScript aliases point to the new folders. Backend code and Prisma live outside this folder, in `../backend/`.
