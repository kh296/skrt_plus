# skrt+

This is a minimal package to provide an integrated conda
environment for:

- [Scikit-rt](https://scikit-rt.github.io/scikit-rt/),
- [Ganga](https://github.com/ganga-devs/ganga),
- [ROOT](https://github.com/root-project/root).

## Prerequisites
1. If not already available, install [git](https://git-scm.com/download).

2. If not already avialable, install
[Miniconda](https://docs.conda.io/en/latest/miniconda.html).

## Environment creation

1. Clone this repository:
```
git clone https://github.com/kh296/skrt_plus
```

2. Create either the user environment or the developer environment.

   1. User environment

      - Create the environment with:
        ```
        cd skrt_plus
        conda env create --file environment.yml
         ```

2. Developer environment

   - Clone the repositories `scikit-rt` and `ganga-skrt`:
     ```
     git clone https://github.com/scikit-rt/scikit-rt
     git clone https://github.com/kh296/ganga-skrt
     ```

   - Create the environment with:
     ```
     cd skrt_plus
     conda env create --file environment-dev.yml
      ```
   
## Environment activation
   
Activate envrionment with:
```
conda activate skrt+
```

## Environment setup file for Ganga

Ganga jobs that use Scikit-rt must be accompanied by a setup
script for environment creation.  With the `skrt+` environment activated,
such a script can be created with:

```
create_setup -c <conda_home> -e skrt+ -o skrt_setup.sh
# <conda_home> is the path to the user's conda installlation.
# For more information, use: create_setup -h
```



