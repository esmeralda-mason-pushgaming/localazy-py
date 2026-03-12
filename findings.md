

# Authentication
Project tokens or ...
Organization tokens are available only upon request. Contact us at team@localazy.com for beta access.

# CLI
CLI has separate read and write access tokens.

Requires project to contain a [localazy.json](./localazy.json)

Keys can either be in the main json or in a dedicated [localazy.keys.json](./localazy.keys.json)

After installing the cli there is only one command to download all available translation files into the location specified int he main json.

The keys downloaded seem to ignore the hidden status.


# Typescript package
test implemented in foxy branch [localazy-test](https://github.com/gsi-io/foxy-game-editor/tree/localazy-test)

```
import { ApiClient, Project, I18nJson, Locales } from '@localazy/api-client';

const json: I18nJson = { en: { tooltip: 'Elegant unicorn' } };

const api: ApiClient = new ApiClient({ authToken: 'your-project-token' });
const project: Project = await api.projects.first();
// const file: File = await api.import.json({ project, json: json });
const fr: I18nJson = await api.export.json({ project, file, langs: [Locales.FRENCH] });
``` 
With TS api there is no way to restrict developers from pushing destructive changes using the module.

Key.hidden seems to not be populated from the website for this API too. 

## Documentation 
https://github.com/localazy/api-client/blob/main/docs/api-client-reference.md#files

# decision

