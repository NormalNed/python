<img src="https://cdn.freebiesupply.com/logos/large/2x/python-5-logo-svg-vector.svg" align="right" width="200"/>

# Python

Python is an interpreted, interactive object-oriented programming
language suitable (amongst other uses) for distributed application
development, scripting, numeric computing and system testing.  Python
is often compared to Tcl, Perl, Java, JavaScript, Visual Basic or
Scheme.  To find out more about what Python can do for you, point your
browser to http://www.python.org/.

# 🔨 Building
Below you will find anything you need to know.

## 💻 Windows

For a quick guide to building you can read [this documentation](https://cpython-core-tutorial.readthedocs.io/en/latest/build_cpython_windows.html) from Victor Stinner.

Python 2.7 uses Microsoft Visual Studio 2008, which is most easily obtained through an MSDN subscription. To use the build files in the PCbuild directory you will also need Visual Studio 2010, see the 2.7 readme for more details. If you have VS 2008 but not 2010 you can use the build files in the PC/VS9.0 directory, see the VS9 readme for details.
When installing Visual Studio 2017, select the Python development workload and the optional Python native development tools component to obtain all of the necessary build tools. If you do not already have git installed, you can find git for Windows on the Individual components tab of the installer.

Note If you want to build MSI installers, be aware that the build toolchain for them has a dependency on the Microsoft .NET Framework Version 3.5 (which may not be configured on recent versions of Windows, such as Windows 10). If you are building on a recent Windows version, use the Control Panel (Programs | Programs and Features | Turn Windows Features on or off) and ensure that the entry “.NET Framework 3.5 (includes .NET 2.0 and 3.0)” is enabled.
Your first build should use the command line to ensure any external dependencies are downloaded:

```PCBuild\build.bat```

After this build succeeds, you can open the PCBuild\pcbuild.sln solution in Visual Studio to continue development.

See the readme for more details on what other software is necessary and how to build.

## 🐧 Linux

```bash
$ ./configure
$ make
```

## 🍎 MacOS

```bash
brew install openssl xz
CPPFLAGS="-I$(brew --prefix openssl)/include" LDFLAGS="-L$(brew --prefix openssl)/lib" MACOSX_DEPLOYMENT_TARGET=10.6 ./configure
make```
