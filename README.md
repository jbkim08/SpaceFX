## SpaceFX
A simple tiny space game written in JavaFX.

The "dev" branch contains new developments that might come to the game later on. The "simpleversion" branch is like the name says more simple and should also run on
embedded devices etc. 
The "master" branch now contains some more fun things like enemies attacking in waves, a level boss that needs more hits to kill, enemies that drop bombs and an
enemy boss that also fires rockets.
This "mobile" branch is like the name says for mobile devices, it contains exactly the same code that is used in the "master" branch but needs some adjustments.
At the moment you cannot use sound on the mobile platform so this has to be disabled and other things.
Be aware that the "mobile" branch is using maven where the other branches use gradle, this will change in the future and is only temporary.

Donations are welcome at [Paypal](https://paypal.me/hans0l0)

### Overview
![Overview](https://raw.githubusercontent.com/HanSolo/SpaceFX/mobile/SpaceFX_iOS.png)


### Run SpaceFX on iOS (you need OS X to compile it)
To compile/run SpaceFX on an iOS device you will need JDK 11 and you should follow the instructions from [gluon](https://github.com/gluonhq/client-samples)

Make sure that in the pom.xml file the right target is configured as follows:

```
<plugin>
    <groupId>com.gluonhq</groupId>
    <artifactId>client-maven-plugin</artifactId>
    <version>${client.plugin.version}</version>
    <configuration>
        <target>ios</target>        
        ...
    </configuration>
</plugin>
```

You need to have an Apple developer account and your device must be registered for development.
Make sure that your device is connected to your computer.

If your setup is correct you can build the iOS version by using the following commands on the console:
```
export JAVA_HOME=$GRAALVM_HOME

mvn clean client:build

mvn client:run
```

### Run SpaceFX on Android (you need Linux to compile it)
To compile/run SpaceFX on an Android device you will need JDK 11 and you should follow the instructions from [gluon](https://github.com/gluonhq/client-samples)

Make sure that in the pom.xml file the right target is configured as follows:

```
<plugin>
    <groupId>com.gluonhq</groupId>
    <artifactId>client-maven-plugin</artifactId>
    <version>${client.plugin.version}</version>
    <configuration>
        <target>android</target>        
        ...
    </configuration>
</plugin>
```

Your device must be enabled as a developer device.
Make sure that your device is connected to your computer.

If your setup is correct you can build the Android version by using the following commands on the console:
`
export JAVA_HOME=$GRAALVM_HOME

mvn clean client:build

mvn client:run
