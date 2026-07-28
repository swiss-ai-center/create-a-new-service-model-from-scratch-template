# model-creation

<!-- TODO 1: Update the description of the service and the link to the documentation. -->
_Check the [related documentation](https://docs.swiss-ai-center.ch/reference/core-concepts/service/) for more information._

Use uv as the dependency manager for the model project. Initialize this
directory with a `pyproject.toml` and add DVC as a project dependency when the
model experiment is implemented.

Until `model-creation/pyproject.toml` exists, GitHub Actions skips model
training and artifact upload but continues to lint and test the serving
template. Release and deployment jobs remain disabled because there is no
model artifact to package.
