# Java - Hello World <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTAz787-8JSk6nbHfpnh5FCRop-aDMcrDBzLdMp135Okw&s" width=100 alt="Java logo" align="right">

Java is a general-purpose programming language that is class-based, object-oriented, and designed to have as few implementation dependencies as possible. It is intended to let application developers write once, run anywhere (WORA), meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.

## Hello World Program
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

This is a simple program that displays the string `Hello, World!` to the standard output.

To run this program
```bash
javac HelloWorld.java
java HelloWorld
```

## ***NEW HELLO WORLD***
```java
void main() {
    System.out.println("Hello, World!");
}
```

### From [Java update #jep-463](https://openjdk.org/jeps/463) onwards, Java 22 is released with new features and enhancements.

JEP 463: Implicitly Declared Classes and Instance Main Methods (Second Preview)
-   Relates to: [JEP 445: Unnamed Classes and Instance Main Methods (Preview)](https://openjdk.org/jeps/445)

> With Java 21, this initial step has been shortened. You can define a source code file, say, HelloWorld.java,
> with the following code, to print a message to the console (it doesn’t need to define a class;
> it has a shorter signature for method main()):
>> [JetBrains Blog - Java 22 and IntelliJ IDEA](https://blog.jetbrains.com/idea/2024/03/java-22-and-intellij-idea/).

***However***,  unnamed classes are a preview feature and are disabled by default.
To enable them, you need to use the `--enable-preview` flag.

To run this program
```bash
# --enable-preview is used to enable preview features and  --enable-preview must be used with either -source or --release
javac --enable-preview --source 22 HelloWorld.java
# Preview features are not enabled for Main if --enable-preview is not used
java --enable-preview HelloWorld
```