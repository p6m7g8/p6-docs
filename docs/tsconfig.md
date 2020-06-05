The configuration from the base file are loaded first, then overridden by those in the inheriting config file. All relative paths found in the configuration file will be resolved relative to the configuration file they originated in

# Composite - composite
The composite option enforces certain constraints which make it possible for build tools (including TypeScript itself, under --build mode) to quickly determine if a project has been built yet.

When this setting is on:

The rootDir setting, if not explicitly set, defaults to the directory containing the tsconfig.json file.
All implementation files must be matched by an include pattern or listed in the files array. If this constraint is violated, tsc will inform you which files weren’t specified.
declaration defaults to true
You can find documentation on TypeScript projects in the handbook.

# Declaration Map - declarationMap
Generates a source map for .d.ts files which map back to the original .ts source file. This will allow editors such as VS Code to go to the original .ts file when using features like Go to Definition.

You should strongly consider turning this on if you’re using project references.

# Incremental - incremental
Tells TypeScript to save information about the project graph from the last compilation to files stored on disk. This creates a series of .tsbuildinfo files in the same folder as your compilation output. They are not used by your JavaScript at runtime and can be safely deleted. You can read more about the flag in the 3.4 release notes.

To control which folders you want to the files to be built to, use the config option tsBuildInfoFile.

# Out Dir - outDir

# Remove Comments - removeComments

#Strict Checks
We recommend using the option strict to opt-in to every possible improvement as they are built.


Default
false, unless strict is set

# No Implicit Any - noImplicitAny
In some cases where no type annotations are present, TypeScript will fall back to a type of any for a variable when it cannot infer the type.

# Strict - strict
Default false


With "baseUrl": "./" inside this project TypeScript will look for files starting at the same folder as the tsconfig.json.

import { helloWorld } from "hello/world"

# Paths - paths
A series of entries which re-map imports to lookup locations relative to the baseUrl, there is a larger coverage of paths in the handbook.

paths lets you declare how TypeScript should resolve an import in your require/imports.

# Root Dirs - rootDirs
Using rootDirs, you can inform the compiler that there are many “virtual” directories acting as a single root. This allows the compiler to resolve relative module imports within these “virtual” directories, as if they were merged in to one directory.

# Type Roots - typeRoots
By default all visible ”@types” packages are included in your compilation. Packages in node_modules/@types of any enclosing folder are considered visible.

When you have this option set, by not including a module in the types array it:

Will not add globals to your project (e.g process in node, or expect in Jest)
Will not have exports appear as auto-import recommendations
This feature differs from typeRoots in that it is about specifying only the exact types you want included, whereas typeRoots supports saying you want particular folders.

# No Fallthrough Cases In Switch - noFallthroughCasesInSwitch

# No Implicit Returns - noImplicitReturns
When enabled, TypeScript will check all code paths in a function to ensure they return a value.

# No Unused Locals - noUnusedLocals
Report errors on unused local variables.

# No Unused Parameters - noUnusedParameters
Report errors on unused parameters in functions.

# Allow Unreachable Code - allowUnreachableCode
Set to false to disable warnings about unreachable code. These warnings are only about code which is provably unreachable due to the use of JavaScript syntax, for example:

# Allow Unused Labels - allowUnusedLabels
Set to false to disable warnings about unused labels.

# Declaration Dir - declarationDir
Offers a way to configure the root directory for where declaration files are emitted.

# Force Consistent Casing In File Names - forceConsistentCasingInFileNames
TypeScript follows the case sensitivity rules of the file system it’s running on. This can be problematic if some developers are working in a case-sensitive file system and others aren’t. If a file attempts to import fileManager.ts by specifying ./FileManager.ts the file will be found in a case-insensitive file system, but not on a case-sensitive file system.

When this option is set, TypeScript will issue an error if a program tries to include a file by a casing different from the casing on disk.

# Imports Not Used As Values - importsNotUsedAsValues
This flag controls how import works, there are 3 different options:

remove: The default behavior of dropping import statements which only reference types.
preserve: Preserves all import statements whose values or types are never used. This can cause imports/side-effects to be preserved.
error: This preserves all imports (the same as the preserve option), but will error when a value import is only used as a type. This might be useful if you want to ensure no values are being accidentally imported, but still make side-effect imports explicit.
This flag works because you can use import type to explicitly create an import statement which should never be emitted into JavaScript.

# List Emitted Files - listEmittedFiles
Print names of generated files part of the compilation to the terminal.

This flag is useful in two cases

# List Files - listFiles
Print names of files part of the compilation. This is useful when you are not sure that TypeScript has included a file you expected.

For example:

# No Error Truncation - noErrorTruncation

# No Resolve - noResolve
By default, TypeScript will examine the initial set of files for import and <reference directives and add these resolved files to your program.

If noResolve is set, this process doesn’t happen. However, import statements are still checked to see if they resolve to a valid module, so you’ll need to make sure this is satisfied by some other means.

# Trace Resolution - traceResolution
When you are trying to debug why a module isn’t being included. You can set traceResolutions to true to have TypeScript print information about its resolution process for each processed file.

You can read more about this in the handbook.

tsc --build --clean
