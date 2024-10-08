> [!IMPORTANT]  
> ModuleSpace was a temporary student-run company created as part of a project seminar at our high school. This seminar is designed to give students practical experience in business and project management. The company does not exist anymore. However, this repository will continue to be available


# ModuleSpaceRapid

Welcome to the official ModuleSpace Rapid repository on GitHub!

# What is ModuleSpaceRapid

ModuleSpaceRapid is a template for creating simple ExpressJs backends.

# History

This is a fragment of what was built to be the backend of our website - module-space.de, however, we decided that we'd go another route but didn't want to abandon our backend structure in case we can help someone out with creating a simple backend application, so we removed all our own code and published it as a template on GitHub.

# How to add Routes

- To add a Route, simply create a new file in the ```src/routes``` folder and call it ```{YOUR_ROUTE_NAME}.ts```

- Start editing the file and make sure to create a router object:
```
import { Router } from "express";
import { makeRoute } from "../transform/route";

const router: Router = Router();
const route: string = makeRoute(__filename);
```
- Add functionality:
```
router.get(route, (req, res) => {
    res.status(200).send("OK");
});
```

- Make sure to export the router as default:

```
export default router;
```

- Then import the route in index.ts, the main file of the project:

```
import myRouter from './routes/myroute';
```

- add your new route:

```
app.use('/', myRouter);
```

# Usage

Dev:
- Start dev with ```npm run dev```

Note that the server will automatically restart on code changes.

Build:
- Build the project: ```npm run build``` 
- Run compiled code: ```npm run start```

# License

The MIT License (MIT)
