Created by running

```sh
# Create a nx monorepo
# - react standalone
# - CSS
# - vite testing
npx create-nx-workspace acme --e2eTestRunner=none --nxCloud=skip --workspaceType=standalone  --preset=react-standalone --appName=acme --bundler=vite --style=css

cd acme
# Add nx-wrapped remix
npm install --save-dev @nx/remix

# Create a remix app
npx nx g @nx/remix:app myapp --unitTestRunner=vitest --e2eTestRunner=none
npx nx build myapp

# Setup tailwind in the remix app
npx nx g @nx/react:setup-tailwind --project=myapp
```
