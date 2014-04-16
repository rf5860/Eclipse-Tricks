# Eclipse-Tricks

Tips and Tricks for making Eclipse more Productive

## Content Assist

By default, content assist is set to trigger on '.'. So if you have a basic class:
```java
public class A {
  private String a;
  public String getA(){return a;}
  public void setA(String a){ this.a = a;}
  
  public void doThing() { System.out.println("Thing");}
  public void doOther() { System.out.println("Other");}
}
```

Then you have an instance of that class elsewhere:
```java
A someA = new A();
```

If you type the following, you should get some content assist for the relevant methods:
```java
someA.
```

![Standard Content Assist](resources/old-ca.gif)

This is cool - but wouldn't it be *better* if we could get content assist that felt more... intelligent? Well, the great news is that we can!
Under Windows --> Preferences --> Java --> Editor --> Content Assist

![Content Assist Settings](resources/ca.png)

They key parts are:

*Auto activation delay* and *Auto activiation triggers for Java*.

Changing the delay to 1 ms and the triggers to '.abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ' results in some really cool features.

If I now have:
```java
so
```

Content assist will offer some sugestions - like someA. If it's the only suggestion, typing "." will auto-complete the variable for us - neat!

This now enables us to have some really cool camel-case completion of methods as well. Typing:

```java
someA.dT
```

The suggestion doThing will automatically appear. Typing ';' will then autocomplete that line. Awesome.

![New Content Assist](resources/new-ca.gif)

## Favourites

## Templates
