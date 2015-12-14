Ecpy ext demo
=============

This package provides a template for creating Ecpy extensions packages. An
extension package is used to extend the capabilities of the main Ecpy
application through plugins.

This README gives a brief overview of what needs to be edited in the template.
For more details about the mechanism behind extension packages please refer to
the Ecpy documentation.

The package contains a number of files and two subfolders :

Files :

- setup.py : This is the installation file. You should edit the name of the
  project, and other informations as you see fit. Note that following the main
  Ecpy project the authors are listed in the AUTHORS file and the licence is
  set to BSD. By default, the package declare an extension to the entry point
  'ecpy_package_extension' which to the 'list_manifests' function found into
  the __init__.py module of the ecpy_ext_demo package. You can make it point to
  any function of your choice or leave the default setting.
  For more details about the working of setup scripts please refer to the
  setuptools documentation.
- AUTHOR : File listing the authors and contributors to the project.
- CHANGES : changelog listing changes between versions.

The following files can be left untouched.

- LICENCE : Copy of the licence under which the software is distributed.
- setup.cfg : configuration file.
- .gitignore : Files that git (version control system) should ignore.
- .gitattributes : git configuration.
- .coveragerc : coverage report configuration (when running tests).

Folders :

- ecpy_ext_demo : this is the folder where to add your code and that you SHOULD
  rename. Inside it you will three files :
    - __init__.py : this module defines a single function 'list_manifests' that
      should return a list of all the manifest that should be registered. You
      can remove if you made the entry point points to another function.
    - manifest.enaml : this module defines the plugin manifest which lists the
      contribution of a plugin to the application. You can write your manifest
      in this file or another it does not matter as long as 'list_manifest' (or
      its equivalent) return the manifests you want to register.
    - version.py : a simple module defining the version of the package. You
      should edit the name
- tests : in this folder you can add unit test for your package (if you do so
  it might make sense to configure a Continuous integration system for your
  package, Ecpy relies on Tracis CI). By default the tests check that the
  extension package is correctly detected by Ecpy. To work this requires the
  package to be INSTALLED (works in develop mode).

You can also add documentation for your package. The usual tool to use is
sphinx and the source for the documentation should be located under a 'docs'
folder.

