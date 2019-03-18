# pyspark-analytics-workshop

Some helper code to get setup for a workshop on using
 pyspark for big data analytics

## Setup
### Create a virtualenv
- `cd pyspark-analytics-workshop`
- `virtualenv venv_spark_workshop`
- `. venv_spark_workshop/bin/activate`
- `pip install -r requirements.txt`
- `ipython kernel install --user --name=pyspark-workshop`

## Starting local pyspark
Start pyspark using a jupyter notebook environment. This should automatically open a browser window.
When you start a notebook from here, the spark context will be available in a variable `spark`.

- `cd notebooks`
- `SPARK_HOME="$(ls -d ../venv_spark_workshop/lib/python*)/site-packages/pyspark" PYSPARK_DRIVER_PYTHON=jupyter PYSPARK_DRIVER_PYTHON_OPTS='notebook' pyspark`
  - Note: if you have a spark already installed globally, do not set `SPARK_HOME` here