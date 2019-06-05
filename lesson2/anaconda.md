## init 
* Python 3.6、Jupyter Notebook、NumPy、pandas、Matplotlib 和 Seaborn。
```
conda install pandas 
conda install numpy pandas
conda create -n data python=3.7 numpy pandas

```
* install notebook
```
conda install jupyter notebook
```

## install 
```
conda install package_name
```

## manageing environments
* use conda create -n env_name list of packages in your terminal. Here -n env_name sets the name of your environment (-n for name) and list of packages is the list of packages you want installed in the environment. For example, to create an environment named my_env and install numpy in it, type conda create -n my_env numpy.

```
conda craete -n env_name list of packages

```
## search packages
```
conda search *package_name* | grep -v 'py\d\d'
```

*  To create an environment with a specific Python version, do something like conda create -n py3 python=3 or conda create -n py2 python=2. 

```
conda craete -n py3 pathon=3
```

## enter and leave environment 
```
conda activate my_env
conda deactivate my_env

cource activate my_env
cource deactivate my_env
```

## Saving and loading environments
* A really useful feature is sharing environments so others can install all the packages used in your code, with the correct versions. You can save the packages to a YAML file with 

* The first part conda env export writes out all the packages in the environment, including the Python version.
```
conda env export > environment.yaml
```
* To create an environment from an environment file use conda env create -f environment.yaml. This will create a new environment with the same name listed in environment.yaml.
```
conda env create -f environment.yaml
```

## Listing environments
* If you forget what your environments are named (happens to me sometimes), use conda env list to list out all the environments you've created.
```
conda env list
```

## Removing environments
* If there are environments you don't use anymore, conda env remove -n env_name will remove the specified environment (here, named env_name).
```
conda env remove -n env_name
```

