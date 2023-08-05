## Steps towards packaging
1) Install Hatch: Using pip, you install Hatch with pip install hatch.

2) Create a New Hatch Project: Use hatch new my_package to create a new project with the necessary structure.

3) Specify Package Metadata: Edit the pyproject.toml file to add your package's metadata (e.g., name, version, license, authors).

4) Add Dependencies: Specify your package's dependencies in the pyproject.toml file under the [tool.hatch.dependencies] section.

5) Build the Package: Use hatch wheel to build your package, which creates a .whl file in the dist/ directory.

6) Publish the Package: Publish your package to PyPI using hatch release. You'll need to authenticate with your PyPI account.

7) Install Your Package: Once published, your package is available for installation via pip install my_package.
