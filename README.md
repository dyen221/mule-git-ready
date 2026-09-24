# mule-git-ready

## Local setup

1. Clone the repository and switch to `dev`.
2. Copy `src/main/resources/config.properties.example` to `src/main/resources/config.properties`.
3. Replace the Salesforce client ID and secret with values from your Salesforce connected app.
4. Set the Salesforce token URL and Redis connection values for your environment.
5. Run the application from Anypoint Studio.

The real `config.properties` file is ignored by Git and must never be committed. The application loads it through `configuration-properties` in `src/main/mule/sfcdc.xml`.

## Branch workflow

Use `dev` for active work. Promote tested changes to `production`, then promote releases to `main`.

```powershell
git switch dev
git pull
git add -A
git commit -m "Describe the change"
git push
```
