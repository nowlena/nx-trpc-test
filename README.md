# NX tRPC v10 Test

Most basic implementation of:

- [NX](https://nx.dev/)
- [tRPC v10](https://trpc.io/)
- [Prisma](https://www.prisma.io/)

## Development

```bash
git clone git@github.com:nowlena/nx-trpc-test.git
cd nx-trpc-test
yarn
yarn start
```

## Directory Structure

```
.
├── apps
│   ├── frontend              # NextJS App
│   ├── frontend-e2e          # NextJS App E2E Tests
├── libs
│   ├── api                   # tRPC
│   ├── prisma                # Prisma
```

## Additional Comments

### Prisma Schema Location

Please note that the Prisma Schema location is reference within our root `package.json`. If you change the Schema location be sure to update this `package.json` entry as well so that the Prisma CLI can continue to function properly.

```json
"prisma": {
  "schema": "libs/prisma/schema.prisma"
},
```

### Prisma CLI Commands

With the current configuration you will likely want to run your Prisma CLI commands via `npx prisma [command]`.

You can certainly add your own [Nx run-commands](https://nx.dev/packages/workspace/executors/run-commands) to the `libs/prisma/project.json` if you'd like to use something like `nx run prisma:generate` instead to be consistent with the general Nx approach.
