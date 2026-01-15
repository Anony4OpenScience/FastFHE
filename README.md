# FastFHE

## How to run
### Prerequisites
Linux operative system, with at least 200GB of RAM.

In order to run the program, you need to install:
- `cmake`
- `g++` or `clang`
- `OpenFHE` ([how to install OpenFHE](https://openfhe-development.readthedocs.io/en/latest/sphinx_rsts/intro/installation/installation.html)), this work has been tested on v1.0.4

### 1) Build the project

Setup the project using this command:
```
mkdir build
cmake -B "build" -S FHEcontroller_CKKS_RESNET
Then build it using
```
cmake --build "build" --target
```

### 2) Execute the project

After building, go to the created `build` folder:

```
cd build
```
and run it with the following command:
```
./FHEcontroller_CKKS_RESNET
```

#### Some examples

The first execution should be launched with the `generate_keys`:
```
./FHEcontroller_CKKS_RESNET generate_keys
```
This command create the required keys and stores them in a new folder called `keys`, in the root folder of the project.

The default command creates a new context and classifies the default image in `inputs` file. We can, however, use custom arguments.
We can use a set of serialized context and keys with the argument `load_keys` as follows:

```
./FHEcontroller_CKKS_RESNET
```
