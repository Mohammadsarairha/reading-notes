# File and Stream I/O

## Files and directories

- File : Is collection of bytes that has specific storage , When we wor k with file that mean we work with path and storage and name.

- System.IO : Is one of built in class have namespaces contain types that enable reading and writing.

## file and directory classes

### There some of common classes deal with file and directory:

- File : Is static methods for creating, copying, deleting, moving, and opening files.

- FileInfo : Is for instance methods for creating, copying, deleting, moving, and opening files.

- Directory : Is static methods for creating, moving directorys.

- Path : Is methods provides you to work with paths.

## Streams

- Streams is base class make read and write bytes , And work with operating system and underlying devices.

### There some of classes deal with streams:

- FileStream : for reading and writing to a file.

- IsolatedStorageFileStream : for reading and writing to a file in isolated storage.

- MemoryStream : for reading and writing to memory as the backing store.

- BufferedStream : for improving performance of read and write operations.

- NetworkStream : for reading and writing over network sockets.

- PipeStream : for reading and writing over anonymous and named pipes.

- CryptoStream : for linking data streams to cryptographic transformations.

## Readers and writers

- The System.IO namespace also provides you to deal and reading encoded characters from streams , And writing them to streams. 

- Streams are designed for byte input and output. 

- The reader and writer types handle the conversion of the encoded characters to and from bytes

### There some of classes deal with reader and writer:

- BinaryReader and BinaryWriter : for reading and writing data types as binary values (0 - 1).

- StreamReader and StreamWriter : for reading and writing convert the characters to and from bytes.

- StringReader and StringWriter : for reading and writing characters to and from strings.

- TextReader and TextWriter : Is Abstract base classes read and write characters and strings.

## Asynchronous I/O operations

### What are you doing if your app need to read or write big data ??

- There is to way to deal with that :
    1. Asynchronous : With Asynchronous I/O operations no need to stop your app working tell ist done .

    2. Synchronous : With Synchronous I/O operations is block all your resorse and you app stopped working.

    3. keywords for Asynchronous : Async and await for method Ex :

    ```C#
    private async void Button_Click(object sender, RoutedEventArgs e)
        {
             await sourceStream.CopyToAsync(destinationStream);
        }
    ```

## What Does Isolated Storage Mean?

- Isolated storage : Is  serves as a virtual file system managed by the .NET Common Language Runtime (CLR).

- stream and serialization methods may be used to read and write data.


# How to: Write text to a file

- There is to many way to use System.io class  to write files , There is some way to dp that.

- Defulte file is in bin file in your project . 
### Synchronously write text

```C# 
using System;
using System.IO;

class Program
{
    static void Main(string[] args)
    {

        String path = "WriteLines.txt";
        String text  = "First Second Third "
        File.WriteAllText(path,text);

    }
}
```
- Output

```bash
First Second Third
```


# How to: Read text from a file

- There is to many way to use System.io class  to write files , There is some way to dp that.

```C#
using System;
using System.IO;

class Program
{
    public static void Main()
    {
        // File path
        string text = File.ReadAllText(@"C:\Users\HP\Documents\WriteLines.txt");

        // Display the file contents to the console. Variable text is a string.
        Console.WriteLine(text);

    }
}
```

- Output

```bash
First Second Third
```
