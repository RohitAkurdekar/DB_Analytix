# Apache installation in UBUNTU

__Install JAVA__:

    sudo apt install openjdk-8-jre
    
__Download Spark__:

https://spark.apache.org/downloads.html

* Download Apache Spark from above link.
* Go to Download folder and Unzip file

      cd ~/Downloads/
      tar xzvf spark-*****.tgz 

* Make a directory with name 'spark':

      sudo mkdir /usr/local/spark

* Change directory on terminal to:

      cd ~/Downloads/spark***/
      
* Move all data to newly created directory:

      sudo mv * /usr/local/spark/
    
* Install python2

      sudo apt install python2
      
* Open __bashrc__ file in editing mode:

      sudo nano ~/.bashrc     
  
Verify path using of spark and python:

      whereis <name>
    
* Add following lines in bashrc file:

      SPARK_HOME=/usr/local/spark
      export PATH="$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin"
      export PATH="/usr/local/spark/python:$PATH"

      export PYTHONPATH=$PYTHONPAH:/usr/lib/python2.7
      export PYSPARK_PYTHON=python2.7
      
* Run bashrc using source command:

      source ~/.bashrc
      
--------------------------------------------------------------------------------------------

__Run spark shell__:

      spark-shell
      
__Run Spark shell using python__:

      pyspark
      
---------------------------------------------------------------------------------------------

2023, Rohit Akurdekar.
