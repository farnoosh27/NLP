## Steps towards packaging
1. Organize Your Code Into a Package Directory

2. Initialize Your Project as a Python Package

3. Create a pyproject.toml File



4. Build Your Package with Hatch
 * Install Hatch: pip install hatch
 * Use Hatch to build your project
* Navigate to your project's root directory (the directory containing pyproject.toml)
   * hatch build
5. Install Your Package Locally

```
pip install dist/my_project_src-0.1.0-py3-none-any.whl
```

or 
```
pip install -e .
```
## difference between them
  
  * pip install dist/my_project_src-0.1.0-py3-none-any.whl:

This command installs a specific pre-built wheel file (.whl) from the dist directory. A wheel file is a built package that can be installed without needing to compile anything or run any setup code. This command installs the package "as is" and any changes to the source code will not affect the installed package.

* pip install -e . (assuming you meant to include the .):

The -e flag installs the package in "editable" mode, often used in development. It means that instead of copying the files into the site-packages directory (where installed packages reside), pip will create a link to your source code directory. So, when you change the source code, those changes are immediately reflected in the installed package without needing to reinstall it.

In summary, the first command installs a specific built version of the package, while the second allows you to keep working on the code and see your changes reflected in the installed package without needing to rebuild and reinstall. The first command is more typical for installing production code, while the second is often used by developers working on the package.




