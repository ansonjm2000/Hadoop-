PIG

cd course/softwares

#downloading PIG
wget https://archive.apache.org/dist/pig/pig-0.17.0/pig-0.17.0.tar.gz

#unzipping the pig folder
tar -xzf pig-0.17.0.tar.gz
mv pig-0.17.0 pig

nano ~/.bashrc
export PIG_HOME=$HOME/Desktop/course/softwares/pig
export PATH=$PATH:$PIG_HOME/sbin:$PIG_HOME/bin
export CLASSPATH=$CLASSPATH:$PIG_HOME/lib/*
export PIG_CLASSPATH=$PIG_HOME/conf:$HADOOP_HOME/etc/hadoop
export PIG_CONF_DIR=$PIG_HOME/conf
export PIG_CLASSPATH=$PIG_CONF_DIR:$PATH

source ~/.bashrc

start-dfs.sh
start-yarn.sh
hdfs dfs -put /home/anson/hadoopdata/empdata.csv /user/data/empdata_pig.csv

pig 

