```
curl "http://cdnbakmi.kaltura.com/content/clientlibs/java_22-06-2016.tar.gz" > ~/downloads/kaltura-java.tar.gz
cd ~/downloads
tar -xvf kaltura-java.tar.gz
cd java
mvn assembly:assembly -DdescriptorId=jar-with-dependencies -Dmaven.test.skip=true

cd /path/to/this/repo
javac -cp ~/downloads/java/target/KalturaClient-3.3.1-jar-with-dependencies.jar com/kaltura/code/example/CodeExample.java
java -cp ~/downloads/java/target/KalturaClient-3.3.1-jar-with-dependencies.jar:. com.kaltura.code.example.CodeExample
```
