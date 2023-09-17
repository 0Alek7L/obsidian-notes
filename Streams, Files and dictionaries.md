#Advanced 
!!Всеки stream има buffer!!

**absolute path** - the whole path
**relative path** - gradually going folder to folder

**Using StreamReader**
 - The *using(...)* statement closes properly the stream at the end

**.Peek**
	Returns an integer representing the next character to be read, or -1 if there are no characters to be read or if the stream does not support seeking.

 var reader = new StreamReader(filename);
     using(reader)
    {
        //Use the reader here, e.g.
        string line = reader.ReadLine();
    }

reader.Read -> reads next character's ASCII code
(char)reader.Read -> reads next character
reader.ReadToEnd -> reads everything

**Path.GetFullPath(".")**

To exit the current folder and get to the other use ../
`StreamReader reader=new StreamReader("../input.txt");

---
**Directory & FileInfo**

    string[] fileNames = Directory.GetFiles(inputFolderPath);
    foreach(var file in fileNames)
    {
    FileInfo fileInfo = new(file);
    }
fileInfo.Extension
fileInfo.DirectoryName
fileInfo.Exists

---
**File**

File.Copy(sourceFileName, destFileName)
File.Create(stringPath)
File.Delete(path)
File.Move((sourceFileName, destFileName)
File.ReadAllLines(path)
File.ReadAllText(path)
---
**ZIP**

string inputFile = @"..\..\..\copyMe.png";
string zipArchiveFile = @"..\..\..\archive.zip";
string extractedFile = @"....\..\extracted.png";
var fileName= Path.GetFileName(inputFile);
    - To Zip
using ZipArchive archive = ZipFile.Open(zipArchiveFilePath, ZipArchiveMode.Create);
string fileName = Path.GetFileName(inputFilePath);
archive.CreateEntryFromFile(inputFilePath, fileName);
    - To Unzip
using ZipArchive archive = ZipFile.OpenRead(zipArchiveFilePath); 
ZipArchiveEntry fileForExtraction = archive.GetEntry(fileName);
fileForExtraction.ExtractToFile(outputFilePath);
[[Sets and Dictionaries]]