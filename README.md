# powerlog

A no nonsense logging utility for Deno.

```ts
import { createLogger, setDefaultName, enableDebug } from "https://x.nest.land/powerlog@0.0.1/mod.ts";

// Set an optional default name.
setDefaultName("main");

// Enable or disable debug logs.
enableDebug(true);

const log1 = createLogger("overwrite the default name here if you want")

// Create a logger with no name.
const log2 = createLogger();

const logChild = log2.child("Create a child logger");
const logChildDepth = log1.child("create sub children easily with multiple args", "another child!");

const quickChildLogger = createLogger("name or empty string", ["easy way to make more child loggers"]);
```