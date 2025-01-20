This repository demonstrates a common error in Dockerfiles: the failure to copy or create necessary files before execution.

The `Dockerfile` attempts to run a Python script (app.py), but this script is missing from the build context.  The `DockerfileFixed` shows the correct solution.

To reproduce the bug:
1. Clone this repo.
2. Try to build the original Dockerfile:  `docker build -t buggy-app .`
3. Build the fixed Dockerfile: `docker build -t fixed-app .`